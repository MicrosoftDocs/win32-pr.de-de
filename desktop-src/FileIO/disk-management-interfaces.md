---
description: Schnittstellen, die in der Datenträgerverwaltung verwendet werden.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Datenträgerverwaltungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7314de976b1a5228a8b537da5d09be3df66936ed57915d86d78b0a84c4361e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823210"
---
# <a name="disk-management-interfaces"></a>Datenträgerverwaltungsschnittstellen

Die folgenden Schnittstellen werden in der Datenträgerverwaltung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                     | BESCHREIBUNG                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Steuert die Datenträgerkontingente eines einzelnen NTFS-Dateisystem-Volumes.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Empfängt kontingentbezogene Ereignisbenachrichtigungen.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Stellt einen einzelnen Benutzerkontingenteintrag in der Volumekontingent-Informationsdatei dar.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Fügt einem Container mehrere Kontingentbenutzerobjekte hinzu, die dann in einem einzigen Aufruf zur Aktualisierung übermittelt werden.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Enumeriert Benutzerkontingenteinträge auf dem Volume.<br/>                                                        |



 

 

