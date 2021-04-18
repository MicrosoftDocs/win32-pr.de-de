---
description: Die Methode "dosetwindowstyle" ändert die typischen oder erweiterten Fenster Stile.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Cbasecontrolwindow. dosetwindowstyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364831"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="54f88-103">Cbasecontrolwindow. dosetwindowstyle-Methode</span><span class="sxs-lookup"><span data-stu-id="54f88-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="54f88-104">Die- `DoSetWindowStyle` Methode ändert die typischen oder erweiterten Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="54f88-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="54f88-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54f88-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="54f88-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54f88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54f88-107">*Stil*</span><span class="sxs-lookup"><span data-stu-id="54f88-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="54f88-108">Geeignete Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="54f88-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="54f88-109">*Windowlong*</span><span class="sxs-lookup"><span data-stu-id="54f88-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="54f88-110">Wert, der angibt, welche Stile festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="54f88-110">Value specifying which styles to set.</span></span> <span data-ttu-id="54f88-111">Dies muss eine der folgenden Ressourcen sein:</span><span class="sxs-lookup"><span data-stu-id="54f88-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="54f88-112">GWL- \_ Stil</span><span class="sxs-lookup"><span data-stu-id="54f88-112">GWL\_STYLE</span></span>   | <span data-ttu-id="54f88-113">Abrufen der Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="54f88-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="54f88-114">GWL- \_ ExStyle</span><span class="sxs-lookup"><span data-stu-id="54f88-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="54f88-115">Ruft die erweiterten Fenster Stile ab.</span><span class="sxs-lookup"><span data-stu-id="54f88-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54f88-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54f88-116">Return value</span></span>

<span data-ttu-id="54f88-117">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54f88-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54f88-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54f88-118">Remarks</span></span>

<span data-ttu-id="54f88-119">Diese Member-Funktion Ruft die Win32-Funktion **SetWindowLong** auf, um den Fenster Stil festzulegen, und zeigt dann das Fenster an der aktuellen Position erneut an.</span><span class="sxs-lookup"><span data-stu-id="54f88-119">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="54f88-120">Diese Member-Funktion wird durch das [**cbasecontrolwindow::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) -und [**cbasecontrolwindow::p UT \_ windowstyleex**](cbasecontrolwindow-put-windowstyleex.md) -Member-Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="54f88-120">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="54f88-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54f88-121">Requirements</span></span>



| <span data-ttu-id="54f88-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54f88-122">Requirement</span></span> | <span data-ttu-id="54f88-123">Wert</span><span class="sxs-lookup"><span data-stu-id="54f88-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f88-124">Header</span><span class="sxs-lookup"><span data-stu-id="54f88-124">Header</span></span><br/>  | <dl> <span data-ttu-id="54f88-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54f88-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="54f88-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54f88-126">Library</span></span><br/> | <dl> <span data-ttu-id="54f88-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="54f88-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54f88-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54f88-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f88-129">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="54f88-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




