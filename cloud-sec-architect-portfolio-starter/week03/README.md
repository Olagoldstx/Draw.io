
```mermaid
flowchart LR
  %% Shared Responsibility Model: Provider vs Customer across AWS, Azure, GCP

  subgraph AWS[Amazon Web Services]
    AProv[Provider\n- Physical DCs &amp; Facilities\n- Network &amp; Hypervisor\n- Managed Service Platform]:::prov
    ACust[Customer\n- Data &amp; Identity (IAM)\n- OS/Apps/Configs (IaaS)\n- Access Controls &amp; Keys\n- Compliance-in-Cloud]:::cust
  end

  subgraph AZ[Microsoft Azure]
    ZProv[Provider\n- Physical DCs &amp; Facilities\n- Network &amp; Hypervisor\n- PaaS/SaaS Runtime]:::prov
    ZCust[Customer\n- Data &amp; Identity (Entra ID)\n- Workloads/Configs (IaaS)\n- RBAC/Policies/Keys\n- Compliance-in-Cloud]:::cust
  end

  subgraph GCP[Google Cloud Platform]
    GProv[Provider\n- Physical DCs &amp; Facilities\n- Network &amp; Hypervisor\n- Global Control Plane]:::prov
    GCust[Customer\n- Data &amp; Identity (IAM)\n- Workloads/Configs (IaaS)\n- Org Policies/Keys\n- Compliance-in-Cloud]:::cust
  end

  classDef prov fill:#eef7ff,stroke:#1f6feb,stroke-width:1.5px,color:#0b3563
  classDef cust fill:#f5fff0,stroke:#1a7f37,stroke-width:1.5px,color:#0b3b19

  %% Legend (instead of note over, since not supported in flowchart)
  subgraph Legend[Legend]
    L1[SaaS → Provider handles app/runtime; you own data + access]
    L2[PaaS → Shared at runtime/config; you own data + access]
    L3[IaaS → You manage OS/apps/configs; provider = physical/infra]
  end
```



