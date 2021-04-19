---
description: Es gibt drei Hauptfunktionen für den Stations Status, für die Steuerungs Nachrichten gewartet werden müssen und die weitergeleitet werden und die nicht gestört werden müssen.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Stations Status-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f6ddd1b1ce6df1ad2f3dc61e891ed6952a7f05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360527"
---
# <a name="station-status-control"></a>Stations Status-Steuerelement

Es gibt drei Hauptfunktionen für den Stations Status, die Steuern müssen: Nachrichten Wartezeiten, weiterleiten und nicht stören. Weiterleitungs-und nicht störende Funktionen sind über die vorhandene [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion (die Adress spezifisch ist) steuerbar und können mithilfe von [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)abgefragt werden. Das msgwait-Bit linedevstatusflags \_ im **dwdevstatusflags** -Member von [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) gibt den Status der Nachrichten Warteschlange auf dem Gerät an, und eine linedevstate-msgwaideff- \_ \_ Nachricht wird gesendet, um anzugeben, wann sich der Status ändert. Mit der [**linesetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) -Funktion kann die Warteschlange für Nachrichten gesteuert werden, ohne dass hierfür ein TAPI-Telefongerät implementiert werden muss. Das linefeature \_ setdevstatus-Bit (im **dwlinefeatures** -Member von [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) und **linedevstatus**) gibt an, wann es aufgerufen werden kann, und der **dwsettabledevstatus** -Member von **linedevcaps** ermöglicht der Anwendung, zu erkennen, welche Gerätestatus Einstellungen von der Anwendung gesteuert werden können. Zusätzlich dazu, dass die Funktion "Nachrichten Warteschlange" gesteuert werden kann, kann auch der Status "verbunden", "INService" und "gesperrt" des Geräts so festgelegt werden, dass diese vom Switch oder anderer Hardware unterstützt werden. Aufrufe dieser Funktion führen dazu, dass [**entsprechende \_ linienlinedevstate**](line-linedevstate.md) -Meldungen gesendet werden, um den neuen Status widerzuspiegeln.

 

 



