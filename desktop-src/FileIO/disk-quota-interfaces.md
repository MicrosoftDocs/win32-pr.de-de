---
description: Schnittstellen, die mit Datenträgerkontingenten verwendet werden.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Datenträgerkontingentschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d7406425ccce59db6f5b2fd7eae0e33473215c0fda1e8ecd497169ad188c25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997868"
---
# <a name="disk-quota-interfaces"></a>Datenträgerkontingentschnittstellen

Die folgenden Schnittstellen werden mit Datenträgerkontingenten verwendet.



| Schnittstelle                                          | Beschreibung                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | Steuert die Datenträgerkontingente eines einzelnen NTFS-Dateisystemvolumes.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | Empfängt kontingentbezogene Ereignisbenachrichtigungen.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | Stellt einen einzelnen Benutzerkontingenteintrag in der Volumekontingentinformationsdatei dar.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | Fügt einem Container mehrere Kontingentbenutzerobjekte hinzu, die dann in einem einzigen Aufruf zur Aktualisierung übermittelt werden.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | Listet Benutzerkontingenteinträge auf dem Volume auf.<br/>                                                        |



 

 

