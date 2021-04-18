---
description: Der Reference \_ time ()-Operator wandelt das Objekt in einen Verweis \_ Zeit Datentyp um.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: REFERENCE_TIME-Methode ("Ref time. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372433"
---
# <a name="creftimeoperator-reference_time-method"></a><span data-ttu-id="deb01-103">Methode zum Aufrufen der Methode "forf time. Operator" \_</span><span class="sxs-lookup"><span data-stu-id="deb01-103">CRefTime.operator REFERENCE\_TIME method</span></span>

<span data-ttu-id="deb01-104">Der- `REFERENCE_TIME()` Operator wandelt das Objekt in einen [**Verweis \_ Zeit**](reference-time.md) Datentyp um.</span><span class="sxs-lookup"><span data-stu-id="deb01-104">The `REFERENCE_TIME()` operator casts the object to a [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="deb01-105">Syntax</span></span>


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a><span data-ttu-id="deb01-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="deb01-106">Parameters</span></span>

<span data-ttu-id="deb01-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="deb01-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="deb01-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="deb01-108">Return value</span></span>

<span data-ttu-id="deb01-109">Gibt den Wert von " [**krefitime:: m \_ time**](creftime-m-time.md)" zurück.</span><span class="sxs-lookup"><span data-stu-id="deb01-109">Returns the value of [**CRefTime::m\_time**](creftime-m-time.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="deb01-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="deb01-110">Remarks</span></span>

<span data-ttu-id="deb01-111">Im folgenden Beispiel wird gezeigt, wie Sie diesen Umwandlungs Operator verwenden:</span><span class="sxs-lookup"><span data-stu-id="deb01-111">The following example shows how to use this cast operator:</span></span>


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a><span data-ttu-id="deb01-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deb01-112">Requirements</span></span>



| <span data-ttu-id="deb01-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="deb01-113">Requirement</span></span> | <span data-ttu-id="deb01-114">Wert</span><span class="sxs-lookup"><span data-stu-id="deb01-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb01-115">Header</span><span class="sxs-lookup"><span data-stu-id="deb01-115">Header</span></span><br/>  | <dl> <span data-ttu-id="deb01-116"><dt>Ref time. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="deb01-116"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="deb01-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="deb01-117">Library</span></span><br/> | <dl> <span data-ttu-id="deb01-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="deb01-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




