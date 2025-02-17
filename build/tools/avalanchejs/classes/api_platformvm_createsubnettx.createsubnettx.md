[avalanche](../README.md) › [API-PlatformVM-CreateSubnetTx](../modules/api_platformvm_createsubnettx.md) › [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md)

# Class: CreateSubnetTx

## Hierarchy

  ↳ [BaseTx](api_platformvm_basetx.basetx.md)

  ↳ **CreateSubnetTx**

## Index

### Constructors

* [constructor](api_platformvm_createsubnettx.createsubnettx.md#constructor)

### Properties

* [_codecID](api_platformvm_createsubnettx.createsubnettx.md#protected-_codecid)
* [_typeID](api_platformvm_createsubnettx.createsubnettx.md#protected-_typeid)
* [_typeName](api_platformvm_createsubnettx.createsubnettx.md#protected-_typename)
* [blockchainID](api_platformvm_createsubnettx.createsubnettx.md#protected-blockchainid)
* [ins](api_platformvm_createsubnettx.createsubnettx.md#protected-ins)
* [memo](api_platformvm_createsubnettx.createsubnettx.md#protected-memo)
* [networkID](api_platformvm_createsubnettx.createsubnettx.md#protected-networkid)
* [numins](api_platformvm_createsubnettx.createsubnettx.md#protected-numins)
* [numouts](api_platformvm_createsubnettx.createsubnettx.md#protected-numouts)
* [outs](api_platformvm_createsubnettx.createsubnettx.md#protected-outs)
* [subnetOwners](api_platformvm_createsubnettx.createsubnettx.md#protected-subnetowners)

### Methods

* [clone](api_platformvm_createsubnettx.createsubnettx.md#clone)
* [create](api_platformvm_createsubnettx.createsubnettx.md#create)
* [deserialize](api_platformvm_createsubnettx.createsubnettx.md#deserialize)
* [fromBuffer](api_platformvm_createsubnettx.createsubnettx.md#frombuffer)
* [getBlockchainID](api_platformvm_createsubnettx.createsubnettx.md#getblockchainid)
* [getCodecID](api_platformvm_createsubnettx.createsubnettx.md#getcodecid)
* [getIns](api_platformvm_createsubnettx.createsubnettx.md#getins)
* [getMemo](api_platformvm_createsubnettx.createsubnettx.md#getmemo)
* [getNetworkID](api_platformvm_createsubnettx.createsubnettx.md#getnetworkid)
* [getOuts](api_platformvm_createsubnettx.createsubnettx.md#getouts)
* [getSubnetOwners](api_platformvm_createsubnettx.createsubnettx.md#getsubnetowners)
* [getTotalOuts](api_platformvm_createsubnettx.createsubnettx.md#gettotalouts)
* [getTxType](api_platformvm_createsubnettx.createsubnettx.md#gettxtype)
* [getTypeID](api_platformvm_createsubnettx.createsubnettx.md#gettypeid)
* [getTypeName](api_platformvm_createsubnettx.createsubnettx.md#gettypename)
* [select](api_platformvm_createsubnettx.createsubnettx.md#select)
* [serialize](api_platformvm_createsubnettx.createsubnettx.md#serialize)
* [sign](api_platformvm_createsubnettx.createsubnettx.md#sign)
* [toBuffer](api_platformvm_createsubnettx.createsubnettx.md#tobuffer)
* [toString](api_platformvm_createsubnettx.createsubnettx.md#tostring)

## Constructors

###  constructor

\+ **new CreateSubnetTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [TransferableOutput](api_platformvm_outputs.transferableoutput.md)[], `ins`: [TransferableInput](api_platformvm_inputs.transferableinput.md)[], `memo`: Buffer, `subnetOwners`: [SECPOwnerOutput](api_platformvm_outputs.secpowneroutput.md)): *[CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md)*

*Overrides [BaseTx](api_platformvm_basetx.basetx.md).[constructor](api_platformvm_basetx.basetx.md#constructor)*

*Defined in [src/apis/platformvm/createsubnettx.ts:75](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L75)*

Class representing an unsigned Create Subnet transaction.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`networkID` | number | DefaultNetworkID | Optional networkID, [DefaultNetworkID](../modules/utils_constants.md#const-defaultnetworkid) |
`blockchainID` | Buffer | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16) |
`outs` | [TransferableOutput](api_platformvm_outputs.transferableoutput.md)[] | undefined | Optional array of the [TransferableOutput](api_platformvm_outputs.transferableoutput.md)s |
`ins` | [TransferableInput](api_platformvm_inputs.transferableinput.md)[] | undefined | Optional array of the [TransferableInput](api_platformvm_inputs.transferableinput.md)s |
`memo` | Buffer | undefined | Optional [Buffer](https://github.com/feross/buffer) for the memo field |
`subnetOwners` | [SECPOwnerOutput](api_platformvm_outputs.secpowneroutput.md) | undefined | Optional [SECPOwnerOutput](api_platformvm_outputs.secpowneroutput.md) class for specifying who owns the subnet.  |

**Returns:** *[CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md)*

## Properties

### `Protected` _codecID

• **_codecID**: *number* = undefined

*Inherited from [SigIdx](common_signature.sigidx.md).[_codecID](common_signature.sigidx.md#protected-_codecid)*

*Defined in [src/utils/serialization.ts:40](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L40)*

___

### `Protected` _typeID

• **_typeID**: *number* = PlatformVMConstants.CREATESUBNETTX

*Overrides [BaseTx](api_platformvm_basetx.basetx.md).[_typeID](api_platformvm_basetx.basetx.md#protected-_typeid)*

*Defined in [src/apis/platformvm/createsubnettx.ts:16](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L16)*

___

### `Protected` _typeName

• **_typeName**: *string* = "SECPCredential"

*Overrides [BaseTx](api_platformvm_basetx.basetx.md).[_typeName](api_platformvm_basetx.basetx.md#protected-_typename)*

*Defined in [src/apis/platformvm/createsubnettx.ts:15](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L15)*

___

### `Protected` blockchainID

• **blockchainID**: *Buffer* = Buffer.alloc(32)

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[blockchainID](common_transactions.standardbasetx.md#protected-blockchainid)*

*Defined in [src/common/tx.ts:52](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L52)*

___

### `Protected` ins

• **ins**: *[StandardTransferableInput](common_inputs.standardtransferableinput.md)[]*

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[ins](common_transactions.standardbasetx.md#protected-ins)*

*Defined in [src/common/tx.ts:56](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L56)*

___

### `Protected` memo

• **memo**: *Buffer* = Buffer.alloc(0)

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[memo](common_transactions.standardbasetx.md#protected-memo)*

*Defined in [src/common/tx.ts:57](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L57)*

___

### `Protected` networkID

• **networkID**: *Buffer* = Buffer.alloc(4)

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[networkID](common_transactions.standardbasetx.md#protected-networkid)*

*Defined in [src/common/tx.ts:51](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L51)*

___

### `Protected` numins

• **numins**: *Buffer* = Buffer.alloc(4)

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[numins](common_transactions.standardbasetx.md#protected-numins)*

*Defined in [src/common/tx.ts:55](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L55)*

___

### `Protected` numouts

• **numouts**: *Buffer* = Buffer.alloc(4)

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[numouts](common_transactions.standardbasetx.md#protected-numouts)*

*Defined in [src/common/tx.ts:53](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L53)*

___

### `Protected` outs

• **outs**: *[StandardTransferableOutput](common_output.standardtransferableoutput.md)[]*

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[outs](common_transactions.standardbasetx.md#protected-outs)*

*Defined in [src/common/tx.ts:54](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L54)*

___

### `Protected` subnetOwners

• **subnetOwners**: *[SECPOwnerOutput](api_platformvm_outputs.secpowneroutput.md)* = undefined

*Defined in [src/apis/platformvm/createsubnettx.ts:31](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L31)*

## Methods

###  clone

▸ **clone**(): *this*

*Inherited from [BaseTx](api_platformvm_basetx.basetx.md).[clone](api_platformvm_basetx.basetx.md#clone)*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[clone](common_transactions.standardbasetx.md#abstract-clone)*

*Defined in [src/apis/platformvm/basetx.ts:133](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/basetx.ts#L133)*

**Returns:** *this*

___

###  create

▸ **create**(...`args`: any[]): *this*

*Inherited from [BaseTx](api_platformvm_basetx.basetx.md).[create](api_platformvm_basetx.basetx.md#create)*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[create](common_transactions.standardbasetx.md#abstract-create)*

*Defined in [src/apis/platformvm/basetx.ts:139](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/basetx.ts#L139)*

**Parameters:**

Name | Type |
------ | ------ |
`...args` | any[] |

**Returns:** *this*

___

###  deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/src_utils.md#serializedencoding)): *void*

*Overrides [BaseTx](api_platformvm_basetx.basetx.md).[deserialize](api_platformvm_basetx.basetx.md#deserialize)*

*Defined in [src/apis/platformvm/createsubnettx.ts:25](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L25)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`fields` | object | - |
`encoding` | [SerializedEncoding](../modules/src_utils.md#serializedencoding) | "hex" |

**Returns:** *void*

___

###  fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): *number*

*Overrides [BaseTx](api_platformvm_basetx.basetx.md).[fromBuffer](api_platformvm_basetx.basetx.md#frombuffer)*

*Defined in [src/apis/platformvm/createsubnettx.ts:57](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L57)*

Takes a [Buffer](https://github.com/feross/buffer) containing an [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md), parses it, populates the class, and returns the length of the [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md) in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`bytes` | Buffer | - | A [Buffer](https://github.com/feross/buffer) containing a raw [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md) |
`offset` | number | 0 | A number for the starting position in the bytes.  |

**Returns:** *number*

The length of the raw [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md)

___

###  getBlockchainID

▸ **getBlockchainID**(): *Buffer*

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[getBlockchainID](common_transactions.standardbasetx.md#getblockchainid)*

*Defined in [src/common/tx.ts:72](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L72)*

Returns the Buffer representation of the BlockchainID

**Returns:** *Buffer*

___

###  getCodecID

▸ **getCodecID**(): *number*

*Inherited from [SigIdx](common_signature.sigidx.md).[getCodecID](common_signature.sigidx.md#getcodecid)*

*Defined in [src/utils/serialization.ts:59](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L59)*

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** *number*

___

###  getIns

▸ **getIns**(): *[TransferableInput](api_platformvm_inputs.transferableinput.md)[]*

*Inherited from [BaseTx](api_platformvm_basetx.basetx.md).[getIns](api_platformvm_basetx.basetx.md#getins)*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[getIns](common_transactions.standardbasetx.md#abstract-getins)*

*Defined in [src/apis/platformvm/basetx.ts:52](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/basetx.ts#L52)*

**Returns:** *[TransferableInput](api_platformvm_inputs.transferableinput.md)[]*

___

###  getMemo

▸ **getMemo**(): *Buffer*

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[getMemo](common_transactions.standardbasetx.md#getmemo)*

*Defined in [src/common/tx.ts:92](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L92)*

Returns the [Buffer](https://github.com/feross/buffer) representation of the memo

**Returns:** *Buffer*

___

###  getNetworkID

▸ **getNetworkID**(): *number*

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[getNetworkID](common_transactions.standardbasetx.md#getnetworkid)*

*Defined in [src/common/tx.ts:67](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L67)*

Returns the NetworkID as a number

**Returns:** *number*

___

###  getOuts

▸ **getOuts**(): *[TransferableOutput](api_platformvm_outputs.transferableoutput.md)[]*

*Inherited from [BaseTx](api_platformvm_basetx.basetx.md).[getOuts](api_platformvm_basetx.basetx.md#getouts)*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[getOuts](common_transactions.standardbasetx.md#abstract-getouts)*

*Defined in [src/apis/platformvm/basetx.ts:48](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/basetx.ts#L48)*

**Returns:** *[TransferableOutput](api_platformvm_outputs.transferableoutput.md)[]*

___

###  getSubnetOwners

▸ **getSubnetOwners**(): *[SECPOwnerOutput](api_platformvm_outputs.secpowneroutput.md)*

*Defined in [src/apis/platformvm/createsubnettx.ts:43](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L43)*

Returns a [Buffer](https://github.com/feross/buffer) for the reward address.

**Returns:** *[SECPOwnerOutput](api_platformvm_outputs.secpowneroutput.md)*

___

###  getTotalOuts

▸ **getTotalOuts**(): *[TransferableOutput](api_platformvm_outputs.transferableoutput.md)[]*

*Inherited from [BaseTx](api_platformvm_basetx.basetx.md).[getTotalOuts](api_platformvm_basetx.basetx.md#gettotalouts)*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[getTotalOuts](common_transactions.standardbasetx.md#abstract-gettotalouts)*

*Defined in [src/apis/platformvm/basetx.ts:57](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/basetx.ts#L57)*

**Returns:** *[TransferableOutput](api_platformvm_outputs.transferableoutput.md)[]*

___

###  getTxType

▸ **getTxType**(): *number*

*Overrides [BaseTx](api_platformvm_basetx.basetx.md).[getTxType](api_platformvm_basetx.basetx.md#gettxtype)*

*Defined in [src/apis/platformvm/createsubnettx.ts:36](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L36)*

Returns the id of the [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md)

**Returns:** *number*

___

###  getTypeID

▸ **getTypeID**(): *number*

*Inherited from [SigIdx](common_signature.sigidx.md).[getTypeID](common_signature.sigidx.md#gettypeid)*

*Defined in [src/utils/serialization.ts:52](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L52)*

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** *number*

___

###  getTypeName

▸ **getTypeName**(): *string*

*Inherited from [SigIdx](common_signature.sigidx.md).[getTypeName](common_signature.sigidx.md#gettypename)*

*Defined in [src/utils/serialization.ts:45](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L45)*

Used in serialization. TypeName is a string name for the type of object being output.

**Returns:** *string*

___

###  select

▸ **select**(`id`: number, ...`args`: any[]): *this*

*Inherited from [BaseTx](api_platformvm_basetx.basetx.md).[select](api_platformvm_basetx.basetx.md#select)*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[select](common_transactions.standardbasetx.md#abstract-select)*

*Defined in [src/apis/platformvm/basetx.ts:143](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/basetx.ts#L143)*

**Parameters:**

Name | Type |
------ | ------ |
`id` | number |
`...args` | any[] |

**Returns:** *this*

___

###  serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/src_utils.md#serializedencoding)): *object*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[serialize](common_transactions.standardbasetx.md#serialize)*

*Defined in [src/apis/platformvm/createsubnettx.ts:18](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L18)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`encoding` | [SerializedEncoding](../modules/src_utils.md#serializedencoding) | "hex" |

**Returns:** *object*

___

###  sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_platformvm_keychain.keychain.md)): *[Credential](common_signature.credential.md)[]*

*Inherited from [BaseTx](api_platformvm_basetx.basetx.md).[sign](api_platformvm_basetx.basetx.md#sign)*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[sign](common_transactions.standardbasetx.md#abstract-sign)*

*Defined in [src/apis/platformvm/basetx.ts:116](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/basetx.ts#L116)*

Takes the bytes of an [UnsignedTx](api_platformvm_transactions.unsignedtx.md) and returns an array of [Credential](common_signature.credential.md)s

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`msg` | Buffer | A Buffer for the [UnsignedTx](api_platformvm_transactions.unsignedtx.md) |
`kc` | [KeyChain](api_platformvm_keychain.keychain.md) | An [KeyChain](api_platformvm_keychain.keychain.md) used in signing  |

**Returns:** *[Credential](common_signature.credential.md)[]*

An array of [Credential](common_signature.credential.md)s

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

*Overrides [StandardBaseTx](common_transactions.standardbasetx.md).[toBuffer](common_transactions.standardbasetx.md#tobuffer)*

*Defined in [src/apis/platformvm/createsubnettx.ts:67](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/apis/platformvm/createsubnettx.ts#L67)*

Returns a [Buffer](https://github.com/feross/buffer) representation of the [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx.md).

**Returns:** *Buffer*

___

###  toString

▸ **toString**(): *string*

*Inherited from [StandardBaseTx](common_transactions.standardbasetx.md).[toString](common_transactions.standardbasetx.md#tostring)*

*Defined in [src/common/tx.ts:129](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L129)*

Returns a base-58 representation of the [StandardBaseTx](common_transactions.standardbasetx.md).

**Returns:** *string*
