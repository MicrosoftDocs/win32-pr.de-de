---
description: Ein Rückruf, der den Host über den Fortschritt einer zugeordneten Anforderung benachrichtigt.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipixprogresscallback::P rogress-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392661"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span data-ttu-id="aa3e1-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>Ipixprogresscallback::P rogress-Methode</span><span class="sxs-lookup"><span data-stu-id="aa3e1-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::Progress method</span></span>

<span data-ttu-id="aa3e1-104">Ein Rückruf, der den Host über den Fortschritt einer zugeordneten Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="aa3e1-104">A callback that notifies the host of the progress of an associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa3e1-105">Syntax</span></span>


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a><span data-ttu-id="aa3e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa3e1-106">Parameters</span></span>

<span data-ttu-id="aa3e1-107">*Strömung* </span><span class="sxs-lookup"><span data-stu-id="aa3e1-107">*current* </span></span>  
<span data-ttu-id="aa3e1-108">Der Teil einer Anforderung wurde abgeschlossen, als Anzahl der abgeschlossenen Schritte.</span><span class="sxs-lookup"><span data-stu-id="aa3e1-108">The portion of a request completed, as a count of the number of steps completed.</span></span>

<span data-ttu-id="aa3e1-109">*MaxSize* </span><span class="sxs-lookup"><span data-stu-id="aa3e1-109">*maxSize* </span></span>  
<span data-ttu-id="aa3e1-110">Die Gesamtanzahl der Schritte zum Durchführen der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aa3e1-110">The total number of steps to complete the request.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa3e1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa3e1-111">Return value</span></span>

<span data-ttu-id="aa3e1-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="aa3e1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aa3e1-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa3e1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa3e1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa3e1-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aa3e1-115">Header</span><span class="sxs-lookup"><span data-stu-id="aa3e1-115">Header</span></span></p></td><td><span data-ttu-id="aa3e1-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aa3e1-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="aa3e1-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa3e1-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="aa3e1-118">**Ipixprogresscallback**</span><span class="sxs-lookup"><span data-stu-id="aa3e1-118">**IPixProgressCallback**</span></span>](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
