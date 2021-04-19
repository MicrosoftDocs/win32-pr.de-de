---
description: Die breakconnect-Methode gibt die Eingabe-PIN von einer Verbindung frei.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Cbaserderderer. breakconnect-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366746"
---
# <a name="cbaserendererbreakconnect-method"></a><span data-ttu-id="f6627-103">Cbaserderderer. breakconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="f6627-103">CBaseRenderer.BreakConnect method</span></span>

<span data-ttu-id="f6627-104">Die- `BreakConnect` Methode gibt die Eingabe-PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="f6627-104">The `BreakConnect` method releases the input pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6627-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6627-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="f6627-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6627-106">Parameters</span></span>

<span data-ttu-id="f6627-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f6627-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6627-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6627-108">Return value</span></span>

<span data-ttu-id="f6627-109">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f6627-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f6627-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f6627-110">Return code</span></span>                                                                                         | <span data-ttu-id="f6627-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6627-111">Description</span></span>                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="f6627-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f6627-112"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="f6627-113">Die PIN war nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="f6627-113">The pin was not connected.</span></span><br/>  |
| <dl> <span data-ttu-id="f6627-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f6627-114"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="f6627-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f6627-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="f6627-116"><dt>**VFW \_ E \_ nicht \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="f6627-116"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="f6627-117">Der Filter ist noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="f6627-117">The filter is still active.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6627-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6627-118">Remarks</span></span>

<span data-ttu-id="f6627-119">Die Eingabe-PIN des Filters ruft diese Methode in der eigenen `BreakConnect` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f6627-119">The filter's input pin calls this method from inside its own `BreakConnect` method.</span></span> <span data-ttu-id="f6627-120">(Weitere Informationen finden Sie unter [**cbasepin:: breakconnect**](cbasepin-breakconnect.md).) Der Filter führt eine interne Buchhaltung aus, z. b. das Flag für das Ende des Streams zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="f6627-120">(For more information, see [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) The filter performs some internal bookkeeping, such as resetting the end-of-stream flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6627-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6627-121">Requirements</span></span>



| <span data-ttu-id="f6627-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6627-122">Requirement</span></span> | <span data-ttu-id="f6627-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f6627-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6627-124">Header</span><span class="sxs-lookup"><span data-stu-id="f6627-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f6627-125"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6627-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6627-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6627-126">Library</span></span><br/> | <dl> <span data-ttu-id="f6627-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f6627-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6627-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6627-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6627-129">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6627-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




