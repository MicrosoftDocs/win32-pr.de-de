---
description: Dieser Operator Fügt zwei Verweis Zeiten hinzu.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Coaref time. Operator +-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a6f5019c61d4c1baec47652db8842aa5085b675
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371649"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="5e9ec-103">Coaref time. Operator +-Methode</span><span class="sxs-lookup"><span data-stu-id="5e9ec-103">COARefTime.operator+ method</span></span>

<span data-ttu-id="5e9ec-104">Dieser Operator Fügt zwei Verweis Zeiten hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e9ec-104">This operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e9ec-105">Syntax</span></span>


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="5e9ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e9ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e9ec-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="5e9ec-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5e9ec-108">Verweis auf das hinzu zufügende **coareftime** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5e9ec-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e9ec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e9ec-109">Return value</span></span>

<span data-ttu-id="5e9ec-110">Gibt ein neues **coareftime** -Objekt zurück, das gleich der Summe der Verweis Zeiten ist.</span><span class="sxs-lookup"><span data-stu-id="5e9ec-110">Returns a new **COARefTime** object equal to the sum of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9ec-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e9ec-111">Requirements</span></span>



| <span data-ttu-id="5e9ec-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e9ec-112">Requirement</span></span> | <span data-ttu-id="5e9ec-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5e9ec-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9ec-114">Header</span><span class="sxs-lookup"><span data-stu-id="5e9ec-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5e9ec-115"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e9ec-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e9ec-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e9ec-116">Library</span></span><br/> | <dl> <span data-ttu-id="5e9ec-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5e9ec-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9ec-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e9ec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9ec-119">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5e9ec-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




