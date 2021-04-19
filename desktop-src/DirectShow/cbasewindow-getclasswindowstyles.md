---
description: Die getclasswindowstyles-Methode ruft die Klassen Stile und Fenster Stile des Fensters ab.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Cbasewindow. getclasswindowstyles-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370084"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a><span data-ttu-id="59856-103">Cbasewindow. getclasswindowstyles-Methode</span><span class="sxs-lookup"><span data-stu-id="59856-103">CBaseWindow.GetClassWindowStyles method</span></span>

<span data-ttu-id="59856-104">Die `GetClassWindowStyles` -Methode ruft die Klassen Stile und Fenster Stile des Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="59856-104">The `GetClassWindowStyles` method retrieves the window's class styles and window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="59856-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59856-105">Syntax</span></span>


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="59856-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59856-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59856-107">*pclassstyles*</span><span class="sxs-lookup"><span data-stu-id="59856-107">*pClassStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="59856-108">Ein Zeiger auf eine Variable, die die Klassen Stile empfängt.</span><span class="sxs-lookup"><span data-stu-id="59856-108">Pointer to a variable that receives the class styles.</span></span>

</dd> <dt>

<span data-ttu-id="59856-109">*pwindowstyles*</span><span class="sxs-lookup"><span data-stu-id="59856-109">*pWindowStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="59856-110">Ein Zeiger auf eine Variable, die die Fenster Stile empfängt.</span><span class="sxs-lookup"><span data-stu-id="59856-110">Pointer to a variable that receives the window styles.</span></span>

</dd> <dt>

<span data-ttu-id="59856-111">*pwindowstylesex*</span><span class="sxs-lookup"><span data-stu-id="59856-111">*pWindowStylesEx*</span></span> 
</dt> <dd>

<span data-ttu-id="59856-112">Ein Zeiger auf eine Variable, die die erweiterten Fenster Stile empfängt.</span><span class="sxs-lookup"><span data-stu-id="59856-112">Pointer to a variable that receives the extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59856-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59856-113">Return value</span></span>

<span data-ttu-id="59856-114">Gibt eine statische Text Zeichenfolge zurück, die den Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="59856-114">Returns a static text string that contains the class name.</span></span>

## <a name="remarks"></a><span data-ttu-id="59856-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59856-115">Remarks</span></span>

<span data-ttu-id="59856-116">Die [**cbasewindow::P Analyse Window**](cbasewindow-preparewindow.md) -Methode ruft diese Methode auf, um die Klassen Stile und Fenster Stile des Fensters abzurufen.</span><span class="sxs-lookup"><span data-stu-id="59856-116">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method to retrieve the window's class styles and window styles.</span></span>

<span data-ttu-id="59856-117">Diese Methode ist rein virtuell. Diese Klasse muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="59856-117">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="59856-118">Das folgende Beispiel zeigt eine mögliche Implementierung:</span><span class="sxs-lookup"><span data-stu-id="59856-118">The following example shows a possible implementation:</span></span>


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



<span data-ttu-id="59856-119">Das-Objekt verwendet den Klassen Stil für den **lpszClassName** -Member einer WNDCLASS-Struktur, die an die **registerClass** -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="59856-119">The object uses the class style for the **lpszClassName** member of a WNDCLASS structure, which it passes to the **RegisterClass** function.</span></span> <span data-ttu-id="59856-120">Das-Objekt verwendet die Fenster Stile für den *dwExStyle* -Parameter und den *dwstyle* -Parameter **der Funktion "** -Funktion".</span><span class="sxs-lookup"><span data-stu-id="59856-120">The object uses the window styles for the *dwExStyle* and *dwStyle* parameters of the **CreateWindowEx** function.</span></span> <span data-ttu-id="59856-121">Weitere Informationen finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="59856-121">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="59856-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59856-122">Requirements</span></span>



| <span data-ttu-id="59856-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59856-123">Requirement</span></span> | <span data-ttu-id="59856-124">Wert</span><span class="sxs-lookup"><span data-stu-id="59856-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59856-125">Header</span><span class="sxs-lookup"><span data-stu-id="59856-125">Header</span></span><br/>  | <dl> <span data-ttu-id="59856-126"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59856-126"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59856-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59856-127">Library</span></span><br/> | <dl> <span data-ttu-id="59856-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="59856-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59856-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59856-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59856-130">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="59856-130">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




