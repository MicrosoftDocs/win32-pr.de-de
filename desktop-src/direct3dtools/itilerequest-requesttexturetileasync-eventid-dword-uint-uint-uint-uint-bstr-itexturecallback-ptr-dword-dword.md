---
description: Fordert an, den Inhalt einer gekachelten Textur als zu erhalten. DDS-Datei (DirectDraw Surface).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Itilerequest:: requesttexturetileasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124711"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span data-ttu-id="f5db8-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>Itilerequest:: requesttexturetileasync-Methode</span><span class="sxs-lookup"><span data-stu-id="f5db8-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync method</span></span>

<span data-ttu-id="f5db8-104">Fordert an, den Inhalt einer gekachelten Textur als zu erhalten. DDS-Datei (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="f5db8-104">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5db8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5db8-105">Syntax</span></span>


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f5db8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5db8-106">Parameters</span></span>

<span data-ttu-id="f5db8-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="f5db8-107">*eventID* </span></span>  
<span data-ttu-id="f5db8-108">Das angegebene Ereignis, mit dem der Inhalt des Puffers verglichen werden soll (z. b. kann sich ein Renderziel im Laufe der Zeit ändern).</span><span class="sxs-lookup"><span data-stu-id="f5db8-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="f5db8-109">*texturemeleptr* </span><span class="sxs-lookup"><span data-stu-id="f5db8-109">*textureFileptr* </span></span>  
<span data-ttu-id="f5db8-110">Die Adresse des angegebenen Textur Objekts.</span><span class="sxs-lookup"><span data-stu-id="f5db8-110">The address of the specified texture object.</span></span>

<span data-ttu-id="f5db8-111">*tilesubresource* </span><span class="sxs-lookup"><span data-stu-id="f5db8-111">*tileSubresource* </span></span>  
<span data-ttu-id="f5db8-112">Die angegebene untergeordnete Quelle der Kachel.</span><span class="sxs-lookup"><span data-stu-id="f5db8-112">The specified subresource of the tile.</span></span>

<span data-ttu-id="f5db8-113">*Tilex* </span><span class="sxs-lookup"><span data-stu-id="f5db8-113">*tileX* </span></span>  
<span data-ttu-id="f5db8-114">Die angegebene X-Position der Kachel.</span><span class="sxs-lookup"><span data-stu-id="f5db8-114">The specified tile X position.</span></span>

<span data-ttu-id="f5db8-115">*tiley* </span><span class="sxs-lookup"><span data-stu-id="f5db8-115">*tileY* </span></span>  
<span data-ttu-id="f5db8-116">Die angegebene Y-Position der Kachel.</span><span class="sxs-lookup"><span data-stu-id="f5db8-116">The specified tile Y position.</span></span>

<span data-ttu-id="f5db8-117">*tilez* </span><span class="sxs-lookup"><span data-stu-id="f5db8-117">*tileZ* </span></span>  
<span data-ttu-id="f5db8-118">Die angegebene Z-Position der Kachel.</span><span class="sxs-lookup"><span data-stu-id="f5db8-118">The specified tile Z position.</span></span>

<span data-ttu-id="f5db8-119">*ddsfilename* </span><span class="sxs-lookup"><span data-stu-id="f5db8-119">*ddsFilename* </span></span>  
<span data-ttu-id="f5db8-120">Eine com-Zeichenfolge, die den Pfadnamen der DDS-Datei enthält, in die die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f5db8-120">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="f5db8-121">*prequestcallback* </span><span class="sxs-lookup"><span data-stu-id="f5db8-121">*pRequestCallback* </span></span>  
<span data-ttu-id="f5db8-122">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5db8-122">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="f5db8-123">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="f5db8-123">*requestCookie* </span></span>  
<span data-ttu-id="f5db8-124">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5db8-124">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="f5db8-125">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="f5db8-125">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f5db8-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5db8-126">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5db8-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5db8-127">Return value</span></span>

<span data-ttu-id="f5db8-128">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f5db8-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5db8-129">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5db8-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5db8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5db8-130">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f5db8-131">Header</span><span class="sxs-lookup"><span data-stu-id="f5db8-131">Header</span></span></p></td><td><span data-ttu-id="f5db8-132">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f5db8-132">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f5db8-133"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5db8-133"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f5db8-134">**Itilerequest**</span><span class="sxs-lookup"><span data-stu-id="f5db8-134">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
