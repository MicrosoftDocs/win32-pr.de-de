---
description: Ruft die Anzahl der icontextlink-Objekte in dieser Auflistung ab.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'Icontextlinks:: GetCount-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214671"
---
# <a name="icontextlinksgetcount-method"></a><span data-ttu-id="31d4a-103">Icontextlinks:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="31d4a-103">IContextLinks::GetCount method</span></span>

<span data-ttu-id="31d4a-104">Ruft die Anzahl der [**icontextlink**](icontextlink.md) -Objekte in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="31d4a-104">Gets the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31d4a-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="31d4a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d4a-107">*pulCount* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="31d4a-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="31d4a-108">Die Anzahl der [**icontextlink**](icontextlink.md) -Objekte, die in dieser Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="31d4a-108">The number of [**IContextLink**](icontextlink.md) objects that are contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d4a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31d4a-109">Return value</span></span>

<span data-ttu-id="31d4a-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="31d4a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31d4a-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d4a-111">Requirements</span></span>



| <span data-ttu-id="31d4a-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31d4a-112">Requirement</span></span> | <span data-ttu-id="31d4a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="31d4a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d4a-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31d4a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="31d4a-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d4a-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="31d4a-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31d4a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="31d4a-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="31d4a-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="31d4a-118">Header</span><span class="sxs-lookup"><span data-stu-id="31d4a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d4a-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="31d4a-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="31d4a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="31d4a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d4a-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d4a-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="31d4a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31d4a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d4a-123">**Icontextlinks**</span><span class="sxs-lookup"><span data-stu-id="31d4a-123">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="31d4a-124">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="31d4a-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




