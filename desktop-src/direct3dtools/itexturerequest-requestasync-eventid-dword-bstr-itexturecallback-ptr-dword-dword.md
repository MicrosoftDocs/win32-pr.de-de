---
description: Fordert an, den Inhalt einer Textur als zu erhalten. DDS-Datei (DirectDraw Surface).
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Itexturerequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482566"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span data-ttu-id="8b1ed-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>Itexturerequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="8b1ed-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest::RequestAsync method</span></span>

<span data-ttu-id="8b1ed-104">Fordert an, den Inhalt einer Textur als zu erhalten. DDS-Datei (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="8b1ed-104">Requests to get the contents of a texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b1ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b1ed-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="8b1ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b1ed-106">Parameters</span></span>

<span data-ttu-id="8b1ed-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="8b1ed-107">*eventID* </span></span>  
<span data-ttu-id="8b1ed-108">Das angegebene Ereignis, mit dem der Inhalt des Puffers verglichen werden soll (z. b. kann sich ein Renderziel im Laufe der Zeit ändern).</span><span class="sxs-lookup"><span data-stu-id="8b1ed-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="8b1ed-109">*texturemeleptr* </span><span class="sxs-lookup"><span data-stu-id="8b1ed-109">*textureFileptr* </span></span>  
<span data-ttu-id="8b1ed-110">Die Adresse des Textur Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-110">The address of the texture object.</span></span>

<span data-ttu-id="8b1ed-111">*ddsfilename* </span><span class="sxs-lookup"><span data-stu-id="8b1ed-111">*ddsFilename* </span></span>  
<span data-ttu-id="8b1ed-112">Eine com-Zeichenfolge, die den Pfadnamen der DDS-Datei enthält, in die die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-112">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="8b1ed-113">*prequestcallback* </span><span class="sxs-lookup"><span data-stu-id="8b1ed-113">*pRequestCallback* </span></span>  
<span data-ttu-id="8b1ed-114">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="8b1ed-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="8b1ed-115">*requestCookie* </span></span>  
<span data-ttu-id="8b1ed-116">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="8b1ed-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="8b1ed-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="8b1ed-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b1ed-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b1ed-119">Return value</span></span>

<span data-ttu-id="8b1ed-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b1ed-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1ed-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b1ed-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8b1ed-123">Header</span><span class="sxs-lookup"><span data-stu-id="8b1ed-123">Header</span></span></p></td><td><span data-ttu-id="8b1ed-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8b1ed-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8b1ed-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b1ed-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8b1ed-126">**Itexturerequest**</span><span class="sxs-lookup"><span data-stu-id="8b1ed-126">**ITextureRequest**</span></span>](/windows/desktop/direct3dtools/itexturerequest)

 

 
