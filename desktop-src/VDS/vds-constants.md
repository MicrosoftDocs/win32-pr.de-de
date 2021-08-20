---
description: VDS-Konstanten
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: VDS-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9fa0c6196e1085de3a5433750b890e2ad3bc42f4a86022587f02157521eacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125693"
---
# <a name="vds-constants"></a>VDS-Konstanten

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

VDS-Konstanten werden wie folgt kategorisiert:

-   [Objektstatuskonst constants](#object-status-constants)
-   [Automagic Hints-Konstanten](#automagic-hints-constants)
-   [Verschiedene Konstanten](#miscellaneous-constants)

### <a name="object-status-constants"></a>Objektstatuskonst constants



| Konstante           | Wert |
|--------------------|-------|
| STATUS \_ UNKNOWN    | 0     |
| STATUS \_ ONLINE     | 1     |
| STATUS \_ NICHT \_ BEREIT | 2     |
| STATUS \_ KEINE \_ MEDIEN  | 3     |
| STATUS \_ OFFLINE    | 4     |
| STATUS \_ FAILED     | 5     |
| STATUS \_ FEHLT    | 6     |



 

### <a name="automagic-hints-constants"></a>Automagic Hints-Konstanten



| Konstante                               | Wert   |
|----------------------------------------|---------|
| \_VDS-HINWEIS \_ GRÖßTENTEILSREADS                 | 0x0002L |
| VDS \_ HINT \_ OPTIMIZEFORSEQUENTIALREADS  | 0x0004L |
| VDS \_ HINT \_ OPTIMIZEFORSEQUENTIALWRITES | 0x0008L |
| VDS \_ HINT \_ REMAPENABLED                | 0x0020L |
| SCHREIBZUGRIFF AUF \_ \_ VDS-HINWEISTHROUGHCACHINGENABLED  | 0x0040L |
| VDS \_ HINT \_ HARDWARECHECKSUMENABLED     | 0x0080L |
| \_VDS-HINWEIS \_ ISYANKABLE                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Verschiedene Konstanten



| Konstante                     | Wert      |
|------------------------------|------------|
| VDS \_ REBUILD \_ PRIORITY \_ MIN  | 0x0001L    |
| VER \_ \_ VDS-LUN-INFORMATIONEN \_   | 1          |
| MAXIMALE \_ \_ COMPUTERNAME-LÄNGE    | 15         |
| MAX \_ PROVIDERNAME \_ LENGTH    | 200        |
| MAX \_ VERSIONSTRING \_ LENGTH   | 16         |
| LAUFWERKBUCHSTABEN \_ \_ PROP          | Nicht zutreffend        |
| MAX. \_ \_ FS-NAMENSGRÖßE \_          | 8          |
| UNGÜLTIGE \_ \_ MEMBER-IDX         | 0xFFFFFFFF |
| LÄNGE DES \_ \_ GPT-PARTITIONSNAMENS \_ | 36         |
| MAX \_ PATH                    | 260        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Referenz](vds-reference.md)
</dt> </dl>

 

 
