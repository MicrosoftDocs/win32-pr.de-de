---
description: Deaktiviert die Indexerstellung und-Änderung für die angegebene Datenbank.
ms.assetid: d079eae2-574e-4ac1-a0f9-11796e56a790
title: Sdbstopindizierungs-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStopIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3c9c6b34c265d611b57a3e73bb0c8fb1822fe752
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523328"
---
# <a name="sdbstopindexing-function"></a><span data-ttu-id="5d051-103">Sdbstopindizierungs-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d051-103">SdbStopIndexing function</span></span>

<span data-ttu-id="5d051-104">Deaktiviert die Indexerstellung und-Änderung für die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5d051-104">Disables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d051-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d051-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStopIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="5d051-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d051-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d051-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d051-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d051-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="5d051-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="5d051-109">*iiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d051-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d051-110">Der Indexbezeichner</span><span class="sxs-lookup"><span data-stu-id="5d051-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d051-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d051-111">Return value</span></span>

<span data-ttu-id="5d051-112">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="5d051-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d051-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d051-113">Requirements</span></span>



| <span data-ttu-id="5d051-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d051-114">Requirement</span></span> | <span data-ttu-id="5d051-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5d051-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d051-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d051-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5d051-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d051-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5d051-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d051-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5d051-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d051-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5d051-120">DLL</span><span class="sxs-lookup"><span data-stu-id="5d051-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d051-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d051-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d051-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d051-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d051-123">**Sdbcommitindexes**</span><span class="sxs-lookup"><span data-stu-id="5d051-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="5d051-124">**Sdbdeclareingedex**</span><span class="sxs-lookup"><span data-stu-id="5d051-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="5d051-125">**Sdbstartindizierung**</span><span class="sxs-lookup"><span data-stu-id="5d051-125">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> </dl>

 

 




