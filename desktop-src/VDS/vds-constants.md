---
description: VDS-Konstanten
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: VDS-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363748"
---
# <a name="vds-constants"></a>VDS-Konstanten

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS-Konstanten werden wie folgt kategorisiert:

-   [Objekt Status Konstanten](#object-status-constants)
-   [Automatisierungs Hinweise-Konstanten](#automagic-hints-constants)
-   [Sonstige Konstanten](#miscellaneous-constants)

### <a name="object-status-constants"></a>Objekt Status Konstanten



| Konstante           | Wert |
|--------------------|-------|
| \_Unbekannter Status    | 0     |
| Status \_ Online     | 1     |
| Status \_ nicht \_ bereit | 2     |
| Status " \_ kein \_ Medium"  | 3     |
| Status \_ Offline    | 4     |
| Status \_ Fehler     | 5     |
| Status \_ fehlt    | 6     |



 

### <a name="automagic-hints-constants"></a>Automatisierungs Hinweise-Konstanten



| Konstante                               | Wert   |
|----------------------------------------|---------|
| VDS- \_ Hinweis " \_ mustlyreads"                 | 0x0002l |
| VDS- \_ Hinweis \_ optimizeforsequentialreads  | 0x0004l |
| VDS- \_ Hinweis \_ optimizeforsequentialschreib Vorgänge | 0x0008l |
| VDS-Hinweis neu zuordnen \_ \_                | 0x0020l |
| VDS- \_ Hinweis " \_ Write-Through cachingenabled"  | 0x0040l |
| VDS- \_ Hinweis \_ hardwarechecksumenabled     | 0x0080l |
| VDS- \_ Hinweis ist \_ isyankable                  | 0x0100l |



 

### <a name="miscellaneous-constants"></a>Sonstige Konstanten



| Konstante                     | Wert      |
|------------------------------|------------|
| VDS-Neuerstellung \_ \_ Priorität \_ Min.  | 0x0001l    |
| \_VDS- \_ LUN- \_ Informationen   | 1          |
| maximale \_ Länge des Computer namens \_    | 15         |
| maximale \_ Länge von ProviderName \_    | 200        |
| maximale \_ Länge der Versions Zeichenfolge \_   | 16         |
| Laufwerk \_ Buchstaben- \_ Prop          | –        |
| maximale \_ Größe des FS- \_ namens \_          | 8          |
| Ungültiger \_ IDX-Member. \_         | 0xFFFFFFFF |
| Länge des GPT- \_ Partitions \_ namens \_ | 36         |
| Maximaler \_ Pfad                    | 260        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Referenz](vds-reference.md)
</dt> </dl>

 

 
