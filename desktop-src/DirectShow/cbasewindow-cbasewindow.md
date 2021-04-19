---
description: Konstruktormethode.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Cbasewindow. cbasewindow-Konstruktor (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1741f8596210afac676a7e81f57b46e18fbba9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359252"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="f2219-103">Cbasewindow. cbasewindow-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="f2219-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="f2219-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f2219-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2219-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2219-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="f2219-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2219-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2219-107">*bdogetdc*</span><span class="sxs-lookup"><span data-stu-id="f2219-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="f2219-108">Boolescher Wert, der angibt, ob der Gerätekontext abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2219-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="f2219-109">*bpostto Destroy*</span><span class="sxs-lookup"><span data-stu-id="f2219-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="f2219-110">Boolescher Wert, der die [**cbasewindow:: m \_ bdopostdedestroy**](cbasewindow-m-bdoposttodestroy.md) -Element Variable angibt.</span><span class="sxs-lookup"><span data-stu-id="f2219-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2219-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2219-111">Remarks</span></span>

<span data-ttu-id="f2219-112">Nachdem Sie das-Objekt erstellt haben, rufen Sie die [**cbasewindow::P Analyse Window**](cbasewindow-preparewindow.md) -Methode auf, um das-Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2219-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="f2219-113">**Preparewindow** ist eine virtuelle Methode.</span><span class="sxs-lookup"><span data-stu-id="f2219-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="f2219-114">[**Cbasewindow:: initialicwindow**](cbasewindow-initialisewindow.md)wird auch als virtuelle Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f2219-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="f2219-115">Diese Methoden werden vom-Konstruktor getrennt, sodass abgeleitete Klassen Sie ggf. überschreiben können.</span><span class="sxs-lookup"><span data-stu-id="f2219-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="f2219-116">Wenn der Wert des *bdogetdc* -Parameters " **true**" ist, ruft das- `CBaseWindow` Objekt ein Handle für den Gerätekontext des Fensters ab und speichert es in der [**cbasewindow:: m-Element Variablen ( \_ hdc**](cbasewindow-m-hdc.md) ).</span><span class="sxs-lookup"><span data-stu-id="f2219-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="f2219-117">Das-Objekt erstellt außerdem einen kompatiblen Arbeitsspeicher-DC, der in der Element Variablen [**cbasewindow:: m \_ memorydc**](cbasewindow-m-memorydc.md) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f2219-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="f2219-118">Diese Aktionen treten in der **initialierwindow** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f2219-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2219-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2219-119">Requirements</span></span>



| <span data-ttu-id="f2219-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2219-120">Requirement</span></span> | <span data-ttu-id="f2219-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f2219-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2219-122">Header</span><span class="sxs-lookup"><span data-stu-id="f2219-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f2219-123"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2219-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2219-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2219-124">Library</span></span><br/> | <dl> <span data-ttu-id="f2219-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f2219-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2219-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2219-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2219-127">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2219-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




