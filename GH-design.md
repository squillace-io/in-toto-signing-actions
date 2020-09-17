# Verifiable Software Supply Chains using Github Actions, Registry, Marketplace, and CNAB bundles

Right now the open-source developer nexus for the entire world is Github. Though there will soon be tribal competitors like Gitlab and foreign competitors like Gitee in China gain strenth, for the forseeable two years Github not only can deliver for every developer, all over the world, but can expand the abilities that everyone has for personal or professional development. This proposal is one example.

Github, along with CNCF projects https://in-toto.io/ and https://theupdateframework.io/ and the Linux Foundation specification for Cloud Native Application Bundles (https://cnab.io), can build an experience for every developer using GH actions that enables to demonstrate that **only** approved contributors have merged code to a repository by giving anyone with the public metadata to the repository a GH service that can verify this fact using signed commits and an in-toto metadata service enabled by GH actions.

In addition, repositories need _distribution_ not merely _deployment_. To distribute -- and perhaps even sell -- solutions, developers and ISVs need a packaging that supports these very same open source protocols. If a CNAB bundle is built from the repository using the https://github.com/deislabs/porter-gh-action Github Action, that bundle can be pushed to the Github Registry -- a bundle is an OCI image of type "cnab" -- and then also offered free on either the Github Marketplace, or sold, using the already available Github Sponsors account as the payment engine.

No one can give these very advanced enterprise confidence features to the world except Github. The techologies exist right now; let's build the backing system to make use of them. 



## The experience

1. The signed commits experience needs to be evangelized and streamlined. It should be easy to set up from any OS and repos should ASK on creation to enable it.
2. Repos with signed commits enabled should suggest that ONLY signed commits be permitted.
3. Repos with signed commits have a tab for in-toto metadata to add permitted contributor identities.
4. Repos that permit only signed commits automatically create an in-toto metadata link chain from the commits and identities.
5. Each sucessful GH action pipeline results in verified in-toto metadata about the committer chain.
6. Each successful verification results in a CNAB bundle using the Porter GH action that is signed with the same in-toto metadata.
7. Each signed bundle can be pushed to the Github Registry, which can display a confirmed Badge and public verification endpoint URL.
8. Each signed bundle pushed to the Github registry can be promoted to the Marketplace (depending on configurations).
9. Each signed bundle promoted to the marketplace can have direct-to-cloud or direct-to-local launch urls that pass through a billing page (if not purely OSS) that can instantly enable payments to the repo's Github Sponsor account.

## Enabling features and technologies



## What's missing

1. GH in-toto actions (NYU and other upstream entities would love to help out here)
2. Robust bundle publish testing with GH registry
3. A notary or other in-toto instance must be available behind GH actions (happy to foot PoC resources here)
4. Front end work for badges and launch url generation
5. Front and backend work for marketplace wireup to sponsors; legal entanglements.
6. ????

## Who's involved 
Direct:
- azooinmyluggage (GH)
- squillace (Microsoft)
- Brian Clark (GH)
- GH Marketplace??
- GH Sponsors??
- GH Repos
- GH Packages
- GH Container registry
- GH Dev Evangelism
- MSFT Cloud Dev Advocates


Community Collaborators
in-toto:
- Santiago Torres Arias (NYU)
- DataDog: Trishank Karthik Kuppusamy (DataDog)
