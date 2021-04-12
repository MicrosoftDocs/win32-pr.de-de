---
description: Eine Rückruffunktion, die verwendet wird, um den Host den Status der Offline Analyse zu benachrichtigen.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisProgress\_DWORD\_DOUBLE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iofflineanalysiscallback:: offlineanalysisprogress-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 17847FD7-A10A-4E52-90AD-ADE446D87E73
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisProgress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4184be5d8d40b0ef46fe5e0029e9e4b1f38cf120
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392861"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span data-ttu-id="79d7f-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>Iofflineanalysiscallback:: offlineanalysisprogress-Methode</span><span class="sxs-lookup"><span data-stu-id="79d7f-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback::OfflineAnalysisProgress method</span></span>

<span data-ttu-id="79d7f-104">Eine Rückruffunktion, die verwendet wird, um den Host den Status der Offline Analyse zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="79d7f-104">A callback function used to notify the host of offline analysis progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d7f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79d7f-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="79d7f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79d7f-106">Parameters</span></span>

<span data-ttu-id="79d7f-107">*KS* </span><span class="sxs-lookup"><span data-stu-id="79d7f-107">*cookie* </span></span>  
<span data-ttu-id="79d7f-108">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79d7f-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="79d7f-109">*Progress* </span><span class="sxs-lookup"><span data-stu-id="79d7f-109">*progress* </span></span>  
<span data-ttu-id="79d7f-110">Der Fortschritt in Prozent.</span><span class="sxs-lookup"><span data-stu-id="79d7f-110">The progress percentage.</span></span>

## <a name="return-value"></a><span data-ttu-id="79d7f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79d7f-111">Return value</span></span>

<span data-ttu-id="79d7f-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="79d7f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79d7f-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79d7f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d7f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79d7f-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="79d7f-115">Header</span><span class="sxs-lookup"><span data-stu-id="79d7f-115">Header</span></span></p></td><td><span data-ttu-id="79d7f-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="79d7f-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="79d7f-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79d7f-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="79d7f-118">**Iofflineanalysiscallback**</span><span class="sxs-lookup"><span data-stu-id="79d7f-118">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
