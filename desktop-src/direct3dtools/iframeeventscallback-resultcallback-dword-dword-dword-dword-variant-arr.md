---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Ereignisse in der Ereignisliste zu benachrichtigen.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframeeventscallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213919"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span data-ttu-id="40dbc-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>Iframeeventscallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="40dbc-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback method</span></span>

<span data-ttu-id="40dbc-104">Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Ereignisse in der Ereignisliste zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="40dbc-104">A callback function used to notify the host of information about events in the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="40dbc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40dbc-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="40dbc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40dbc-106">Parameters</span></span>

<span data-ttu-id="40dbc-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="40dbc-107">*frameNumber* </span></span>  
<span data-ttu-id="40dbc-108">Die dem Ereignis zugeordnete Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="40dbc-108">The frame number associated with the events.</span></span>

<span data-ttu-id="40dbc-109">*numElements* </span><span class="sxs-lookup"><span data-stu-id="40dbc-109">*numElements* </span></span>  
<span data-ttu-id="40dbc-110">Die Gesamtanzahl der Felder in allen Spalten aller Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="40dbc-110">The total number of fields in all columns of all events.</span></span>

<span data-ttu-id="40dbc-111">*numRows* </span><span class="sxs-lookup"><span data-stu-id="40dbc-111">*numRows* </span></span>  
<span data-ttu-id="40dbc-112">Die Anzahl der Ereignisse im Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="40dbc-112">The number of events in the result.</span></span>

<span data-ttu-id="40dbc-113">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="40dbc-113">*numColumns* </span></span>  
<span data-ttu-id="40dbc-114">Die Anzahl der Spalten (Felder) in jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="40dbc-114">The number of columns (fields) in each row.</span></span>

<span data-ttu-id="40dbc-115">*count1 \_ prowdata* </span><span class="sxs-lookup"><span data-stu-id="40dbc-115">*count1\_pRowData* </span></span>  
<span data-ttu-id="40dbc-116">Informationen zu den Ereignissen ein Element für jedes Feld jedes Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="40dbc-116">Information about the events; one item for each field of each event.</span></span>

## <a name="return-value"></a><span data-ttu-id="40dbc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40dbc-117">Return value</span></span>

<span data-ttu-id="40dbc-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="40dbc-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40dbc-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40dbc-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40dbc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40dbc-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="40dbc-121">Header</span><span class="sxs-lookup"><span data-stu-id="40dbc-121">Header</span></span></p></td><td><span data-ttu-id="40dbc-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="40dbc-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="40dbc-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40dbc-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="40dbc-124">**Iframeeventscallback**</span><span class="sxs-lookup"><span data-stu-id="40dbc-124">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
