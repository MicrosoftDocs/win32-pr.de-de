---
description: Die von VDS unterstützten Datentypen definieren Funktions Rückgabewerte, Funktionsparameter und Strukturmember. Datentypen definieren die Größe und Bedeutung dieser Elemente.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: VDS-Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359539"
---
# <a name="vds-data-types"></a>VDS-Datentypen

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Die von VDS unterstützten Datentypen definieren Funktions Rückgabewerte, Funktionsparameter und Strukturmember. Datentypen definieren die Größe und Bedeutung dieser Elemente.



| Datentyp                                                                                      | BESCHREIBUNG                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS- \_ Objekt- \_ ID**<br/> | VDS-Objekt-ID. Diese Werte sind in Neustarts nicht garantiert eindeutig. <br/> Dieser Typ wird in "VDS. h" (vdshwprv. h für Hardware Anbieter) als GUID deklariert. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS- \_ Pfad- \_ ID**<br/>       | VDS-Pfad-ID für Multipfad-e/a (MPIO). <br/> Dieser Typ wird in "VDS. h" (vdshwprv. h für Hardware Anbieter) als UINT64 deklariert.<br/>                                      |



 

 

