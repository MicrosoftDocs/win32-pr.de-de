---
title: Playbackoperation. GetResults-Methode
description: Gibt die Ergebnisse eines asynchronen Vorgangs zurück, der von einer der MediaRenderer-Wiedergabe Methoden gestartet wurde.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, playbackoperation-Schnittstelle
- Playbackoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104388914"
---
# <a name="playbackoperationgetresults-method"></a><span data-ttu-id="cf0ae-106">Playbackoperation. GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="cf0ae-106">PlaybackOperation.GetResults method</span></span>

<span data-ttu-id="cf0ae-107">Gibt die Ergebnisse eines asynchronen Vorgangs zurück, der von einer der [**MediaRenderer**](mediarenderer.md) -Wiedergabe Methoden gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-107">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf0ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf0ae-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="cf0ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf0ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf0ae-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cf0ae-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0ae-111">Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-111">The result of the operation.</span></span> <span data-ttu-id="cf0ae-112">Der Wert 0 gibt an, dass der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-112">A value of 0 indicates that the operation completed.</span></span> <span data-ttu-id="cf0ae-113">Andere Werte sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-113">Other values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf0ae-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf0ae-114">Return value</span></span>

<span data-ttu-id="cf0ae-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cf0ae-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cf0ae-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cf0ae-117">Return code</span></span>                                                                          | <span data-ttu-id="cf0ae-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf0ae-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cf0ae-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf0ae-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cf0ae-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf0ae-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf0ae-121">Remarks</span></span>

<span data-ttu-id="cf0ae-122">Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](playbackoperation-completed.md) Eigenschaft registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](playbackoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf0ae-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf0ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0ae-124">**Playbackoperation**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-124">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 





