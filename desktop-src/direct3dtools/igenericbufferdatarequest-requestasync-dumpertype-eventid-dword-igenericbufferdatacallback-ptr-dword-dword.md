---
description: Fordert die Rückgabe von generischen Objektdaten an, die ein Objekt in der vsglog-Datei für das angegebene Ereignis und das angegebene Format beschreiben.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Igenericbufferdatarequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345420"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span data-ttu-id="ad401-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>Igenericbufferdatarequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="ad401-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync method</span></span>

<span data-ttu-id="ad401-104">Fordert die Rückgabe von generischen Objektdaten an, die ein Objekt in der vsglog-Datei für das angegebene Ereignis und das angegebene Format beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ad401-104">Requests to return generic object data that describes an object in the .vsglog file for the specified event and in the specified format.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad401-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad401-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ad401-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad401-106">Parameters</span></span>

<span data-ttu-id="ad401-107">*dumpertype* </span><span class="sxs-lookup"><span data-stu-id="ad401-107">*dumperType* </span></span>  
<span data-ttu-id="ad401-108">Das angegebene Format der Textdarstellung des-Objekts (HTML, XML usw.).</span><span class="sxs-lookup"><span data-stu-id="ad401-108">The specified format of the textual representation of the object (HTML, XML, etc.)</span></span>

<span data-ttu-id="ad401-109">*EventID* </span><span class="sxs-lookup"><span data-stu-id="ad401-109">*eventID* </span></span>  
<span data-ttu-id="ad401-110">Das angegebene Ereignis, mit dem der Inhalt des Puffers verglichen werden soll (z. b. kann sich ein Renderziel im Laufe der Zeit ändern).</span><span class="sxs-lookup"><span data-stu-id="ad401-110">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="ad401-111">*Requesteddatauid* </span><span class="sxs-lookup"><span data-stu-id="ad401-111">*RequestedDataUID* </span></span>  
<span data-ttu-id="ad401-112">Die Adresse des angegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad401-112">The address of the specified object.</span></span>

<span data-ttu-id="ad401-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ad401-113">*requestCallback* </span></span>  
<span data-ttu-id="ad401-114">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad401-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ad401-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="ad401-115">*requestCookie* </span></span>  
<span data-ttu-id="ad401-116">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad401-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ad401-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="ad401-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ad401-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad401-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad401-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad401-119">Return value</span></span>

<span data-ttu-id="ad401-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ad401-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ad401-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad401-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad401-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad401-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ad401-123">Header</span><span class="sxs-lookup"><span data-stu-id="ad401-123">Header</span></span></p></td><td><span data-ttu-id="ad401-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ad401-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ad401-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad401-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ad401-126">**Igenericbufferdatarequest**</span><span class="sxs-lookup"><span data-stu-id="ad401-126">**IGenericBufferDataRequest**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
