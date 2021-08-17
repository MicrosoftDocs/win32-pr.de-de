---
description: Es gibt drei wichtige Stationsstatusfunktionen, die die Steuerung von Nachrichtenwartelichtern, Weiterleitung und Nicht störend erfordern.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Stationsstatus-Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e136450dbda8cec260a460f49ce8d45b65d1b58ec588ccbcc435c5e3a2b1cd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861933"
---
# <a name="station-status-control"></a>Stationsstatus-Steuerung

Es gibt drei wichtige Stationsstatusfunktionen, die gesteuert werden müssen: Nachrichtenwartelichter, Weiterleitung und Nicht störend. Weiterleitung und Nicht stören können über die vorhandene [**lineForward-Funktion**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (die adressspezifisch ist) gesteuert und mithilfe von [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)abgefragt werden. Das MSGWAIT-Bit LINEDEVSTATUSFLAGS \_ im **Member dwDevStatusFlags** von [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) gibt den Status der Nachricht an, die auf das Gerät wartet, und eine LINEDEVSTATE \_ MSGWAITON- oder LINEDEVSTATE \_ MSGWAITOFF-Nachricht wird gesendet, um anzugeben, wann sich der Zustand ändert. Die [**lineSetLineDevStatus-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) ermöglicht die Steuerung des Wartelichts für Nachrichten, ohne dass ein TAPI-Telefongerät nur für diesen Zweck implementiert werden muss. Das \_ LINEFEATURE SETDEVSTATUS-Bit (im **dwLineFeatures-Member** von [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) und **LINEDEVSTATUS**) gibt an, wann es aufgerufen werden kann, und mit dem **dwSettableDevStatus-Member** von **LINEDEVCAPS** kann die Anwendung erkennen, welche Gerätestatuseinstellungen von der Anwendung gesteuert werden können. Neben der Steuerung der Funktion "Warten auf Nachrichten" kann auch der Status Verbunden, Inservice und Gesperrt des Geräts festgelegt werden, sofern diese vom Switch oder von anderer Hardware unterstützt werden. Aufrufe dieser Funktion führen dazu, dass entsprechende [**LINE \_ LINEDEVSTATE-Meldungen**](line-linedevstate.md) gesendet werden, um den neuen Status widerzuspiegeln.

 

 



