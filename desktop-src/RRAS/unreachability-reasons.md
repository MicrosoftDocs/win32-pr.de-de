---
title: Gründe für die Nichterreichbarkeit
description: In der folgenden Tabelle werden Konstante Werte aufgelistet, die angeben, warum eine Schnittstelle nicht erreichbar ist.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039340"
---
# <a name="unreachability-reasons"></a>Gründe für die Nichterreichbarkeit

In der folgenden Tabelle werden Konstante Werte aufgelistet, die angeben, warum eine Schnittstelle nicht erreichbar ist.



| Wert                                       | Bedeutung                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| MPR- \_ Schnittstellen \_ Administrator \_ deaktiviert             | Der Administrator hat die Schnittstelle deaktiviert.                                                  |
| MPR- \_ Schnittstellen \_ Verbindungs \_ Fehler         | Der vorherige Verbindungsversuch ist fehlgeschlagen. Überprüfen Sie den **dwlasterror** -Member auf den Fehlercode. |
| Einschränkung der MPR- \_ Schnittstellen-ddstunden \_ \_ \_ | Das auswählgerät ist zum aktuellen Zeitpunkt nicht zulässig.                                                   |
| MPR- \_ Schnittstelle \_ aus \_ \_ Ressourcen          | Es sind keine Ports oder Geräte zur Verwendung verfügbar.                                                     |
| MPR- \_ Schnittstellen \_ Dienst \_ angehalten             | Der Dienst wurde angehalten.                                                                         |
| MPR- \_ Schnittstelle \_ ohne \_ Medien \_ Sinn            | Das Netzwerkkabel ist von der Netzwerkkarte getrennt.                                       |
| MPR- \_ Schnittstelle \_ ohne \_ Gerät                  | Die Netzwerkkarte wurde vom Computer entfernt.                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MPR- \_ Schnittstelle \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**MPR- \_ Schnittstelle \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**MIB \_ ifrow**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**MIB \_ if-Status**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 