---
description: Die hidecursor-Methode blendet den Cursor aus oder zeigt ihn an.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Cbasecontrolwindow. hidecursor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367082"
---
# <a name="cbasecontrolwindowhidecursor-method"></a><span data-ttu-id="902f2-103">Cbasecontrolwindow. hidecursor-Methode</span><span class="sxs-lookup"><span data-stu-id="902f2-103">CBaseControlWindow.HideCursor method</span></span>

<span data-ttu-id="902f2-104">Mit der- `HideCursor` Methode wird der Cursor ausgeblendet oder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="902f2-104">The `HideCursor` method hides or displays the cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="902f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="902f2-105">Syntax</span></span>


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a><span data-ttu-id="902f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="902f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="902f2-107">*Hidecursor*</span><span class="sxs-lookup"><span data-stu-id="902f2-107">*HideCursor*</span></span> 
</dt> <dd>

<span data-ttu-id="902f2-108">Wert, der angibt, ob der Cursor angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="902f2-108">Value specifying whether to show the cursor.</span></span> <span data-ttu-id="902f2-109">Legen Sie fest, um den Cursor auszublenden, oder oafalse, um den Cursor anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="902f2-109">Set to OATRUE to hide the cursor, or OAFALSE to display the cursor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="902f2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="902f2-110">Return value</span></span>

<span data-ttu-id="902f2-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="902f2-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="902f2-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="902f2-112">Requirements</span></span>



| <span data-ttu-id="902f2-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="902f2-113">Requirement</span></span> | <span data-ttu-id="902f2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="902f2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="902f2-115">Header</span><span class="sxs-lookup"><span data-stu-id="902f2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="902f2-116"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="902f2-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="902f2-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="902f2-117">Library</span></span><br/> | <dl> <span data-ttu-id="902f2-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="902f2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="902f2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="902f2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="902f2-120">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="902f2-120">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




