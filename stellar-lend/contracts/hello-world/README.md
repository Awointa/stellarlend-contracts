# Hello-World Contract (StellarLend Core)

This contract exposes the core API for StellarLend, including lending/borrowing, cross-asset operations, bridges, analytics, monitoring, recovery/multisig, upgrades, data and configuration.

## Key Entry Points

- Initialization: `initialize(admin)`
- Core: `deposit_collateral`, `borrow`, `repay`, `withdraw`, `liquidate`
- Cross-Asset: `set_asset_params`, `deposit_collateral_asset`, `borrow_asset`, `repay_asset`, `withdraw_asset`, `get_cross_position_summary`
- Oracle & Pricing: `set_asset_price`, `oracle_*`, `set_price_cache_ttl`
- Governance: `gov_*`
- AMM: `set_amm_pool`, `amm_swap`, `amm_add_liquidity`, `amm_remove_liquidity`
- Flash Loans: `flash_loan`, `set_flash_loan_fee_bps`
- Bridge: `register_bridge`, `set_bridge_fee`, `bridge_deposit`, `bridge_withdraw`, `list_bridges`, `get_bridge_config`
- Analytics: metrics updated on core actions; getters via storage (see code)
- Monitoring: `monitor_report_health`, `monitor_report_performance`, `monitor_report_security`, `monitor_get`
- Recovery: `set_guardians`, `start_recovery`, `approve_recovery`, `execute_recovery`
- Multisig: `ms_set_admins`, `ms_propose_set_min_cr`, `ms_approve`, `ms_execute`
- Upgrade: `upgrade_propose`, `upgrade_approve`, `upgrade_execute`, `upgrade_rollback`, `upgrade_status`
- Data Store: `data_save`, `data_load`, `data_backup`, `data_restore`, `data_migrate_bump_version`
- Config: `config_set`, `config_get`, `config_backup`, `config_restore`

Refer to `src/lib.rs` for detailed types and events.

