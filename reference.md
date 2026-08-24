# Reference
## Stores
<details><summary><code>client.stores.<a href="/src/api/resources/stores/client/Client.ts">list</a>() -> Leal.ListStoresResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns every store the authenticated user has access to, including summary counts for locations, cards, customers, and posters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stores.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StoresClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stores.<a href="/src/api/resources/stores/client/Client.ts">get</a>({ ...params }) -> Leal.GetStoresResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns detailed information for a single store, including summary counts for its associated resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stores.get({
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.GetStoresRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StoresClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stores.<a href="/src/api/resources/stores/client/Client.ts">update</a>({ ...params }) -> Leal.UpdateStoresResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the store's name or store_name. Use `store_name` for the public-facing name displayed to customers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stores.update({
    id: 1,
    account: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.UpdateStoresRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StoresClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Cards
<details><summary><code>client.cards.<a href="/src/api/resources/cards/client/Client.ts">list</a>({ ...params }) -> Leal.ListCardsResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns loyalty card templates for the specified store. By default, only
active (unarchived) cards are returned. Use the `scope` parameter to include
archived cards.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.cards.list({
    account_id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.ListCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.cards.<a href="/src/api/resources/cards/client/Client.ts">create</a>({ ...params }) -> Leal.CreateCardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new loyalty stamp card template for the store. The card defines the
visual design (colours, icon, strip) and program rules (stamps required,
initial stamps).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.cards.create({
    account_id: 1,
    card: {
        name: "name"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.CreateCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.cards.<a href="/src/api/resources/cards/client/Client.ts">get</a>({ ...params }) -> Leal.GetCardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single loyalty card template by ID, including reward and customer card counts.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.cards.get({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.GetCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.cards.<a href="/src/api/resources/cards/client/Client.ts">update</a>({ ...params }) -> Leal.UpdateCardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing loyalty card template. Only the provided attributes are changed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.cards.update({
    account_id: 1,
    id: 1,
    card: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.UpdateCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customers
<details><summary><code>client.customers.<a href="/src/api/resources/customers/client/Client.ts">list</a>({ ...params }) -> Leal.ListCustomersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of customers for the store. Use the `search` parameter to filter
by name, email, phone, card code (barcode), or external reference ID. Alternatively, pass
`source` AND `external_id` together to perform an exact lookup by an external reference -
the response will contain at most one customer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customers.list({
    account_id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.ListCustomersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customers.<a href="/src/api/resources/customers/client/Client.ts">create</a>({ ...params }) -> Leal.CreateCustomersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new customer for the store. Requires `first_name` and at least one of `email` or `phone`.
Optionally enroll the customer in a loyalty card by passing `card_id`, and trigger delivery of
card links (email/SMS) by passing `send_card_links`. When a card with initial stamps is assigned,
those stamps are automatically applied as a welcome bonus.

Pass `metadata` to attach arbitrary key/value data, and `external_references` to link the
customer to records in other systems (e.g. Square, Shopify). External references are upserted
by `(source, external_id)` so this endpoint is safe to call with the same references twice.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customers.create({
    account_id: 1,
    customer: {
        first_name: "first_name"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.CreateCustomersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customers.<a href="/src/api/resources/customers/client/Client.ts">get</a>({ ...params }) -> Leal.GetCustomersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns detailed information about a single customer, including all of their
enrolled loyalty cards with stamp progress and wallet pass URLs (`apple_wallet_url`
and `google_wallet_url`) for each card. Also includes `metadata` and
`external_references` so you can sync state with external systems.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customers.get({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.GetCustomersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customers.<a href="/src/api/resources/customers/client/Client.ts">update</a>({ ...params }) -> Leal.UpdateCustomersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing customer's details. To add stamps or redeem rewards, use the
customer cards endpoints instead.

`metadata` is shallow-merged into the existing metadata. `external_references` are upserted
by `(source, external_id)` - to remove a reference, omit it from subsequent calls and use
a separate `DELETE` workflow (not yet exposed via API; manage in dashboard for now).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customers.update({
    account_id: 1,
    id: 1,
    customer: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.UpdateCustomersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Cards
<details><summary><code>client.customerCards.<a href="/src/api/resources/customerCards/client/Client.ts">list</a>({ ...params }) -> Leal.ListCustomerCardsResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all loyalty cards enrolled for a specific customer, including stamp progress,
status, wallet pass installation state, and wallet pass URLs (`apple_wallet_url` and
`google_wallet_url`) that you can use to let customers add their loyalty card to
Apple Wallet or Google Wallet from your own app or website.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customerCards.list({
    account_id: 1,
    customer_id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.ListCustomerCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomerCardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customerCards.<a href="/src/api/resources/customerCards/client/Client.ts">get</a>({ ...params }) -> Leal.GetCustomerCardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns detailed information about a specific customer card, including stamp progress,
a list of rewards the customer has earned enough stamps to redeem, and wallet pass URLs
(`apple_wallet_url` and `google_wallet_url`) for adding the card to Apple Wallet or
Google Wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customerCards.get({
    account_id: 1,
    customer_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.GetCustomerCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomerCardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customerCards.<a href="/src/api/resources/customerCards/client/Client.ts">redeem</a>({ ...params }) -> Leal.RedeemCustomerCardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Redeems a reward for a customer, deducting the required stamps from their card.
The customer must have enough stamps on this card to cover the reward's cost.
Triggers wallet pass updates and push notifications.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customerCards.redeem({
    account_id: 1,
    customer_id: 1,
    id: 1,
    reward_id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.RedeemCustomerCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomerCardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customerCards.<a href="/src/api/resources/customerCards/client/Client.ts">stamp</a>({ ...params }) -> Leal.StampCustomerCardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Adds stamps to a customer's loyalty card. Triggers ledger entries, wallet pass updates,
and push notifications. Pass `skip_notifications` to stamp silently.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customerCards.stamp({
    account_id: 1,
    customer_id: 1,
    id: 1,
    stamps: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.StampCustomerCardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomerCardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Locations
<details><summary><code>client.locations.<a href="/src/api/resources/locations/client/Client.ts">list</a>({ ...params }) -> Leal.ListLocationsResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns every physical location belonging to the specified store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.locations.list({
    account_id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.ListLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.locations.<a href="/src/api/resources/locations/client/Client.ts">create</a>({ ...params }) -> Leal.CreateLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new physical location for the store. The provided address is
automatically geocoded to latitude and longitude coordinates in the background.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.locations.create({
    account_id: 1,
    location: {
        address: "address",
        name: "name"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.CreateLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.locations.<a href="/src/api/resources/locations/client/Client.ts">get</a>({ ...params }) -> Leal.GetLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single location by ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.locations.get({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.GetLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.locations.<a href="/src/api/resources/locations/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently deletes a location. This action cannot be undone.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.locations.delete({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.DeleteLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.locations.<a href="/src/api/resources/locations/client/Client.ts">update</a>({ ...params }) -> Leal.UpdateLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing location. If the address is changed, it will be re-geocoded automatically.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.locations.update({
    account_id: 1,
    id: 1,
    location: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.UpdateLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Posters
<details><summary><code>client.posters.<a href="/src/api/resources/posters/client/Client.ts">list</a>({ ...params }) -> Leal.ListPostersResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all posters for the store. Optionally filter by card or active status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.posters.list({
    account_id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.ListPostersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PostersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posters.<a href="/src/api/resources/posters/client/Client.ts">create</a>({ ...params }) -> Leal.CreatePostersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new printable QR code poster for customer signup. The poster will automatically
generate a unique public signup URL and QR code. The `card_id` is required on create to
associate the poster with a loyalty card.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.posters.create({
    account_id: 1,
    poster: {
        card_id: 1
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.CreatePostersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PostersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posters.<a href="/src/api/resources/posters/client/Client.ts">get</a>({ ...params }) -> Leal.GetPostersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single poster by ID, including generated signup and display URLs.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.posters.get({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.GetPostersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PostersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posters.<a href="/src/api/resources/posters/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently deletes a poster. The public signup URL will stop working.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.posters.delete({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.DeletePostersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PostersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posters.<a href="/src/api/resources/posters/client/Client.ts">update</a>({ ...params }) -> Leal.UpdatePostersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing poster. The `card_id` cannot be changed after creation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.posters.update({
    account_id: 1,
    id: 1,
    poster: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.UpdatePostersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PostersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Rewards
<details><summary><code>client.rewards.<a href="/src/api/resources/rewards/client/Client.ts">list</a>({ ...params }) -> Leal.ListRewardsResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all rewards for the store. Optionally filter by card or active status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.rewards.list({
    account_id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.ListRewardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.rewards.<a href="/src/api/resources/rewards/client/Client.ts">create</a>({ ...params }) -> Leal.CreateRewardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new reward for a loyalty card. The card must belong to the same store.
The `card_id` is required on create but cannot be changed afterwards.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.rewards.create({
    account_id: 1,
    reward: {
        card_id: 1,
        name: "name",
        stamps_required: 1
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.CreateRewardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.rewards.<a href="/src/api/resources/rewards/client/Client.ts">get</a>({ ...params }) -> Leal.GetRewardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single reward by ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.rewards.get({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.GetRewardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.rewards.<a href="/src/api/resources/rewards/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently deletes a reward. This cannot be undone.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.rewards.delete({
    account_id: 1,
    id: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.DeleteRewardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.rewards.<a href="/src/api/resources/rewards/client/Client.ts">update</a>({ ...params }) -> Leal.UpdateRewardsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing reward. The `card_id` cannot be changed after creation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.rewards.update({
    account_id: 1,
    id: 1,
    reward: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Leal.UpdateRewardsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Status
<details><summary><code>client.status.<a href="/src/api/resources/status/client/Client.ts">check</a>() -> Leal.CheckStatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the status of the API. No authentication required.

Every response from this API, including this one, carries `RateLimit-Limit`,
`RateLimit-Remaining`, `RateLimit-Reset` and `RateLimit-Policy`. Exceeding
the limit returns 429 with `Retry-After` in seconds.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.status.check();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StatusClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

