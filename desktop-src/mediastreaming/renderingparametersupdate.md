---
title: Renderingparametersupdate-Ereignis
description: Tritt auf, wenn ein beliebiger Satz von renderingsteuerungsparametern auf der DMR aktualisiert wird.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- Renderingparametersupdate-Ereignis Medien Streaming-API
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314847"
---
# <a name="renderingparametersupdate-event"></a><span data-ttu-id="c0115-104">Renderingparametersupdate-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c0115-104">RenderingParametersUpdate event</span></span>

<span data-ttu-id="c0115-105">Tritt auf, wenn ein beliebiger Satz von renderingsteuerungsparametern auf der DMR aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c0115-105">Occurs whenever any of a set of rendering control parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0115-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0115-106">Syntax</span></span>


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="c0115-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0115-107">Parameters</span></span>

<span data-ttu-id="c0115-108">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="c0115-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0115-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0115-109">Return value</span></span>

<span data-ttu-id="c0115-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c0115-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0115-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0115-111">Remarks</span></span>

<span data-ttu-id="c0115-112">Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie mithilfe der [**Add \_ renderingparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) -Methode eine [**renderingparametersupdatehandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c0115-112">To handle notifications from this event, register a [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) event handler function using the [**add\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) method.</span></span> <span data-ttu-id="c0115-113">Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die Methode [**Remove \_ renderingparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="c0115-113">To unregister the event handler, use the [**remove\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) method.</span></span>

 

 