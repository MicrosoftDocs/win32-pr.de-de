---
description: Flag, das angibt, ob das Fenster seine Zerstörungs Nachricht postet oder sendet.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Cbasewindow:: m_bDoPostToDestroy Member (winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359676"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a><span data-ttu-id="1369c-103">Cbasewindow:: m \_ bdopostdedestroy-Member</span><span class="sxs-lookup"><span data-stu-id="1369c-103">CBaseWindow::m\_bDoPostToDestroy member</span></span>

<span data-ttu-id="1369c-104">Flag, das angibt, ob das Fenster seine Zerstörungs Nachricht postet oder sendet.</span><span class="sxs-lookup"><span data-stu-id="1369c-104">Flag that specifies whether the window posts or sends its destruction message.</span></span> <span data-ttu-id="1369c-105">**True** gibt an, dass die [**cbasewindow::D onewithwindow**](cbasewindow-donewithwindow.md) -Methode die **PostMessage** -Funktion verwendet, um sich selbst eine private Zerstörungs Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="1369c-105">If **TRUE**, the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method uses the **PostMessage** function to send itself a private destruction message.</span></span> <span data-ttu-id="1369c-106">**False** gibt an, dass **donewithwindow** die **SendMessage** -Funktion verwendet, um die Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="1369c-106">If **FALSE**, **DoneWithWindow** uses the **SendMessage** function to send the message.</span></span> <span data-ttu-id="1369c-107">Standardmäßig ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="1369c-107">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1369c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1369c-108">Syntax</span></span>


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a><span data-ttu-id="1369c-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1369c-109">Requirements</span></span>



| <span data-ttu-id="1369c-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1369c-110">Requirement</span></span> | <span data-ttu-id="1369c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1369c-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1369c-112">Header</span><span class="sxs-lookup"><span data-stu-id="1369c-112">Header</span></span><br/>  | <dl> <span data-ttu-id="1369c-113"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1369c-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1369c-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1369c-114">Library</span></span><br/> | <dl> <span data-ttu-id="1369c-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1369c-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1369c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1369c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1369c-117">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1369c-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




