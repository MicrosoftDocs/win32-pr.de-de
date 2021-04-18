---
description: Eine asynchrone Anforderung zum erhalten von Mesh-Daten aus dem angegebenen Ereignis.
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest3:: requestmeshasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 50fc73c803f708284ecef73f89ba74a452816bc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344776"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span data-ttu-id="eea5b-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3:: requestmeshasync-Methode</span><span class="sxs-lookup"><span data-stu-id="eea5b-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3::RequestMeshAsync method</span></span>

<span data-ttu-id="eea5b-104">Eine asynchrone Anforderung zum erhalten von Mesh-Daten aus dem angegebenen Ereignis.</span><span class="sxs-lookup"><span data-stu-id="eea5b-104">An asynchronous request to get mesh data from the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea5b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eea5b-105">Syntax</span></span>


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="eea5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eea5b-106">Parameters</span></span>

<span data-ttu-id="eea5b-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="eea5b-107">*eventID* </span></span>  
<span data-ttu-id="eea5b-108">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="eea5b-108">The specified event.</span></span>

<span data-ttu-id="eea5b-109">*meshfilename* </span><span class="sxs-lookup"><span data-stu-id="eea5b-109">*meshFilename* </span></span>  
<span data-ttu-id="eea5b-110">Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die die Mesh-Daten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="eea5b-110">A COM string containing the pathname of the file where the mesh data is written.</span></span>

<span data-ttu-id="eea5b-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="eea5b-111">*requestCallback* </span></span>  
<span data-ttu-id="eea5b-112">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eea5b-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="eea5b-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="eea5b-113">*requestCookie* </span></span>  
<span data-ttu-id="eea5b-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eea5b-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="eea5b-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="eea5b-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="eea5b-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="eea5b-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="eea5b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eea5b-117">Return value</span></span>

<span data-ttu-id="eea5b-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="eea5b-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eea5b-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eea5b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea5b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eea5b-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eea5b-121">Header</span><span class="sxs-lookup"><span data-stu-id="eea5b-121">Header</span></span></p></td><td><span data-ttu-id="eea5b-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eea5b-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="eea5b-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eea5b-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="eea5b-124">**IPipeLineStagesRequest3**</span><span class="sxs-lookup"><span data-stu-id="eea5b-124">**IPipeLineStagesRequest3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
