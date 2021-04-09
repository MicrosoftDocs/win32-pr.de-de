---
description: Sucht das nächste untergeordnete Tag innerhalb des angegebenen übergeordneten Elements und gibt die TagID des nächsten untergeordneten Elements zurück.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Sdbgetnextchild-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861048"
---
# <a name="sdbgetnextchild-function"></a><span data-ttu-id="57ba1-103">Sdbgetnextchild-Funktion</span><span class="sxs-lookup"><span data-stu-id="57ba1-103">SdbGetNextChild function</span></span>

<span data-ttu-id="57ba1-104">Sucht das nächste untergeordnete Tag innerhalb des angegebenen übergeordneten Elements und gibt die **TagID** des nächsten untergeordneten Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="57ba1-104">Searches for the next child TAG within the specified parent and returns the **TAGID** of the next child.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ba1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57ba1-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="57ba1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57ba1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ba1-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57ba1-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ba1-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="57ba1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="57ba1-109">*tiparent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57ba1-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ba1-110">Die **TagID** des Such Starts.</span><span class="sxs-lookup"><span data-stu-id="57ba1-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="57ba1-111">Dieser Parameter kann eine **TagID \_** -Stamm-oder **\_ Tagtyp \_ Liste** sein.</span><span class="sxs-lookup"><span data-stu-id="57ba1-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="57ba1-112">*tiprev* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57ba1-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ba1-113">Die **TagID** des vorherigen untergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="57ba1-113">The **TAGID** of the previous child.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ba1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57ba1-114">Return value</span></span>

<span data-ttu-id="57ba1-115">Die **TagID** des untergeordneten Elements oder der **TagID \_ null** , wenn kein untergeordnetes Element gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="57ba1-115">The **TAGID** of the child or **TAGID\_NULL** if no child is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="57ba1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57ba1-116">Remarks</span></span>

<span data-ttu-id="57ba1-117">Bevor Sie diese Funktion aufrufen, rufen Sie die [**sdbgetfirstchild**](sdbgetfirstchild.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="57ba1-117">Before calling this function, call the [**SdbGetFirstChild**](sdbgetfirstchild.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ba1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57ba1-118">Requirements</span></span>



| <span data-ttu-id="57ba1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57ba1-119">Requirement</span></span> | <span data-ttu-id="57ba1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="57ba1-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57ba1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57ba1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57ba1-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57ba1-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="57ba1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57ba1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57ba1-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57ba1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="57ba1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="57ba1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57ba1-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ba1-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ba1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57ba1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ba1-128">**Sdbfindfirsttag**</span><span class="sxs-lookup"><span data-stu-id="57ba1-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="57ba1-129">**Sdbfindnexttag**</span><span class="sxs-lookup"><span data-stu-id="57ba1-129">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="57ba1-130">**Sdbgetfirstchild**</span><span class="sxs-lookup"><span data-stu-id="57ba1-130">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
</dt> </dl>

 

 




