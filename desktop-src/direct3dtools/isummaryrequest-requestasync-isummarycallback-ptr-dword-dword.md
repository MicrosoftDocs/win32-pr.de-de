---
description: Eine asynchrone Anforderung zum erhalten von Zusammenfassungs Informationen zu einem Grafik Protokoll.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Isummaryrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339668"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span data-ttu-id="9a181-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>Isummaryrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="9a181-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync method</span></span>

<span data-ttu-id="9a181-104">Eine asynchrone Anforderung zum erhalten von Zusammenfassungs Informationen zu einem Grafik Protokoll.</span><span class="sxs-lookup"><span data-stu-id="9a181-104">An asynchronous request to get summary information about a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a181-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a181-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="9a181-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a181-106">Parameters</span></span>

<span data-ttu-id="9a181-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="9a181-107">*requestCallback* </span></span>  
<span data-ttu-id="9a181-108">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a181-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="9a181-109">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="9a181-109">*requestCookie* </span></span>  
<span data-ttu-id="9a181-110">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a181-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="9a181-111">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="9a181-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="9a181-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a181-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a181-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a181-113">Return value</span></span>

<span data-ttu-id="9a181-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a181-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a181-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a181-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a181-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a181-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9a181-117">Header</span><span class="sxs-lookup"><span data-stu-id="9a181-117">Header</span></span></p></td><td><span data-ttu-id="9a181-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9a181-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9a181-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a181-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9a181-120">**Isummaryrequest**</span><span class="sxs-lookup"><span data-stu-id="9a181-120">**ISummaryRequest**</span></span>](/windows/desktop/direct3dtools/isummaryrequest)

 

 
