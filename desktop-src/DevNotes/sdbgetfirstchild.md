---
description: Sucht nach einem untergeordneten Tag innerhalb des angegebenen übergeordneten Elements und gibt die TagID des ersten untergeordneten Elements zurück.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Sdbgetfirstchild-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522803"
---
# <a name="sdbgetfirstchild-function"></a><span data-ttu-id="0370a-103">Sdbgetfirstchild-Funktion</span><span class="sxs-lookup"><span data-stu-id="0370a-103">SdbGetFirstChild function</span></span>

<span data-ttu-id="0370a-104">Sucht nach einem untergeordneten Tag innerhalb des angegebenen übergeordneten Elements und gibt die **TagID** des ersten untergeordneten Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="0370a-104">Searches for a child TAG within the specified parent and returns the **TAGID** of the first child.</span></span>

## <a name="syntax"></a><span data-ttu-id="0370a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0370a-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a><span data-ttu-id="0370a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0370a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0370a-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0370a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0370a-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0370a-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0370a-109">*tiparent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0370a-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0370a-110">Die **TagID** des Such Starts.</span><span class="sxs-lookup"><span data-stu-id="0370a-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="0370a-111">Dieser Parameter kann eine **TagID \_** -Stamm-oder **\_ Tagtyp \_ Liste** sein.</span><span class="sxs-lookup"><span data-stu-id="0370a-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0370a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0370a-112">Return value</span></span>

<span data-ttu-id="0370a-113">Die **TagID** des ersten untergeordneten Elements oder **TagID \_ null** ist kein untergeordnetes Element wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0370a-113">The **TAGID** of the first child or **TAGID\_NULL** is no child is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="0370a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0370a-114">Requirements</span></span>



| <span data-ttu-id="0370a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0370a-115">Requirement</span></span> | <span data-ttu-id="0370a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0370a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0370a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0370a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0370a-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0370a-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0370a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0370a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0370a-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0370a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0370a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0370a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0370a-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0370a-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0370a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0370a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0370a-124">**Sdbfindfirsttag**</span><span class="sxs-lookup"><span data-stu-id="0370a-124">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="0370a-125">**Sdbfindnexttag**</span><span class="sxs-lookup"><span data-stu-id="0370a-125">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="0370a-126">**Sdbgetnextchild**</span><span class="sxs-lookup"><span data-stu-id="0370a-126">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
</dt> </dl>

 

 




