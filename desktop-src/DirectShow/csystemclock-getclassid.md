---
description: 'Die GetClassID-Methode ruft den Klassen Bezeichner (CLSID) des-Objekts ab. Diese Methode implementiert die ipersistent:: GetClassID-Methode.'
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Csystemclock. GetClassID-Methode (sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365845"
---
# <a name="csystemclockgetclassid-method"></a><span data-ttu-id="26f07-104">Csystemclock. GetClassID-Methode</span><span class="sxs-lookup"><span data-stu-id="26f07-104">CSystemClock.GetClassID method</span></span>

<span data-ttu-id="26f07-105">Die- `GetClassID` Methode ruft den Klassen Bezeichner (CLSID) des-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="26f07-105">The `GetClassID` method retrieves the class identifier (CLSID) of the object.</span></span> <span data-ttu-id="26f07-106">Diese Methode implementiert die **ipersistent:: GetClassID-** Methode.</span><span class="sxs-lookup"><span data-stu-id="26f07-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f07-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f07-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="26f07-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26f07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f07-109">*pclsid*</span><span class="sxs-lookup"><span data-stu-id="26f07-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="26f07-110">Ein Zeiger auf eine Variable, die den Wert CLSID \_ systemclock empfängt.</span><span class="sxs-lookup"><span data-stu-id="26f07-110">Pointer to a variable that receives the value CLSID\_SystemClock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f07-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26f07-111">Return value</span></span>

<span data-ttu-id="26f07-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="26f07-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f07-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f07-113">Requirements</span></span>



| <span data-ttu-id="26f07-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26f07-114">Requirement</span></span> | <span data-ttu-id="26f07-115">Wert</span><span class="sxs-lookup"><span data-stu-id="26f07-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f07-116">Version</span><span class="sxs-lookup"><span data-stu-id="26f07-116">Version</span></span><br/> | <span data-ttu-id="26f07-117">Csystemclock-Klasse</span><span class="sxs-lookup"><span data-stu-id="26f07-117">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="26f07-118">Header</span><span class="sxs-lookup"><span data-stu-id="26f07-118">Header</span></span><br/>  | <dl> <span data-ttu-id="26f07-119"><dt>Sysclock. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26f07-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="26f07-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26f07-120">Library</span></span><br/> | <dl> <span data-ttu-id="26f07-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="26f07-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




