---
description: Die dogetwindowstyle-Methode ruft die aktuellen normalen oder erweiterten Fenster Stile ab.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Cbasecontrolwindow. dogetwindowstyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367022"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="a48fd-103">Cbasecontrolwindow. dogetwindowstyle-Methode</span><span class="sxs-lookup"><span data-stu-id="a48fd-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="a48fd-104">Die- `DoGetWindowStyle` Methode ruft die aktuellen normalen oder erweiterten Fenster Stile ab.</span><span class="sxs-lookup"><span data-stu-id="a48fd-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="a48fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a48fd-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="a48fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a48fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a48fd-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="a48fd-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="a48fd-108">Ein Zeiger auf eine Variable, die die Stil Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a48fd-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="a48fd-109">*Windowlong*</span><span class="sxs-lookup"><span data-stu-id="a48fd-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="a48fd-110">Ein Wert, der angibt, welche Stile abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a48fd-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="a48fd-111">Dies muss eine der folgenden Ressourcen sein:</span><span class="sxs-lookup"><span data-stu-id="a48fd-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="a48fd-112">GWL- \_ Stil</span><span class="sxs-lookup"><span data-stu-id="a48fd-112">GWL\_STYLE</span></span>   | <span data-ttu-id="a48fd-113">Abrufen der Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="a48fd-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="a48fd-114">GWL- \_ ExStyle</span><span class="sxs-lookup"><span data-stu-id="a48fd-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="a48fd-115">Ruft die erweiterten Fenster Stile ab.</span><span class="sxs-lookup"><span data-stu-id="a48fd-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a48fd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a48fd-116">Return value</span></span>

<span data-ttu-id="a48fd-117">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a48fd-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a48fd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a48fd-118">Remarks</span></span>

<span data-ttu-id="a48fd-119">Diese Member-Funktion Ruft die Win32 **GetWindowLong** -Funktion auf, um den Fenster Stil abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a48fd-119">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="a48fd-120">Sie wird von den Element Funktionen [**cbasecontrolwindow:: get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) und [**cbasecontrolwindow:: get \_ windowstyleex**](cbasecontrolwindow-get-windowstyleex.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a48fd-120">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a48fd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a48fd-121">Requirements</span></span>



| <span data-ttu-id="a48fd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a48fd-122">Requirement</span></span> | <span data-ttu-id="a48fd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a48fd-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48fd-124">Header</span><span class="sxs-lookup"><span data-stu-id="a48fd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a48fd-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a48fd-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a48fd-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a48fd-126">Library</span></span><br/> | <dl> <span data-ttu-id="a48fd-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a48fd-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a48fd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a48fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48fd-129">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a48fd-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




