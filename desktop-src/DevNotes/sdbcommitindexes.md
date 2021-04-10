---
description: Führt einen Commit für neu erstellte Indizes zur angegebenen Datenbank aus.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: Sdbcommitindexes-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126170"
---
# <a name="sdbcommitindexes-function"></a><span data-ttu-id="090ae-103">Sdbcommitindexes-Funktion</span><span class="sxs-lookup"><span data-stu-id="090ae-103">SdbCommitIndexes function</span></span>

<span data-ttu-id="090ae-104">Führt einen Commit für neu erstellte Indizes zur angegebenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="090ae-104">Commits newly created indexes to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="090ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="090ae-105">Syntax</span></span>


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="090ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="090ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090ae-107">*PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="090ae-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="090ae-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="090ae-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090ae-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="090ae-109">Return value</span></span>

<span data-ttu-id="090ae-110">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="090ae-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="090ae-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="090ae-111">Requirements</span></span>



| <span data-ttu-id="090ae-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="090ae-112">Requirement</span></span> | <span data-ttu-id="090ae-113">Wert</span><span class="sxs-lookup"><span data-stu-id="090ae-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="090ae-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="090ae-114">Minimum supported client</span></span><br/> | <span data-ttu-id="090ae-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="090ae-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="090ae-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="090ae-116">Minimum supported server</span></span><br/> | <span data-ttu-id="090ae-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="090ae-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="090ae-118">DLL</span><span class="sxs-lookup"><span data-stu-id="090ae-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="090ae-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="090ae-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="090ae-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="090ae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090ae-121">**Sdbdeclareingedex**</span><span class="sxs-lookup"><span data-stu-id="090ae-121">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="090ae-122">**Sdbstartindizierung**</span><span class="sxs-lookup"><span data-stu-id="090ae-122">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="090ae-123">**Sdbstopindizierung**</span><span class="sxs-lookup"><span data-stu-id="090ae-123">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




