---
description: Ruft Informationen darüber ab, welche Spalten (Ereignisdaten Typen) von der Ereignisliste unterstützt werden.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframeeventscallback:: getsupportedeventcolumns-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5b7bc9f74998a061ea63fca925263b7b4a0a4d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481942"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span data-ttu-id="95434-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>Iframeeventscallback:: getsupportedeventcolumns-Methode</span><span class="sxs-lookup"><span data-stu-id="95434-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback::GetSupportedEventColumns method</span></span>

<span data-ttu-id="95434-104">Ruft Informationen darüber ab, welche Spalten (Ereignisdaten Typen) von der Ereignisliste unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="95434-104">Gets information about which columns (types of event data) are supported by the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="95434-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95434-105">Syntax</span></span>


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="95434-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95434-106">Parameters</span></span>

<span data-ttu-id="95434-107">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="95434-107">*numColumns* </span></span>  
<span data-ttu-id="95434-108">Die Anzahl der von unterstützten Spalten.</span><span class="sxs-lookup"><span data-stu-id="95434-108">The number of columns supported by</span></span>

<span data-ttu-id="95434-109">*count0 \_ PIDs* </span><span class="sxs-lookup"><span data-stu-id="95434-109">*count0\_pIDs* </span></span>  
<span data-ttu-id="95434-110">Die IDs der einzelnen Spalten, die von der Ereignisliste unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="95434-110">The IDs of each column supported by the event list.</span></span>

<span data-ttu-id="95434-111">*count0 \_ pbstrinnames* </span><span class="sxs-lookup"><span data-stu-id="95434-111">*count0\_pBstrNames* </span></span>  
<span data-ttu-id="95434-112">Die Namen der einzelnen Spalten (als com-Zeichenfolge), die von der Ereignisliste unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="95434-112">The names of each column, as a COM string, supported by the event list.</span></span>

## <a name="return-value"></a><span data-ttu-id="95434-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95434-113">Return value</span></span>

<span data-ttu-id="95434-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="95434-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95434-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95434-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="95434-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95434-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="95434-117">Header</span><span class="sxs-lookup"><span data-stu-id="95434-117">Header</span></span></p></td><td><span data-ttu-id="95434-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="95434-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="95434-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95434-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="95434-120">**Iframeeventscallback**</span><span class="sxs-lookup"><span data-stu-id="95434-120">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
