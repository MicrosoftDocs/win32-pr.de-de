---
description: Die iscurrsorhidden-Methode ruft den aktuellen Zustand des m \_ bcurrsorhidden-Datenmembers ab.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Cbasecontrolwindow. iscurrsorhidden-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367146"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a><span data-ttu-id="b1714-103">Cbasecontrolwindow. iscurrsorhidden-Methode</span><span class="sxs-lookup"><span data-stu-id="b1714-103">CBaseControlWindow.IsCursorHidden method</span></span>

<span data-ttu-id="b1714-104">Die- `IsCursorHidden` Methode ruft den aktuellen Zustand des **m \_ bcurrsorhidden** -Datenmembers ab.</span><span class="sxs-lookup"><span data-stu-id="b1714-104">The `IsCursorHidden` method retrieves the current state of the **m\_bCursorHidden** data member.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1714-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1714-105">Syntax</span></span>


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a><span data-ttu-id="b1714-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1714-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1714-107">*Cursor ausgeblendet*</span><span class="sxs-lookup"><span data-stu-id="b1714-107">*CursorHidden*</span></span> 
</dt> <dd>

<span data-ttu-id="b1714-108">Zeiger auf den Wert von **m \_ bcurrsorhidden**.</span><span class="sxs-lookup"><span data-stu-id="b1714-108">Pointer to the value of **m\_bCursorHidden**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1714-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1714-109">Return value</span></span>

<span data-ttu-id="b1714-110">Wenn der Aufruf ohne einen-Parameter erfolgt, wird oatrue zurückgegeben, wenn der Cursor ausgeblendet ist, oder oafalse, wenn der Cursor sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="b1714-110">When called without a parameter, returns OATRUE if the cursor is hidden, or OAFALSE if the cursor is visible.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1714-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1714-111">Remarks</span></span>

<span data-ttu-id="b1714-112">Interne Objekte sollten diese Member-Funktion ohne den " *Cursor Hidden* "-Parameter aufrufen, um zu vermeiden, dass der kritische Abschnitt gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="b1714-112">Internal objects should call this member function without the *CursorHidden* parameter to avoid locking the critical section.</span></span> <span data-ttu-id="b1714-113">Externe Objekte greifen mithilfe des *Cursor* -Parameters über die [**IVideoWindow:: iscurrsorhidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) -Methode auf diese Member-Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="b1714-113">External objects access this member function with the *CursorHidden* parameter through the [**IVideoWindow::IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1714-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1714-114">Requirements</span></span>



| <span data-ttu-id="b1714-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1714-115">Requirement</span></span> | <span data-ttu-id="b1714-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b1714-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1714-117">Header</span><span class="sxs-lookup"><span data-stu-id="b1714-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b1714-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1714-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1714-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1714-119">Library</span></span><br/> | <dl> <span data-ttu-id="b1714-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b1714-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1714-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1714-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1714-122">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b1714-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




