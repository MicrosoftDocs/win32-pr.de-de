---
title: Gründe für Nichterreichbarkeit
description: In der folgenden Tabelle sind konstante Werte aufgeführt, die angeben, warum eine Schnittstelle nicht erreichbar ist.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb833409d9d2ba31adedbc2942d39399c0a5763ad4d65dc7cdcaf234f97efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025410"
---
# <a name="unreachability-reasons"></a>Gründe für Nichterreichbarkeit

In der folgenden Tabelle sind konstante Werte aufgeführt, die angeben, warum eine Schnittstelle nicht erreichbar ist.



| Wert                                       | Bedeutung                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| \_MPR-SCHNITTSTELLENADMINISTRATOR \_ \_ DEAKTIVIERT             | Der Administrator hat die Schnittstelle deaktiviert.                                                  |
| VERBINDUNGSFEHLER BEI \_ \_ MPR-SCHNITTSTELLE \_         | Fehler beim vorherigen Verbindungsversuch. Sehen Sie sich den **DwLastError-Member** nach dem Fehlercode an. |
| MPR \_ INTERFACE \_ DIALOUT \_ HOURS \_ RESTRICTION | Einwählen ist zum aktuellen Zeitpunkt nicht zulässig.                                                   |
| \_MPR-SCHNITTSTELLE \_ FÜR \_ RESSOURCEN \_          | Es sind keine Ports oder Geräte zur Verwendung verfügbar.                                                     |
| \_MPR-SCHNITTSTELLENDIENST \_ \_ ANGEHALTEN             | Der Dienst wurde angehalten.                                                                         |
| \_MPR-SCHNITTSTELLE \_ KEIN MEDIA \_ \_ SENSE            | Das Netzwerkkabel ist von der Netzwerkkarte getrennt.                                       |
| \_MPR-SCHNITTSTELLE \_ KEIN \_ GERÄT                  | Die Netzwerkkarte wurde vom Computer entfernt.                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_MPR-SCHNITTSTELLE \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**\_MPR-SCHNITTSTELLE \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**MIB \_ IFROW**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**MIB \_ IFSTATUS**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 