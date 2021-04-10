---
title: Transportparametersupdate-Ereignis
description: Tritt auf, wenn eine beliebige Anzahl von Transport Parametern auf der DMR aktualisiert wird.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- Transportparametersupdate-Ereignis Medien-Streaming-API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858232"
---
# <a name="transportparametersupdate-event"></a><span data-ttu-id="b7c7a-104">Transportparametersupdate-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b7c7a-104">TransportParametersUpdate event</span></span>

<span data-ttu-id="b7c7a-105">Tritt auf, wenn eine beliebige Anzahl von Transport Parametern auf der DMR aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b7c7a-105">Occurs whenever any of a set of transport parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c7a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c7a-106">Syntax</span></span>


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="b7c7a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c7a-107">Parameters</span></span>

<span data-ttu-id="b7c7a-108">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="b7c7a-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7c7a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7c7a-109">Return value</span></span>

<span data-ttu-id="b7c7a-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b7c7a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7c7a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7c7a-111">Remarks</span></span>

<span data-ttu-id="b7c7a-112">Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**transportparametersupdatehandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) mithilfe der Methode [**Add \_ transportparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="b7c7a-112">To handle notifications from this event, register a [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) event handler function using the [**add\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) method.</span></span> <span data-ttu-id="b7c7a-113">Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die Methode [**Remove \_ transportparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="b7c7a-113">To unregister the event handler, use the [**remove\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) method.</span></span>

 

 