---
description: Sucht eine tagübereinstimmung innerhalb des angegebenen übergeordneten Elements und gibt die TagID der ersten Übereinstimmung zurück.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: Sdbfindfirsttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958121"
---
# <a name="sdbfindfirsttag-function"></a><span data-ttu-id="04c6e-103">Sdbfindfirsttag-Funktion</span><span class="sxs-lookup"><span data-stu-id="04c6e-103">SdbFindFirstTag function</span></span>

<span data-ttu-id="04c6e-104">Sucht eine tagübereinstimmung innerhalb des angegebenen übergeordneten Elements und gibt die **TagID** der ersten Übereinstimmung zurück.</span><span class="sxs-lookup"><span data-stu-id="04c6e-104">Searches for a TAG match within the specified parent and returns the **TAGID** of the first match.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04c6e-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a><span data-ttu-id="04c6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04c6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04c6e-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04c6e-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04c6e-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="04c6e-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="04c6e-109">*tiparent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04c6e-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04c6e-110">Die **TagID** des Such Starts.</span><span class="sxs-lookup"><span data-stu-id="04c6e-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="04c6e-111">Dieser Parameter kann eine **TagID \_** -Stamm-oder **\_ Tagtyp \_ Liste** sein.</span><span class="sxs-lookup"><span data-stu-id="04c6e-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="04c6e-112">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04c6e-112">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04c6e-113">Das Tag, das abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="04c6e-113">The TAG to be matched.</span></span> <span data-ttu-id="04c6e-114">Eine Liste möglicher Werte finden Sie unter [Tag](tag.md) .</span><span class="sxs-lookup"><span data-stu-id="04c6e-114">See [TAG](tag.md) for a list of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04c6e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04c6e-115">Return value</span></span>

<span data-ttu-id="04c6e-116">Die **TagID** der ersten Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="04c6e-116">The **TAGID** of the first match.</span></span>

## <a name="requirements"></a><span data-ttu-id="04c6e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04c6e-117">Requirements</span></span>



| <span data-ttu-id="04c6e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04c6e-118">Requirement</span></span> | <span data-ttu-id="04c6e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="04c6e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04c6e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04c6e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04c6e-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04c6e-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04c6e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04c6e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04c6e-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04c6e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04c6e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="04c6e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04c6e-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04c6e-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04c6e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04c6e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04c6e-127">**Sdbfindnexttag**</span><span class="sxs-lookup"><span data-stu-id="04c6e-127">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="04c6e-128">**Sdbtagrebtotagid**</span><span class="sxs-lookup"><span data-stu-id="04c6e-128">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




