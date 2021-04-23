---
description: Die DoGetWindowStyle-Methode ruft die aktuellen normalen oder erweiterten Fensterstile ab.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: CBaseControlWindow.DoGetWindowStyle-Methode (Ctlutil.h)
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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909818"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="a8a55-103">CBaseControlWindow.DoGetWindowStyle-Methode</span><span class="sxs-lookup"><span data-stu-id="a8a55-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="a8a55-104">Die `DoGetWindowStyle` -Methode ruft die aktuellen normalen oder erweiterten Fensterstile ab.</span><span class="sxs-lookup"><span data-stu-id="a8a55-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8a55-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="a8a55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8a55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a55-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="a8a55-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a55-108">Zeiger auf eine Variable, die die Formatinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a8a55-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="a8a55-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="a8a55-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a55-110">Wert, der an gibt, welche Stile abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a8a55-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="a8a55-111">Dies muss eine der folgenden Ressourcen sein:</span><span class="sxs-lookup"><span data-stu-id="a8a55-111">Must be one of the following:</span></span>



| <span data-ttu-id="a8a55-112">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="a8a55-112">Label</span></span> | <span data-ttu-id="a8a55-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a55-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="a8a55-114">\_GWL-STIL</span><span class="sxs-lookup"><span data-stu-id="a8a55-114">GWL\_STYLE</span></span>   | <span data-ttu-id="a8a55-115">Rufen Sie die Fensterstile ab.</span><span class="sxs-lookup"><span data-stu-id="a8a55-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="a8a55-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="a8a55-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="a8a55-117">Rufen Sie die erweiterten Fensterstile ab.</span><span class="sxs-lookup"><span data-stu-id="a8a55-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a55-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8a55-118">Return value</span></span>

<span data-ttu-id="a8a55-119">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="a8a55-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8a55-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8a55-120">Remarks</span></span>

<span data-ttu-id="a8a55-121">Diese Memberfunktion ruft die Win32 **GetWindowLong-Funktion** auf, um den Fensterstil abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8a55-121">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="a8a55-122">Sie wird von den [**Memberfunktionen CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) und [**CBaseControlWindow::get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a8a55-122">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a55-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8a55-123">Requirements</span></span>



| <span data-ttu-id="a8a55-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8a55-124">Requirement</span></span> | <span data-ttu-id="a8a55-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a55-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a55-126">Header</span><span class="sxs-lookup"><span data-stu-id="a8a55-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a8a55-127"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8a55-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8a55-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8a55-128">Library</span></span><br/> | <dl> <span data-ttu-id="a8a55-129"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a8a55-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8a55-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8a55-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a55-131">**CBaseControlWindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a8a55-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




