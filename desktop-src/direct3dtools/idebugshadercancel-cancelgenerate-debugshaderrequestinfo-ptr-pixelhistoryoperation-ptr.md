---
description: Anforderungen zum Abbrechen der Generierung von shaderlaufverfolgungs-Anweisungen in einer Debuganforderung.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Idebugshadercancel:: cancelgenerate-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10DA5080-3AA6-47AA-BFE7-774BC26C7F95
api_name:
- IDebugShaderCancel.CancelGenerate
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c2754f0d390960775b11ac5da121d5e6a20705a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345994"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span data-ttu-id="24e89-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>Idebugshadercancel:: cancelgenerate-Methode</span><span class="sxs-lookup"><span data-stu-id="24e89-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel::CancelGenerate method</span></span>

<span data-ttu-id="24e89-104">Anforderungen zum Abbrechen der Generierung von shaderlaufverfolgungs-Anweisungen in einer Debuganforderung.</span><span class="sxs-lookup"><span data-stu-id="24e89-104">Requests to cancel generation of shader trace instructions in a debug request.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24e89-105">Syntax</span></span>


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a><span data-ttu-id="24e89-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24e89-106">Parameters</span></span>

<span data-ttu-id="24e89-107">*RequestInfo* </span><span class="sxs-lookup"><span data-stu-id="24e89-107">*requestInfo* </span></span>  
<span data-ttu-id="24e89-108">Die Adresse einer debugshaderrequestinfo-Struktur, die das angeforderte Ereignis/Scheitelpunkt/Pixel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="24e89-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="24e89-109">*ppixelhistory* </span><span class="sxs-lookup"><span data-stu-id="24e89-109">*pPixelHistory* </span></span>  
<span data-ttu-id="24e89-110">Die Adresse der Pixel Verlaufs Ergebnisse, die zum Suchen des zugeordneten Pixels zum Debuggen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24e89-110">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="24e89-111">Gilt nur beim Debuggen eines Pixelshaders.</span><span class="sxs-lookup"><span data-stu-id="24e89-111">Only applies when debugging a pixel shader.</span></span>

## <a name="return-value"></a><span data-ttu-id="24e89-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24e89-112">Return value</span></span>

<span data-ttu-id="24e89-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="24e89-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24e89-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24e89-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e89-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24e89-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="24e89-116">Header</span><span class="sxs-lookup"><span data-stu-id="24e89-116">Header</span></span></p></td><td><span data-ttu-id="24e89-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="24e89-117">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="24e89-118"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24e89-118"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="24e89-119">**Idebugshadercancel**</span><span class="sxs-lookup"><span data-stu-id="24e89-119">**IDebugShaderCancel**</span></span>](/windows/desktop/direct3dtools/idebugshadercancel)

 

 
