\# Addressing Plan



\## VLANs and subnets



| Site | VLAN | Name | Subnet | Gateway (SVI) |

|---|---|---|---|---|

| HQ | 10 | CORP | 10.1.10.0/24 | 10.1.10.1 |

| HQ | 20 | SERVERS | 10.1.20.0/24 | 10.1.20.1 |

| HQ | 30 | GUEST | 10.1.30.0/24 | 10.1.30.1 |

| HQ | 99 | MGMT | 10.1.99.0/24 | 10.1.99.1 |

| Branch | 10 | CORP | 10.2.10.0/24 | 10.2.10.1 |

| Branch | 30 | GUEST | 10.2.30.0/24 | 10.2.30.1 |

| Branch | 99 | MGMT | 10.2.99.0/24 | 10.2.99.1 |



\## Transit links



| Link | Subnet | Endpoints |

|---|---|---|

| MLS-A to R1 | 10.0.0.0/30 | MLS-A .1, R1 .2 |

| R1 to R2 (WAN) | 10.0.0.4/30 | R1 .5, R2 .6 |

| R2 to MLS-B | 10.0.0.8/30 | R2 .9, MLS-B .10 |



\## OSPF areas



\- Area 1: HQ

\- Area 0: WAN backbone

\- Area 2: Branch

