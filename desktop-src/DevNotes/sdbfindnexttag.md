---
description: Sucht im angegebenen übergeordneten Element nach der nächsten tagübereinstimmung und gibt die TagID der Übereinstimmung zurück.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Sdbfindnexttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860892"
---
# <a name="sdbfindnexttag-function"></a><span data-ttu-id="22c84-103">Sdbfindnexttag-Funktion</span><span class="sxs-lookup"><span data-stu-id="22c84-103">SdbFindNextTag function</span></span>

<span data-ttu-id="22c84-104">Sucht im angegebenen übergeordneten Element nach der nächsten tagübereinstimmung und gibt die **TagID** der Übereinstimmung zurück.</span><span class="sxs-lookup"><span data-stu-id="22c84-104">Searches for the next TAG match within the specified parent and returns the **TAGID** of the match.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22c84-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="22c84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c84-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22c84-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c84-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="22c84-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="22c84-109">*tiparent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22c84-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c84-110">Die **TagID** des Such Starts.</span><span class="sxs-lookup"><span data-stu-id="22c84-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="22c84-111">Dieser Parameter kann eine **TagID \_** -Stamm-oder **\_ Tagtyp \_ Liste** sein.</span><span class="sxs-lookup"><span data-stu-id="22c84-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="22c84-112">*tiprev* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22c84-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c84-113">Die **TagID** der vorherigen Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="22c84-113">The **TAGID** of the previous match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c84-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22c84-114">Return value</span></span>

<span data-ttu-id="22c84-115">Die **TagID** der Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="22c84-115">The **TAGID** of the match.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c84-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22c84-116">Remarks</span></span>

<span data-ttu-id="22c84-117">Bevor Sie diese Funktion aufrufen, rufen Sie die [**sdbfindfirsttag**](sdbfindfirsttag.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="22c84-117">Before calling this function, call the [**SdbFindFirstTag**](sdbfindfirsttag.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c84-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22c84-118">Requirements</span></span>



| <span data-ttu-id="22c84-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22c84-119">Requirement</span></span> | <span data-ttu-id="22c84-120">Wert</span><span class="sxs-lookup"><span data-stu-id="22c84-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22c84-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22c84-121">Minimum supported client</span></span><br/> | <span data-ttu-id="22c84-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22c84-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="22c84-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22c84-123">Minimum supported server</span></span><br/> | <span data-ttu-id="22c84-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22c84-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="22c84-125">DLL</span><span class="sxs-lookup"><span data-stu-id="22c84-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22c84-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c84-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c84-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22c84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c84-128">**Sdbfindfirsttag**</span><span class="sxs-lookup"><span data-stu-id="22c84-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="22c84-129">**Sdbtagrebtotagid**</span><span class="sxs-lookup"><span data-stu-id="22c84-129">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




