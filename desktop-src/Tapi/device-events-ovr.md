---
description: TAPI antwortet auf Geräteänderungen, wie z. b. ein Telefon, das mit dem Klingeln begonnen hat, oder ein Modem, das durch Auslösen von Geräte Ereignissen entfernt wurde.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Geräte Ereignisse (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751625"
---
# <a name="device-events-telephony-api"></a>Geräte Ereignisse (telefonieapi)

TAPI antwortet auf Geräteänderungen, wie z. b. ein Telefon, das mit dem Klingeln begonnen hat, oder ein Modem, das durch Auslösen von Geräte Ereignissen entfernt wurde. Eine TAPI-Anwendung sollte auf ein Geräte Ereignis reagieren, indem Sie die aufgetretene Änderung abfragt und dann entsprechende Maßnahmen ergreifen. Eine Anwendung kann für Ereignisse, die mithilfe der [Ereignis Benachrichtigung](event-notification.md)empfangen werden, angezeigt werden.

**TAPI 2. x:** Anwendungen erhalten mithilfe der [**Zeile \_ linedevstate**](./line-linedevstate.md) eine Benachrichtigung über Geräte Ereignisse. Der aktuelle Status einer Adresse wird durch den Aufruf von [**linegetaddressstatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)bestimmt, der die Informationen in einer [**lineaddressstatus**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) -Struktur zurückgibt. Der Status eines angegebenen Open-Line-Geräts wird durch den Aufruf von [**linegetlinedevstatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)abgerufen, der seine Informationen in einer [**linedevstatus**](/windows/win32/api/tapi/ns-tapi-linedevstatus) -Struktur zurückgibt.

**TAPI 3. x:** Anwendungen erhalten eine [**Adress \_ Ereignis**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) Benachrichtigung, die mithilfe der [**itadressssevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) -Schnittstelle verarbeitet wird. Die [**itaddress-Funktionen**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) können dann verwendet werden, um ausführlichere Informationen zu erhalten.

 

 
