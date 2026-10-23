# eshop-webhooks — Webhooks service

Webhook subscriptions with grant-URL verification; forwards order and price events to subscribers over HTTP.

Part of the eshop-estate: dotnet/eShop `913acea` split into one repository per service. Clone every `eshop-*` repository into the same folder; project references and the app host point at sibling folders.

## Projects

- `src/Webhooks.API`
- `tests/Webhooks.FunctionalTests`
- `tests/Webhooks.UnitTests`

## Depends on

- eshop-platform (EventBus, EventBusRabbitMQ, IntegrationEventLogEF, ServiceDefaults)

## Consumes

- `OrderStatusChangedToPaidIntegrationEvent`
- `OrderStatusChangedToShippedIntegrationEvent`
- `ProductPriceChangedIntegrationEvent`

## Tables

- `Subscriptions`

## Tests

4 test methods under `tests/`.

## Build

```
dotnet build eshop-webhooks.slnx
```

Run the estate from `eshop-apphost` (`dotnet run --project src/eShop.AppHost`).

## License

MIT, as dotnet/eShop (see `LICENSE`). Derived from https://github.com/dotnet/eShop at `913acea`; the split and the reporting service are CogniDev test fixtures.
