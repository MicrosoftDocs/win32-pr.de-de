---
description: Eine Rückruffunktion, die verwendet wird, um den Host von Fehlern während der Erfassung oder Wiedergabe zu benachrichtigen.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ifleiocallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124621"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span data-ttu-id="65ca0-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>Ifleiocallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="65ca0-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback::ResultCallback method</span></span>

<span data-ttu-id="65ca0-104">Eine Rückruffunktion, die verwendet wird, um den Host von Fehlern während der Erfassung oder Wiedergabe zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="65ca0-104">A callback function used to notify the host of errors while during capture or playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ca0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65ca0-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a><span data-ttu-id="65ca0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65ca0-106">Parameters</span></span>

<span data-ttu-id="65ca0-107">*resultstate* </span><span class="sxs-lookup"><span data-stu-id="65ca0-107">*resultState* </span></span>  
<span data-ttu-id="65ca0-108">Gibt die Art des aufgetretenen Fehlers an.</span><span class="sxs-lookup"><span data-stu-id="65ca0-108">Indicates the kind of error encountered.</span></span>

## <a name="return-value"></a><span data-ttu-id="65ca0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65ca0-109">Return value</span></span>

<span data-ttu-id="65ca0-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="65ca0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65ca0-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="65ca0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ca0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65ca0-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="65ca0-113">Header</span><span class="sxs-lookup"><span data-stu-id="65ca0-113">Header</span></span></p></td><td><span data-ttu-id="65ca0-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="65ca0-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="65ca0-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65ca0-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="65ca0-116">**IFI-ocallback**</span><span class="sxs-lookup"><span data-stu-id="65ca0-116">**IFileIOCallback**</span></span>](/windows/desktop/direct3dtools/ifileiocallback)

 

 
