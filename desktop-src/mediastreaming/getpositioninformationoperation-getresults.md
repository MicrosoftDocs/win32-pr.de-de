---
title: Getpositioninformationoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von getpositioninformationasync gestartet wurde.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, getpositioninformationoperation-Schnittstelle
- Getpositioninformationoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726760"
---
# <a name="getpositioninformationoperationgetresults-method"></a><span data-ttu-id="76093-106">Getpositioninformationoperation. GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="76093-106">GetPositionInformationOperation.GetResults method</span></span>

<span data-ttu-id="76093-107">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getpositioninformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="76093-107">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="76093-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="76093-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="76093-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="76093-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76093-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="76093-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="76093-111">Ein Verweis auf eine [**positioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) -Struktur, die die Ergebnisse des Vorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="76093-111">A reference to a [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76093-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76093-112">Return value</span></span>

<span data-ttu-id="76093-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="76093-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="76093-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="76093-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="76093-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76093-115">Return code</span></span>                                                                          | <span data-ttu-id="76093-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76093-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="76093-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76093-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="76093-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76093-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76093-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76093-119">Remarks</span></span>

<span data-ttu-id="76093-120">Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](getpositioninformationoperation-completed.md) Eigenschaft registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="76093-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getpositioninformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="76093-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76093-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76093-122">**Getpositioninformationoperation**</span><span class="sxs-lookup"><span data-stu-id="76093-122">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

