[@ai16z/eliza v1.0.0](../index.md) / IAgentRuntime

# Interface: IAgentRuntime

## Properties

### agentId

> **agentId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

Properties

#### Defined in

[packages/core/src/types.ts:520](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L520)

---

### serverUrl

> **serverUrl**: `string`

#### Defined in

[packages/core/src/types.ts:521](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L521)

---

### databaseAdapter

> **databaseAdapter**: [`IDatabaseAdapter`](IDatabaseAdapter.md)

#### Defined in

[packages/core/src/types.ts:522](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L522)

---

### token

> **token**: `string`

#### Defined in

[packages/core/src/types.ts:523](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L523)

---

### modelProvider

> **modelProvider**: [`ModelProviderName`](../enumerations/ModelProviderName.md)

#### Defined in

[packages/core/src/types.ts:524](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L524)

---

### character

> **character**: [`Character`](../type-aliases/Character.md)

#### Defined in

[packages/core/src/types.ts:525](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L525)

---

### providers

> **providers**: [`Provider`](Provider.md)[]

#### Defined in

[packages/core/src/types.ts:526](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L526)

---

### actions

> **actions**: [`Action`](Action.md)[]

#### Defined in

[packages/core/src/types.ts:527](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L527)

---

### evaluators

> **evaluators**: [`Evaluator`](Evaluator.md)[]

#### Defined in

[packages/core/src/types.ts:528](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L528)

---

### messageManager

> **messageManager**: [`IMemoryManager`](IMemoryManager.md)

#### Defined in

[packages/core/src/types.ts:530](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L530)

---

### descriptionManager

> **descriptionManager**: [`IMemoryManager`](IMemoryManager.md)

#### Defined in

[packages/core/src/types.ts:531](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L531)

---

### loreManager

> **loreManager**: [`IMemoryManager`](IMemoryManager.md)

#### Defined in

[packages/core/src/types.ts:532](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L532)

---

### services

> **services**: `Map`\<[`ServiceType`](../enumerations/ServiceType.md), [`Service`](../classes/Service.md)\>

#### Defined in

[packages/core/src/types.ts:534](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L534)

## Methods

### registerMemoryManager()

> **registerMemoryManager**(`manager`): `void`

#### Parameters

• **manager**: [`IMemoryManager`](IMemoryManager.md)

#### Returns

`void`

#### Defined in

[packages/core/src/types.ts:535](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L535)

---

### getMemoryManager()

> **getMemoryManager**(`name`): [`IMemoryManager`](IMemoryManager.md)

#### Parameters

• **name**: `string`

#### Returns

[`IMemoryManager`](IMemoryManager.md)

#### Defined in

[packages/core/src/types.ts:537](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L537)

---

### getService()

> **getService**\<`Service`\>(`service`): `Service`

#### Type Parameters

• **Service**

#### Parameters

• **service**: `string`

#### Returns

`Service`

#### Defined in

[packages/core/src/types.ts:539](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L539)

---

### registerService()

> **registerService**(`service`): `void`

#### Parameters

• **service**: [`Service`](../classes/Service.md)

#### Returns

`void`

#### Defined in

[packages/core/src/types.ts:541](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L541)

---

### getSetting()

> **getSetting**(`key`): `string`

#### Parameters

• **key**: `string`

#### Returns

`string`

#### Defined in

[packages/core/src/types.ts:543](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L543)

---

### getConversationLength()

> **getConversationLength**(): `number`

Methods

#### Returns

`number`

#### Defined in

[packages/core/src/types.ts:546](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L546)

---

### processActions()

> **processActions**(`message`, `responses`, `state`?, `callback`?): `Promise`\<`void`\>

#### Parameters

• **message**: [`Memory`](Memory.md)

• **responses**: [`Memory`](Memory.md)[]

• **state?**: [`State`](State.md)

• **callback?**: [`HandlerCallback`](../type-aliases/HandlerCallback.md)

#### Returns

`Promise`\<`void`\>

#### Defined in

[packages/core/src/types.ts:547](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L547)

---

### evaluate()

> **evaluate**(`message`, `state`?, `didRespond`?): `Promise`\<`string`[]\>

#### Parameters

• **message**: [`Memory`](Memory.md)

• **state?**: [`State`](State.md)

• **didRespond?**: `boolean`

#### Returns

`Promise`\<`string`[]\>

#### Defined in

[packages/core/src/types.ts:553](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L553)

---

### ensureParticipantExists()

> **ensureParticipantExists**(`userId`, `roomId`): `Promise`\<`void`\>

#### Parameters

• **userId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

• **roomId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

#### Returns

`Promise`\<`void`\>

#### Defined in

[packages/core/src/types.ts:558](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L558)

---

### ensureUserExists()

> **ensureUserExists**(`userId`, `userName`, `name`, `source`): `Promise`\<`void`\>

#### Parameters

• **userId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

• **userName**: `string`

• **name**: `string`

• **source**: `string`

#### Returns

`Promise`\<`void`\>

#### Defined in

[packages/core/src/types.ts:559](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L559)

---

### registerAction()

> **registerAction**(`action`): `void`

#### Parameters

• **action**: [`Action`](Action.md)

#### Returns

`void`

#### Defined in

[packages/core/src/types.ts:565](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L565)

---

### ensureConnection()

> **ensureConnection**(`userId`, `roomId`, `userName`?, `userScreenName`?, `source`?): `Promise`\<`void`\>

#### Parameters

• **userId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

• **roomId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

• **userName?**: `string`

• **userScreenName?**: `string`

• **source?**: `string`

#### Returns

`Promise`\<`void`\>

#### Defined in

[packages/core/src/types.ts:566](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L566)

---

### ensureParticipantInRoom()

> **ensureParticipantInRoom**(`userId`, `roomId`): `Promise`\<`void`\>

#### Parameters

• **userId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

• **roomId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

#### Returns

`Promise`\<`void`\>

#### Defined in

[packages/core/src/types.ts:573](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L573)

---

### ensureRoomExists()

> **ensureRoomExists**(`roomId`): `Promise`\<`void`\>

#### Parameters

• **roomId**: \`$\{string\}-$\{string\}-$\{string\}-$\{string\}-$\{string\}\`

#### Returns

`Promise`\<`void`\>

#### Defined in

[packages/core/src/types.ts:574](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L574)

---

### composeState()

> **composeState**(`message`, `additionalKeys`?): `Promise`\<[`State`](State.md)\>

#### Parameters

• **message**: [`Memory`](Memory.md)

• **additionalKeys?**

#### Returns

`Promise`\<[`State`](State.md)\>

#### Defined in

[packages/core/src/types.ts:575](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L575)

---

### updateRecentMessageState()

> **updateRecentMessageState**(`state`): `Promise`\<[`State`](State.md)\>

#### Parameters

• **state**: [`State`](State.md)

#### Returns

`Promise`\<[`State`](State.md)\>

#### Defined in

[packages/core/src/types.ts:579](https://github.com/ai16z/eliza/blob/main/packages/core/src/types.ts#L579)