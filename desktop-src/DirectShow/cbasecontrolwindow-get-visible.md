---
description: Die get \_ Visible-Methode ruft die aktuelle Fenster Sichtbarkeit ab.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: CBaseControlWindow.get_Visible-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365775"
---
# <a name="cbasecontrolwindowget_visible-method"></a><span data-ttu-id="314fe-103">Cbasecontrolwindow. get \_ Visible-Methode</span><span class="sxs-lookup"><span data-stu-id="314fe-103">CBaseControlWindow.get\_Visible method</span></span>

<span data-ttu-id="314fe-104">Die- `get_Visible` Methode ruft die aktuelle Fenster Sichtbarkeit ab.</span><span class="sxs-lookup"><span data-stu-id="314fe-104">The `get_Visible` method retrieves the current window visibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="314fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="314fe-105">Syntax</span></span>


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a><span data-ttu-id="314fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="314fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314fe-107">*pvisible*</span><span class="sxs-lookup"><span data-stu-id="314fe-107">*pVisible*</span></span> 
</dt> <dd>

<span data-ttu-id="314fe-108">Zeiger auf ein boolesches Automatisierungs Flag (0 ist off, 1 ist on).</span><span class="sxs-lookup"><span data-stu-id="314fe-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314fe-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="314fe-109">Return value</span></span>

<span data-ttu-id="314fe-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="314fe-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="314fe-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="314fe-111">Remarks</span></span>

<span data-ttu-id="314fe-112">Diese Member-Funktion gibt 1 zurück, wenn das Fenster den \_ sichtbaren WS-Stil aufweist; andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="314fe-112">This member function returns  1 if the window has the WS\_VISIBLE style; 0 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="314fe-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="314fe-113">Requirements</span></span>



| <span data-ttu-id="314fe-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="314fe-114">Requirement</span></span> | <span data-ttu-id="314fe-115">Wert</span><span class="sxs-lookup"><span data-stu-id="314fe-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314fe-116">Header</span><span class="sxs-lookup"><span data-stu-id="314fe-116">Header</span></span><br/>  | <dl> <span data-ttu-id="314fe-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="314fe-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="314fe-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="314fe-118">Library</span></span><br/> | <dl> <span data-ttu-id="314fe-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="314fe-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314fe-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="314fe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314fe-121">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="314fe-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




