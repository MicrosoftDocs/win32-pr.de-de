---
description: Die DoSetWindowStyle-Methode ändert die typischen oder erweiterten Fensterstile.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: CBaseControlWindow.DoSetWindowStyle-Methode (Ctlutil.h)
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
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909808"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="b4049-103">CBaseControlWindow.DoSetWindowStyle-Methode</span><span class="sxs-lookup"><span data-stu-id="b4049-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="b4049-104">Die `DoSetWindowStyle` -Methode ändert die typischen oder erweiterten Fensterstile.</span><span class="sxs-lookup"><span data-stu-id="b4049-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4049-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4049-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="b4049-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4049-107">*Stil*</span><span class="sxs-lookup"><span data-stu-id="b4049-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="b4049-108">Geeignete Fensterstile.</span><span class="sxs-lookup"><span data-stu-id="b4049-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="b4049-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="b4049-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="b4049-110">Wert, der angibt, welche Stile festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4049-110">Value specifying which styles to set.</span></span> <span data-ttu-id="b4049-111">Dies muss eine der folgenden Ressourcen sein:</span><span class="sxs-lookup"><span data-stu-id="b4049-111">Must be one of the following:</span></span>



| <span data-ttu-id="b4049-112">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="b4049-112">Label</span></span> | <span data-ttu-id="b4049-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b4049-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="b4049-114">\_GWL-STIL</span><span class="sxs-lookup"><span data-stu-id="b4049-114">GWL\_STYLE</span></span>   | <span data-ttu-id="b4049-115">Rufen Sie die Fensterstile ab.</span><span class="sxs-lookup"><span data-stu-id="b4049-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="b4049-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="b4049-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="b4049-117">Rufen Sie die erweiterten Fensterstile ab.</span><span class="sxs-lookup"><span data-stu-id="b4049-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4049-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4049-118">Return value</span></span>

<span data-ttu-id="b4049-119">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="b4049-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4049-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4049-120">Remarks</span></span>

<span data-ttu-id="b4049-121">Diese Memberfunktion ruft die Win32 **SetWindowLong-Funktion** auf, um den Fensterstil festzulegen, und zeigt das Fenster dann erneut an der aktuellen Position an.</span><span class="sxs-lookup"><span data-stu-id="b4049-121">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="b4049-122">Diese Memberfunktion wird von den [**Memberfunktionen CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) und [**CBaseControlWindow::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b4049-122">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4049-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4049-123">Requirements</span></span>



| <span data-ttu-id="b4049-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4049-124">Requirement</span></span> | <span data-ttu-id="b4049-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b4049-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4049-126">Header</span><span class="sxs-lookup"><span data-stu-id="b4049-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b4049-127"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4049-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4049-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4049-128">Library</span></span><br/> | <dl> <span data-ttu-id="b4049-129"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b4049-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4049-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4049-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4049-131">**CBaseControlWindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b4049-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




