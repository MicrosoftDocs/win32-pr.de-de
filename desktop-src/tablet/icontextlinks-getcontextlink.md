---
description: Ruft den icontextlink am angegebenen Index ab.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'Icontextlinks:: getcontextlink-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129509"
---
# <a name="icontextlinksgetcontextlink-method"></a><span data-ttu-id="4ea2e-103">Icontextlinks:: getcontextlink-Methode</span><span class="sxs-lookup"><span data-stu-id="4ea2e-103">IContextLinks::GetContextLink method</span></span>

<span data-ttu-id="4ea2e-104">Ruft den [**icontextlink**](icontextlink.md) am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="4ea2e-104">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea2e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ea2e-105">Syntax</span></span>


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a><span data-ttu-id="4ea2e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ea2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ea2e-107">*ulindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ea2e-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ea2e-108">Der null basierte Index des abzurufenden [**icontextlink**](icontextlink.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ea2e-108">The zero-based index of the [**IContextLink**](icontextlink.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="4ea2e-109">*ppcontextlink* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4ea2e-109">*ppContextLink* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ea2e-110">Ein Zeiger auf das [**icontextlink**](icontextlink.md) -Objekt am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="4ea2e-110">A pointer to the [**IContextLink**](icontextlink.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ea2e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ea2e-111">Return value</span></span>

<span data-ttu-id="4ea2e-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4ea2e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea2e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ea2e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4ea2e-114">Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextlink* abrufen, wenn Sie den Kontext Link nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="4ea2e-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLink* when you no longer need to use the context link.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ea2e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ea2e-115">Requirements</span></span>



| <span data-ttu-id="4ea2e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ea2e-116">Requirement</span></span> | <span data-ttu-id="4ea2e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4ea2e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea2e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ea2e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4ea2e-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ea2e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ea2e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ea2e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4ea2e-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4ea2e-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4ea2e-122">Header</span><span class="sxs-lookup"><span data-stu-id="4ea2e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ea2e-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4ea2e-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4ea2e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4ea2e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ea2e-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ea2e-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4ea2e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ea2e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea2e-127">**Icontextlinks**</span><span class="sxs-lookup"><span data-stu-id="4ea2e-127">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="4ea2e-128">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="4ea2e-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4ea2e-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4ea2e-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

