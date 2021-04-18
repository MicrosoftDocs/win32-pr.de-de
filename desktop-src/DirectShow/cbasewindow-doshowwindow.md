---
description: Die doshowwindow-Methode legt den Anzeige Zustand des Fensters fest.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Cbasewindow. doshowwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372382"
---
# <a name="cbasewindowdoshowwindow-method"></a><span data-ttu-id="fb3e0-103">Cbasewindow. doshowwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="fb3e0-103">CBaseWindow.DoShowWindow method</span></span>

<span data-ttu-id="fb3e0-104">Die **doshowwindow** -Methode legt den Anzeige Zustand des Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="fb3e0-104">The **DoShowWindow** method sets the window's show state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb3e0-105">Syntax</span></span>


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a><span data-ttu-id="fb3e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb3e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3e0-107">*ShowCmd*</span><span class="sxs-lookup"><span data-stu-id="fb3e0-107">*ShowCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3e0-108">Flag, das angibt, wie das Fenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb3e0-108">Flag that specifies how the window is to be shown.</span></span> <span data-ttu-id="fb3e0-109">Der Wert kann eine beliebige Konstante sein, die für den *nCmdShow* -Parameter der [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fb3e0-109">The value can be any constant defined for the *nCmdShow* parameter of the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3e0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb3e0-110">Return value</span></span>

<span data-ttu-id="fb3e0-111">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fb3e0-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb3e0-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb3e0-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3e0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb3e0-113">Requirements</span></span>



| <span data-ttu-id="fb3e0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb3e0-114">Requirement</span></span> | <span data-ttu-id="fb3e0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fb3e0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3e0-116">Header</span><span class="sxs-lookup"><span data-stu-id="fb3e0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fb3e0-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb3e0-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb3e0-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb3e0-118">Library</span></span><br/> | <dl> <span data-ttu-id="fb3e0-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fb3e0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb3e0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb3e0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3e0-121">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

