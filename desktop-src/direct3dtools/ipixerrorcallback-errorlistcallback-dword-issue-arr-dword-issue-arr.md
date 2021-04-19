---
description: Ein Rückruf, der den Host von Fehlern benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixerrorcallback:: errorlistcallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344928"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span data-ttu-id="faa86-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>Ipixerrorcallback:: errorlistcallback-Methode</span><span class="sxs-lookup"><span data-stu-id="faa86-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback::ErrorListCallback method</span></span>

<span data-ttu-id="faa86-104">Ein Rückruf, der den Host von Fehlern benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="faa86-104">A callback that notifies the host of errors returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="faa86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="faa86-105">Syntax</span></span>


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a><span data-ttu-id="faa86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="faa86-106">Parameters</span></span>

<span data-ttu-id="faa86-107">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="faa86-107">*count* </span></span>  
<span data-ttu-id="faa86-108">Die Anzahl der Fehler.</span><span class="sxs-lookup"><span data-stu-id="faa86-108">The number of errors.</span></span>

<span data-ttu-id="faa86-109">*count0 \_ errorlist* </span><span class="sxs-lookup"><span data-stu-id="faa86-109">*count0\_errorList* </span></span>  
<span data-ttu-id="faa86-110">Die Fehler.</span><span class="sxs-lookup"><span data-stu-id="faa86-110">The errors.</span></span>

<span data-ttu-id="faa86-111">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="faa86-111">*count* </span></span>  
<span data-ttu-id="faa86-112">Die Anzahl der warningns.</span><span class="sxs-lookup"><span data-stu-id="faa86-112">The number of warningns.</span></span>

<span data-ttu-id="faa86-113">*count0 \_ warninglist* </span><span class="sxs-lookup"><span data-stu-id="faa86-113">*count0\_warningList* </span></span>  
<span data-ttu-id="faa86-114">Die Warnungen.</span><span class="sxs-lookup"><span data-stu-id="faa86-114">The warnings.</span></span>

## <a name="return-value"></a><span data-ttu-id="faa86-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="faa86-115">Return value</span></span>

<span data-ttu-id="faa86-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="faa86-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="faa86-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="faa86-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa86-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faa86-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="faa86-119">Header</span><span class="sxs-lookup"><span data-stu-id="faa86-119">Header</span></span></p></td><td><span data-ttu-id="faa86-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="faa86-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="faa86-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faa86-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="faa86-122">**Ipixerrorcallback**</span><span class="sxs-lookup"><span data-stu-id="faa86-122">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
