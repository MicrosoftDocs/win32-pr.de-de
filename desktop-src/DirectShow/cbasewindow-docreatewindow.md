---
description: Das Fenster wird von der dokreatewindow-Methode erstellt.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: CBaseWindow.DoCreatewindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351204"
---
# <a name="cbasewindowdocreatewindow-method"></a><span data-ttu-id="9ba37-103">CBaseWindow.DoCreatewindow-Methode</span><span class="sxs-lookup"><span data-stu-id="9ba37-103">CBaseWindow.DoCreateWindow method</span></span>

<span data-ttu-id="9ba37-104">Mit der- `DoCreateWindow` Methode wird das-Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ba37-104">The `DoCreateWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba37-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ba37-105">Syntax</span></span>


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a><span data-ttu-id="9ba37-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ba37-106">Parameters</span></span>

<span data-ttu-id="9ba37-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ba37-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ba37-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ba37-108">Return value</span></span>

<span data-ttu-id="9ba37-109">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="9ba37-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba37-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ba37-110">Remarks</span></span>

<span data-ttu-id="9ba37-111">Die [**cbasewindow::P Analyse Window**](cbasewindow-preparewindow.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="9ba37-111">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba37-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ba37-112">Requirements</span></span>



| <span data-ttu-id="9ba37-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ba37-113">Requirement</span></span> | <span data-ttu-id="9ba37-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba37-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba37-115">Header</span><span class="sxs-lookup"><span data-stu-id="9ba37-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9ba37-116"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ba37-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9ba37-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ba37-117">Library</span></span><br/> | <dl> <span data-ttu-id="9ba37-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9ba37-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba37-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ba37-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba37-120">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9ba37-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




