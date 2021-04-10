---
description: Fordert an, den Rohinhalt einer Kachel zu erhalten.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Itilerequest:: requestbuffertileasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213995"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span data-ttu-id="01b3a-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>Itilerequest:: requestbuffertileasync-Methode</span><span class="sxs-lookup"><span data-stu-id="01b3a-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest::RequestBufferTileAsync method</span></span>

<span data-ttu-id="01b3a-104">Fordert an, den Rohinhalt einer Kachel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="01b3a-104">Requests to get the raw contents of a tile.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01b3a-105">Syntax</span></span>


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="01b3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01b3a-106">Parameters</span></span>

<span data-ttu-id="01b3a-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="01b3a-107">*eventID* </span></span>  
<span data-ttu-id="01b3a-108">Das angegebene Ereignis, mit dem der Inhalt der Kachel abgeglichen werden soll (z. b. ein Renderziel kann sich im Laufe der Zeit ändern).</span><span class="sxs-lookup"><span data-stu-id="01b3a-108">The specified event to match the tile's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="01b3a-109">*Requesteddatauid* </span><span class="sxs-lookup"><span data-stu-id="01b3a-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="01b3a-110">Die Adresse der angegebenen Kachel.</span><span class="sxs-lookup"><span data-stu-id="01b3a-110">The address of the specified tile.</span></span>

<span data-ttu-id="01b3a-111">*Datei* </span><span class="sxs-lookup"><span data-stu-id="01b3a-111">*File* </span></span>  
<span data-ttu-id="01b3a-112">Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="01b3a-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="01b3a-113">*tileingedex* </span><span class="sxs-lookup"><span data-stu-id="01b3a-113">*tileIndex* </span></span>  
<span data-ttu-id="01b3a-114">Der Index der angegebenen Kachel.</span><span class="sxs-lookup"><span data-stu-id="01b3a-114">The index of the specified tile.</span></span>

<span data-ttu-id="01b3a-115">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="01b3a-115">*requestCallback* </span></span>  
<span data-ttu-id="01b3a-116">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01b3a-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="01b3a-117">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="01b3a-117">*requestCookie* </span></span>  
<span data-ttu-id="01b3a-118">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="01b3a-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="01b3a-119">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="01b3a-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="01b3a-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="01b3a-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="01b3a-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01b3a-121">Return value</span></span>

<span data-ttu-id="01b3a-122">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01b3a-122">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="01b3a-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01b3a-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b3a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01b3a-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="01b3a-125">Header</span><span class="sxs-lookup"><span data-stu-id="01b3a-125">Header</span></span></p></td><td><span data-ttu-id="01b3a-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="01b3a-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="01b3a-127"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01b3a-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="01b3a-128">**Itilerequest**</span><span class="sxs-lookup"><span data-stu-id="01b3a-128">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
