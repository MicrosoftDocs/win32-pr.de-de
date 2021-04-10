---
title: Connectionstatuschangi-Ereignis
description: Tritt auf, wenn sich der Netzwerk Verbindungsstatus des Geräts ändert.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- Connectionstatuschge-Ereignis Medien-Streaming-API
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726761"
---
# <a name="connectionstatuschanged-event"></a><span data-ttu-id="6bd07-104">Connectionstatuschangi-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6bd07-104">ConnectionStatusChanged event</span></span>

<span data-ttu-id="6bd07-105">Tritt auf, wenn sich der Netzwerk Verbindungsstatus des Geräts ändert.</span><span class="sxs-lookup"><span data-stu-id="6bd07-105">Occurs when the device’s network connection status changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd07-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bd07-106">Syntax</span></span>


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a><span data-ttu-id="6bd07-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bd07-107">Parameters</span></span>

<span data-ttu-id="6bd07-108">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="6bd07-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bd07-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bd07-109">Return value</span></span>

<span data-ttu-id="6bd07-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6bd07-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bd07-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bd07-111">Remarks</span></span>

<span data-ttu-id="6bd07-112">Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**connectionstatushandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) mithilfe der [**Add \_ connectionstatuschangi-Methode**](ibasicdevice-add-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="6bd07-112">To handle notifications from this event, register a [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function using the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method.</span></span> <span data-ttu-id="6bd07-113">Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die Methode [**Remove \_ connectionstatuschangi.**](ibasicdevice-remove-connectionstatuschanged.md)</span><span class="sxs-lookup"><span data-stu-id="6bd07-113">To unregister the event handler, use the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

 

 