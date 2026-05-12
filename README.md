# sap-btp-end-to-end-travel-request-app
sap-btp-end-to-end-travel-request-app/
│
├── README.md
├── .gitignore
│
├── backend/                     # CAP project
│   ├── app/
│   ├── db/
│   ├── srv/
│   ├── package.json
│   ├── cds.json
│   └── xs-security.json
│
├── frontend/                    # SAP Build Apps exported project
│   ├── assets/
│   ├── pages/
│   ├── logic/
│   └── README.md
│
├── config/                      # BTP configuration artifacts
│   ├── destinations/
│   │   ├── dev-destination.json
│   │   ├── test-destination.json
│   │   └── prod-destination.json
│   ├── role-collections/
│   ├── xsuaa/
│   └── cf-manifests/
│
├── docs/                        # Documentation
│   ├── architecture.md
│   ├── day-wise-progress.md
│   ├── deployment-guide.md
│   ├── hana-schema.md
│   └── ui-design.md
│
├── diagrams/                    # Architecture diagrams
│   ├── system-architecture.drawio
│   ├── landscape.drawio
│   └── data-model.drawio
│
└── tests/                       # Optional test automation
    ├── api-tests/
    └── ui-tests/
