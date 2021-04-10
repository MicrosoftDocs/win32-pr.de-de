---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Quelldateien zu benachrichtigen, die der Aufruf Liste zugeordnet sind.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Isourcefileingefocallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125540"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span data-ttu-id="63fa0-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>Isourcefileingefocallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="63fa0-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback method</span></span>

<span data-ttu-id="63fa0-104">Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Quelldateien zu benachrichtigen, die der Aufruf Liste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="63fa0-104">A callback function used to notify the host of information about source files associated with the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="63fa0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63fa0-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="63fa0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63fa0-106">Parameters</span></span>

<span data-ttu-id="63fa0-107">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="63fa0-107">*count* </span></span>  
<span data-ttu-id="63fa0-108">Die Anzahl der zurückgegebenen Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="63fa0-108">The number of source files returned.</span></span>

<span data-ttu-id="63fa0-109">*count0 \_ sourcefileingefobuffer* </span><span class="sxs-lookup"><span data-stu-id="63fa0-109">*count0\_sourceFileInfoBuffer* </span></span>  
<span data-ttu-id="63fa0-110">Die Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="63fa0-110">The source files.</span></span>

## <a name="return-value"></a><span data-ttu-id="63fa0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63fa0-111">Return value</span></span>

<span data-ttu-id="63fa0-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="63fa0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63fa0-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63fa0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63fa0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63fa0-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="63fa0-115">Header</span><span class="sxs-lookup"><span data-stu-id="63fa0-115">Header</span></span></p></td><td><span data-ttu-id="63fa0-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="63fa0-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="63fa0-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63fa0-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="63fa0-118">**Isourcefileingefocallback**</span><span class="sxs-lookup"><span data-stu-id="63fa0-118">**ISourceFileInfoCallback**</span></span>](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
