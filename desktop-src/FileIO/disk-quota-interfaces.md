---
description: Mit Datenträger Kontingenten verwendete Schnittstellen.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Schnittstellen für Festplattenkontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485622"
---
# <a name="disk-quota-interfaces"></a>Schnittstellen für Festplattenkontingente

Die folgenden Schnittstellen werden mit Datenträger Kontingenten verwendet.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Idiskquotacontrol**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | Steuert die Festplattenkontingent-Einrichtungen eines einzelnen NTFS-Dateisystem Volumes.<br/>                             |
| [**Idiskquotaevents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | Empfängt Kontingent bezogene Ereignis Benachrichtigungen.<br/>                                                         |
| [**Idiskquotauser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | Stellt einen einzelnen Benutzer Kontingent Eintrag in der Volumekontingent-Informationsdatei dar.<br/>                          |
| [**Idiskquotauserbatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | Fügt einem Container, der in einem einzelnen-Befehl zur Aktualisierung übermittelt wird, mehrere Kontingent Benutzer Objekte hinzu.<br/> |
| [**Ienumdiskquotauszer**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | Listet Benutzer Kontingent Einträge auf dem Volume auf.<br/>                                                        |



 

 

