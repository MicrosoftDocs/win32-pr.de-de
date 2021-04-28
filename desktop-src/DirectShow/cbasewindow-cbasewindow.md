---
description: 'CBaseWindow.CBaseWindow-Konstruktor : Konstruktormethode.'
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: CBaseWindow.CBaseWindow-Konstruktor (Winutil.h)
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
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095818"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="c54f6-103">CBaseWindow.CBaseWindow-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="c54f6-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="c54f6-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="c54f6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c54f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c54f6-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="c54f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c54f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c54f6-107">*bDoGetDC*</span><span class="sxs-lookup"><span data-stu-id="c54f6-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="c54f6-108">Boolescher Wert, der angibt, ob der Gerätekontext abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c54f6-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="c54f6-109">*bPostToDestroy*</span><span class="sxs-lookup"><span data-stu-id="c54f6-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="c54f6-110">Boolescher Wert, der die [**Membervariable CBaseWindow::m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) angibt.</span><span class="sxs-lookup"><span data-stu-id="c54f6-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c54f6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c54f6-111">Remarks</span></span>

<span data-ttu-id="c54f6-112">Nachdem Sie das -Objekt erstellt haben, rufen Sie die [**CBaseWindow::P repareWindow-Methode**](cbasewindow-preparewindow.md) auf, um das Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c54f6-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="c54f6-113">**PrepareWindow** ist eine virtuelle Methode.</span><span class="sxs-lookup"><span data-stu-id="c54f6-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="c54f6-114">Sie ruft [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md)auf, ebenfalls eine virtuelle Methode.</span><span class="sxs-lookup"><span data-stu-id="c54f6-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="c54f6-115">Diese Methoden werden vom Konstruktor getrennt, sodass abgeleitete Klassen sie bei Bedarf überschreiben können.</span><span class="sxs-lookup"><span data-stu-id="c54f6-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="c54f6-116">Wenn der Wert des *bDoGetDC-Parameters* **TRUE** ist, ruft das `CBaseWindow` -Objekt ein Handle für den Gerätekontext (DC) des Fensters ab und speichert es in der [**CBaseWindow::m \_ hdc-Membervariablen.**](cbasewindow-m-hdc.md)</span><span class="sxs-lookup"><span data-stu-id="c54f6-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="c54f6-117">Das -Objekt erstellt auch einen kompatiblen Speicherdomänencontroller, der in der [**Membervariablen CBaseWindow::m \_ MemoryDC**](cbasewindow-m-memorydc.md) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c54f6-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="c54f6-118">Diese Aktionen treten in der **InitialiseWindow-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="c54f6-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c54f6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c54f6-119">Requirements</span></span>



| <span data-ttu-id="c54f6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c54f6-120">Requirement</span></span> | <span data-ttu-id="c54f6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c54f6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c54f6-122">Header</span><span class="sxs-lookup"><span data-stu-id="c54f6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c54f6-123"><dt>Winutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c54f6-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c54f6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c54f6-124">Library</span></span><br/> | <dl> <span data-ttu-id="c54f6-125"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c54f6-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c54f6-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c54f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c54f6-127">**CBaseWindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c54f6-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




