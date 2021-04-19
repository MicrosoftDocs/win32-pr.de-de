---
description: Die preparewindow-Methode erstellt das Fenster.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Cbasewindow. preparewindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370318"
---
# <a name="cbasewindowpreparewindow-method"></a><span data-ttu-id="9e006-103">Cbasewindow. preparewindow-Methode</span><span class="sxs-lookup"><span data-stu-id="9e006-103">CBaseWindow.PrepareWindow method</span></span>

<span data-ttu-id="9e006-104">Mit der- `PrepareWindow` Methode wird das-Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e006-104">The `PrepareWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e006-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e006-105">Syntax</span></span>


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a><span data-ttu-id="9e006-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e006-106">Parameters</span></span>

<span data-ttu-id="9e006-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9e006-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e006-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e006-108">Return value</span></span>

<span data-ttu-id="9e006-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9e006-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9e006-110">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e006-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="9e006-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9e006-111">Return code</span></span>                                                                            | <span data-ttu-id="9e006-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e006-112">Description</span></span>         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="9e006-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e006-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="9e006-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9e006-114">Success.</span></span><br/> |
| <dl> <span data-ttu-id="9e006-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9e006-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="9e006-116">Fehler.</span><span class="sxs-lookup"><span data-stu-id="9e006-116">Failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e006-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e006-117">Remarks</span></span>

<span data-ttu-id="9e006-118">Ruft diese Methode auf, nachdem das-Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9e006-118">Call this method after creating the object.</span></span> <span data-ttu-id="9e006-119">Diese Methode führt eine anfängliche Buchführung aus und ruft dann die [**cbasewindow::D okreatewindow**](cbasewindow-docreatewindow.md) -Methode auf, um das Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e006-119">This method performs some initial bookkeeping and then calls the [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method to create the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e006-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e006-120">Requirements</span></span>



| <span data-ttu-id="9e006-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e006-121">Requirement</span></span> | <span data-ttu-id="9e006-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9e006-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e006-123">Header</span><span class="sxs-lookup"><span data-stu-id="9e006-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9e006-124"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e006-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9e006-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e006-125">Library</span></span><br/> | <dl> <span data-ttu-id="9e006-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9e006-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e006-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e006-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e006-128">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9e006-128">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




