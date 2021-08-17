---
description: TAPI reagiert auf Geräteänderungen, z. B. ein Telefon, das mit dem Läuten begonnen hat, oder ein Modem, das entfernt wurde, indem Geräteereignisse ausgerufen werden.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Geräteereignisse (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59252bddee9697ac453e8e6883c8724e4bc2b22a8a6fb245855bd493821808b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867415"
---
# <a name="device-events-telephony-api"></a>Geräteereignisse (Telefonie-API)

TAPI reagiert auf Geräteänderungen, z. B. ein Telefon, das mit dem Läuten begonnen hat, oder ein Modem, das entfernt wurde, indem Geräteereignisse ausgerufen werden. Eine TAPI-Anwendung sollte auf ein Geräteereignis reagieren, indem sie die spezifische Änderung abfragt, die aufgetreten ist, und dann entsprechende Maßnahmen ergreifen. Eine Anwendung kann mithilfe der Ereignisbenachrichtigung auf Ereignisse anzeigen, die [sie erhält.](event-notification.md)

**TAPI 2.x:** Anwendungen erhalten Benachrichtigungen über Geräteereignisse mithilfe der [**\_ LINEDEVSTATE-Nachricht.**](./line-linedevstate.md) Der aktuelle Status einer Adresse wird durch Aufrufen von [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)bestimmt, der seine Informationen in einer [**LINEADDRESSSTATUS-Struktur**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) zurückgibt. Der Status eines angegebenen Open Line-Geräts wird durch Aufrufen von [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)ermittelt, das seine Informationen in einer [**LINEDEVSTATUS-Struktur**](/windows/win32/api/tapi/ns-tapi-linedevstatus) zurückgibt.

**TAPI 3.x:** Anwendungen erhalten eine [**ADDRESS \_ EVENT-Benachrichtigung,**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) die mithilfe der [**ITAddressEvent-Schnittstelle verarbeitet**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) wird. [**ItAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) kann dann verwendet werden, um weitere Detailinformationen zu erhalten.

 

 
