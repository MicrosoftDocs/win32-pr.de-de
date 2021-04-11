---
description: Fordert an, den Rohdaten Inhalt eines Objekts (Puffer, Textur, renderzielansicht usw.) zu erhalten.
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ibufferobjectdatarequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124171"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span data-ttu-id="f6f74-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>Ibufferobjectdatarequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="f6f74-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest::RequestAsync method</span></span>

<span data-ttu-id="f6f74-104">Fordert an, den Rohdaten Inhalt eines Objekts (Puffer, Textur, renderzielansicht usw.) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6f74-104">Requests to get the raw contents of an object (buffer, texture, render target view, etc.)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6f74-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f6f74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6f74-106">Parameters</span></span>

<span data-ttu-id="f6f74-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="f6f74-107">*eventID* </span></span>  
<span data-ttu-id="f6f74-108">Das angegebene Ereignis, mit dem der Inhalt des Puffers verglichen werden soll (z. b. kann sich ein Renderziel im Laufe der Zeit ändern).</span><span class="sxs-lookup"><span data-stu-id="f6f74-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="f6f74-109">*Requesteddatauid* </span><span class="sxs-lookup"><span data-stu-id="f6f74-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="f6f74-110">Die Adresse des angegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="f6f74-110">The address of the specified object.</span></span>

<span data-ttu-id="f6f74-111">*Datei* </span><span class="sxs-lookup"><span data-stu-id="f6f74-111">*File* </span></span>  
<span data-ttu-id="f6f74-112">Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f6f74-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="f6f74-113">*Ges* </span><span class="sxs-lookup"><span data-stu-id="f6f74-113">*Format* </span></span>  
<span data-ttu-id="f6f74-114">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6f74-114">Not currently used.</span></span> <span data-ttu-id="f6f74-115">Eine com-Zeichenfolge, die das Ausgabeformat angibt.</span><span class="sxs-lookup"><span data-stu-id="f6f74-115">A COM string that specifies the output format.</span></span>

<span data-ttu-id="f6f74-116">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="f6f74-116">*requestCallback* </span></span>  
<span data-ttu-id="f6f74-117">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6f74-117">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="f6f74-118">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="f6f74-118">*requestCookie* </span></span>  
<span data-ttu-id="f6f74-119">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6f74-119">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="f6f74-120">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="f6f74-120">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f6f74-121">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6f74-121">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6f74-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6f74-122">Return value</span></span>

<span data-ttu-id="f6f74-123">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f6f74-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6f74-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6f74-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f74-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6f74-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f6f74-126">Header</span><span class="sxs-lookup"><span data-stu-id="f6f74-126">Header</span></span></p></td><td><span data-ttu-id="f6f74-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f6f74-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f6f74-128"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6f74-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f6f74-129">**Ibufferobjectdatarequest**</span><span class="sxs-lookup"><span data-stu-id="f6f74-129">**IBufferObjectDataRequest**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
