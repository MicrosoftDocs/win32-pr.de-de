---
description: Gibt an, ob sich das Objekt seit dem letzten Speichern im aktuellen Stream geändert hat.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Cpersiststream. IsDirty-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370130"
---
# <a name="cpersiststreamisdirty-method"></a><span data-ttu-id="9f024-103">Cpersiststream. IsDirty-Methode</span><span class="sxs-lookup"><span data-stu-id="9f024-103">CPersistStream.IsDirty method</span></span>

<span data-ttu-id="9f024-104">Gibt an, ob sich das Objekt seit dem letzten Speichern im aktuellen Stream geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9f024-104">Indicates whether the object has changed since it was last saved to its current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f024-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f024-105">Syntax</span></span>


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a><span data-ttu-id="9f024-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f024-106">Parameters</span></span>

<span data-ttu-id="9f024-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9f024-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f024-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f024-108">Return value</span></span>

<span data-ttu-id="9f024-109">Gibt s \_ OK zurück, wenn der Filter gespeichert werden muss, und s \_ false, wenn er nicht gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9f024-109">Returns S\_OK if the filter needs saving and S\_FALSE if it does not need saving.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f024-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f024-110">Remarks</span></span>

<span data-ttu-id="9f024-111">Diese Member-Funktion implementiert die **IPersistStream:: IsDirty** -Methode.</span><span class="sxs-lookup"><span data-stu-id="9f024-111">This member function implements the **IPersistStream::IsDirty** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f024-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f024-112">Requirements</span></span>



| <span data-ttu-id="9f024-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f024-113">Requirement</span></span> | <span data-ttu-id="9f024-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9f024-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f024-115">Header</span><span class="sxs-lookup"><span data-stu-id="9f024-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9f024-116"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f024-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f024-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f024-117">Library</span></span><br/> | <dl> <span data-ttu-id="9f024-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9f024-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f024-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f024-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f024-120">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f024-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




