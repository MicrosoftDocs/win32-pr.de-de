---
title: Getvolumeoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von getvolumeasync gestartet wurde.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, getvolumeoperation-Schnittstelle
- Getvolumeoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339065"
---
# <a name="getvolumeoperationgetresults-method"></a><span data-ttu-id="80c5f-106">Getvolumeoperation. GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="80c5f-106">GetVolumeOperation.GetResults method</span></span>

<span data-ttu-id="80c5f-107">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getvolumeasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="80c5f-107">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="80c5f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="80c5f-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="80c5f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="80c5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c5f-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="80c5f-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="80c5f-111">Das Volume.</span><span class="sxs-lookup"><span data-stu-id="80c5f-111">The volume.</span></span> <span data-ttu-id="80c5f-112">Ein Wert zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="80c5f-112">A value between 0 and 100.</span></span> <span data-ttu-id="80c5f-113">0 gibt das minimale Volume an, und 100 gibt das maximale Volume an.</span><span class="sxs-lookup"><span data-stu-id="80c5f-113">0 indicates minimum volume, and 100 indicates maximum volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c5f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80c5f-114">Return value</span></span>

<span data-ttu-id="80c5f-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="80c5f-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="80c5f-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="80c5f-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="80c5f-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="80c5f-117">Return code</span></span>                                                                          | <span data-ttu-id="80c5f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80c5f-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="80c5f-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80c5f-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="80c5f-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80c5f-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80c5f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80c5f-121">Remarks</span></span>

<span data-ttu-id="80c5f-122">Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](getvolumeoperation-completed.md) Eigenschaft registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="80c5f-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getvolumeoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="80c5f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80c5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c5f-124">**Getvolumeoperation**</span><span class="sxs-lookup"><span data-stu-id="80c5f-124">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

