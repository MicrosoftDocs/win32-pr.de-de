---
title: Getmuteoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von getmuteasync gestartet wurde.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, getmuteoperation-Schnittstelle
- Getmuteoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101514"
---
# <a name="getmuteoperationgetresults-method"></a><span data-ttu-id="cd521-106">Getmuteoperation. GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="cd521-106">GetMuteOperation.GetResults method</span></span>

<span data-ttu-id="cd521-107">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getmuteasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="cd521-107">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd521-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd521-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="cd521-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd521-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd521-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cd521-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cd521-111">Der stumm Wert.</span><span class="sxs-lookup"><span data-stu-id="cd521-111">The mute value.</span></span> <span data-ttu-id="cd521-112">Der Wert true gibt an, dass Audiodaten zurzeit stumm geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="cd521-112">A value of true indicates that audio is currently muted.</span></span> <span data-ttu-id="cd521-113">Der Wert false gibt an, dass Audiodaten nicht stumm geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="cd521-113">A value of false indicates that audio is not muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd521-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd521-114">Return value</span></span>

<span data-ttu-id="cd521-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="cd521-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cd521-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd521-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cd521-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cd521-117">Return code</span></span>                                                                          | <span data-ttu-id="cd521-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd521-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cd521-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd521-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cd521-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd521-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd521-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd521-121">Remarks</span></span>

<span data-ttu-id="cd521-122">Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](getmuteoperation-completed.md) Eigenschaft registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd521-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getmuteoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd521-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd521-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd521-124">**Getmuteoperation**</span><span class="sxs-lookup"><span data-stu-id="cd521-124">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

