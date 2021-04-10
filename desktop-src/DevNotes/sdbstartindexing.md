---
description: Ermöglicht das Erstellen und Ändern von Indizes für die angegebene Datenbank.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: Sdbstartindex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126391"
---
# <a name="sdbstartindexing-function"></a><span data-ttu-id="9701d-103">Sdbstartindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="9701d-103">SdbStartIndexing function</span></span>

<span data-ttu-id="9701d-104">Ermöglicht das Erstellen und Ändern von Indizes für die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9701d-104">Enables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9701d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9701d-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="9701d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9701d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9701d-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9701d-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9701d-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="9701d-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="9701d-109">*iiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9701d-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9701d-110">Der Indexbezeichner</span><span class="sxs-lookup"><span data-stu-id="9701d-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9701d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9701d-111">Return value</span></span>

<span data-ttu-id="9701d-112">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="9701d-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9701d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9701d-113">Requirements</span></span>



| <span data-ttu-id="9701d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9701d-114">Requirement</span></span> | <span data-ttu-id="9701d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9701d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9701d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9701d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9701d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9701d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9701d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9701d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9701d-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9701d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9701d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9701d-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9701d-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9701d-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9701d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9701d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9701d-123">**Sdbcommitindexes**</span><span class="sxs-lookup"><span data-stu-id="9701d-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="9701d-124">**Sdbdeclareingedex**</span><span class="sxs-lookup"><span data-stu-id="9701d-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="9701d-125">**Sdbstopindizierung**</span><span class="sxs-lookup"><span data-stu-id="9701d-125">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




