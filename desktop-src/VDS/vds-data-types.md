---
description: Die von VDS unterstützten Datentypen definieren Funktionsrückgabewerte, Funktionsparameter und Strukturmember. Datentypen definieren die Größe und Bedeutung dieser Elemente.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: VDS-Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83a0f3586cb73b823feb6b41990d1f305056a23f9ac0e47ef8fbfc1e4853267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007930"
---
# <a name="vds-data-types"></a>VDS-Datentypen

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Die von VDS unterstützten Datentypen definieren Funktionsrückgabewerte, Funktionsparameter und Strukturmember. Datentypen definieren die Größe und Bedeutung dieser Elemente.



| Datentyp                                                                                      | BESCHREIBUNG                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ \_ VDS-OBJEKT-ID**<br/> | VDS-Objekt-ID. Es ist nicht garantiert, dass diese Werte bei Neustarts eindeutig sind. <br/> Dieser Typ wird in Vds.h (VdsHwPrv.h für Hardwareanbieter) als GUID deklariert. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS \_ PATH ID (VDS-PFAD-ID) \_**<br/>       | VDS-Pfad-ID für Multipfad-E/A (MPIO). <br/> Dieser Typ wird in Vds.h (VdsHwPrv.h für Hardwareanbieter) als UINT64 deklariert.<br/>                                      |



 

 

