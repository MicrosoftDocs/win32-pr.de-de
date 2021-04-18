---
description: Eine Rückruffunktion, die zum Benachrichtigen des Hosts über Zusammenfassungs Informationen des Grafik Protokolls verwendet wird.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Isummarycallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344926"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span data-ttu-id="17751-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>Isummarycallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="17751-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback::ResultCallback method</span></span>

<span data-ttu-id="17751-104">Eine Rückruffunktion, die zum Benachrichtigen des Hosts über Zusammenfassungs Informationen des Grafik Protokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17751-104">A callback function used to notify the host of graphics log summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="17751-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17751-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a><span data-ttu-id="17751-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17751-106">Parameters</span></span>

<span data-ttu-id="17751-107">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="17751-107">*count* </span></span>  
<span data-ttu-id="17751-108">Die Anzahl der zurückgegebenen Zusammenfassungs Informationselemente.</span><span class="sxs-lookup"><span data-stu-id="17751-108">The number of summary information items returned.</span></span>

<span data-ttu-id="17751-109">*count0 \_ summaryitem* </span><span class="sxs-lookup"><span data-stu-id="17751-109">*count0\_summaryItem* </span></span>  
<span data-ttu-id="17751-110">Die Zusammenfassungs Informationselemente (Schlüssel-Wert-Paare).</span><span class="sxs-lookup"><span data-stu-id="17751-110">The summary information items (key-value pairs).</span></span>

## <a name="return-value"></a><span data-ttu-id="17751-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17751-111">Return value</span></span>

<span data-ttu-id="17751-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="17751-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17751-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17751-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="17751-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17751-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="17751-115">Header</span><span class="sxs-lookup"><span data-stu-id="17751-115">Header</span></span></p></td><td><span data-ttu-id="17751-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="17751-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="17751-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17751-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="17751-118">**Isummarycallback**</span><span class="sxs-lookup"><span data-stu-id="17751-118">**ISummaryCallback**</span></span>](/windows/desktop/direct3dtools/isummarycallback)

 

 
