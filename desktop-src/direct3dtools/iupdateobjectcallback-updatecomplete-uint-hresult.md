---
description: Ein Rückruf, der verwendet wird, um den Host zu benachrichtigen, dass ein Objekt aktualisiert wurde.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iupdateobjectcallback:: updatecomplete-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124694"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span data-ttu-id="4c902-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>Iupdateobjectcallback:: updatecomplete-Methode</span><span class="sxs-lookup"><span data-stu-id="4c902-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete method</span></span>

<span data-ttu-id="4c902-104">Ein Rückruf, der verwendet wird, um den Host zu benachrichtigen, dass ein Objekt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4c902-104">A callback used to notify the host that an object was updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c902-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c902-105">Syntax</span></span>


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a><span data-ttu-id="4c902-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c902-106">Parameters</span></span>

<span data-ttu-id="4c902-107">*objectaddress* </span><span class="sxs-lookup"><span data-stu-id="4c902-107">*objectAddress* </span></span>  
<span data-ttu-id="4c902-108">Die ID des Objekts, das aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4c902-108">The ID of the object that was updated.</span></span>

<span data-ttu-id="4c902-109">*result* </span><span class="sxs-lookup"><span data-stu-id="4c902-109">*result* </span></span>  
<span data-ttu-id="4c902-110">Gibt an, ob das Update erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4c902-110">Indicates whether or not the update succeeded.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c902-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c902-111">Return value</span></span>

<span data-ttu-id="4c902-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4c902-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c902-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4c902-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c902-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c902-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4c902-115">Header</span><span class="sxs-lookup"><span data-stu-id="4c902-115">Header</span></span></p></td><td><span data-ttu-id="4c902-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4c902-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4c902-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c902-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4c902-118">**Iupdateobjectcallback**</span><span class="sxs-lookup"><span data-stu-id="4c902-118">**IUpdateObjectCallback**</span></span>](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
