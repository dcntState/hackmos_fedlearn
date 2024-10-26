# Deploy contract

```just localnet deploy-contract ./../hackmos_fedlearn/contracts/artifacts/fedlearn.wasm```

# Execute contract

```wardend tx wasm execute 'warden14hj2tavq8fpesdwxxcu44rty3hh90vhujrvcmstl4zr3txmfvw9srt30us' '{"create_akash_instance":{"input": "Akash1;akash2"}}' --from shulgin -y | wardend q wait-tx```


# Read result

```wardend q wasm contract-state smart 'warden14hj2tavq8fpesdwxxcu44rty3hh90vhujrvcmstl4zr3txmfvw9srt30us' '{"get_future_result": {"id": 0}}'```