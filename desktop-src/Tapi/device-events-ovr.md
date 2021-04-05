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
# <a name="device-events-telephony-api"></a><span data-ttu-id="68fd0-103">Geräte Ereignisse (telefonieapi)</span><span class="sxs-lookup"><span data-stu-id="68fd0-103">Device Events (Telephony API)</span></span>

<span data-ttu-id="68fd0-104">TAPI antwortet auf Geräteänderungen, wie z. b. ein Telefon, das mit dem Klingeln begonnen hat, oder ein Modem, das durch Auslösen von Geräte Ereignissen entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="68fd0-104">TAPI responds to device changes such as a phone that has started ringing or a modem that has been removed by firing device events.</span></span> <span data-ttu-id="68fd0-105">Eine TAPI-Anwendung sollte auf ein Geräte Ereignis reagieren, indem Sie die aufgetretene Änderung abfragt und dann entsprechende Maßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="68fd0-105">A TAPI application should respond to a device event by querying for the specific change that has occurred and then taking appropriate action.</span></span> <span data-ttu-id="68fd0-106">Eine Anwendung kann für Ereignisse, die mithilfe der [Ereignis Benachrichtigung](event-notification.md)empfangen werden, angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="68fd0-106">An application may screen for events it will receive using [event notification](event-notification.md).</span></span>

<span data-ttu-id="68fd0-107">**TAPI 2. x:** Anwendungen erhalten mithilfe der [**Zeile \_ linedevstate**](./line-linedevstate.md) eine Benachrichtigung über Geräte Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="68fd0-107">**TAPI 2.x:** Applications receive notification of device events using the [**LINE\_LINEDEVSTATE**](./line-linedevstate.md) message.</span></span> <span data-ttu-id="68fd0-108">Der aktuelle Status einer Adresse wird durch den Aufruf von [**linegetaddressstatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)bestimmt, der die Informationen in einer [**lineaddressstatus**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) -Struktur zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="68fd0-108">The current status of an address is determined by calling [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), which returns its information in a [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="68fd0-109">Der Status eines angegebenen Open-Line-Geräts wird durch den Aufruf von [**linegetlinedevstatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)abgerufen, der seine Informationen in einer [**linedevstatus**](/windows/win32/api/tapi/ns-tapi-linedevstatus) -Struktur zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="68fd0-109">The status of a specified open line device is obtained by calling [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), which returns its information in a [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure.</span></span>

<span data-ttu-id="68fd0-110">**TAPI 3. x:** Anwendungen erhalten eine [**Adress \_ Ereignis**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) Benachrichtigung, die mithilfe der [**itadressssevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) -Schnittstelle verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="68fd0-110">**TAPI 3.x:** Applications receive an [**ADDRESS\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) notification, which is processed using the [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) interface.</span></span> <span data-ttu-id="68fd0-111">Die [**itaddress-Funktionen**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) können dann verwendet werden, um ausführlichere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="68fd0-111">The [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) can then be used to acquire more detail information.</span></span>

 

 
