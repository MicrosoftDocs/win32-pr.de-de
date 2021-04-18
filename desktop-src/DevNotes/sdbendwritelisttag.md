---
description: Beendet die Schreibvorgänge für die angegebene Liste.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Sdbendschreitelisttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344583"
---
# <a name="sdbendwritelisttag-function"></a><span data-ttu-id="361ae-103">Sdbendschreitelisttag-Funktion</span><span class="sxs-lookup"><span data-stu-id="361ae-103">SdbEndWriteListTag function</span></span>

<span data-ttu-id="361ae-104">Beendet die Schreibvorgänge für die angegebene Liste.</span><span class="sxs-lookup"><span data-stu-id="361ae-104">Ends the write operations for the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="361ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="361ae-105">Syntax</span></span>


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a><span data-ttu-id="361ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="361ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="361ae-107">*PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="361ae-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="361ae-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="361ae-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="361ae-109">*tilist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="361ae-109">*tiList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="361ae-110">Die [**TagID**](tagid.md) der Liste.</span><span class="sxs-lookup"><span data-stu-id="361ae-110">The [**TAGID**](tagid.md) of the list</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="361ae-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="361ae-111">Return value</span></span>

<span data-ttu-id="361ae-112">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="361ae-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="361ae-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="361ae-113">Remarks</span></span>

<span data-ttu-id="361ae-114">Diese Funktion nach dem Schreiben aller Listeneinträge aufzurufen. das Ende der Liste wird markiert.</span><span class="sxs-lookup"><span data-stu-id="361ae-114">Call this function after writing all list entries; it will mark the end of the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="361ae-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="361ae-115">Requirements</span></span>



| <span data-ttu-id="361ae-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="361ae-116">Requirement</span></span> | <span data-ttu-id="361ae-117">Wert</span><span class="sxs-lookup"><span data-stu-id="361ae-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="361ae-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="361ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="361ae-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="361ae-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="361ae-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="361ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="361ae-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="361ae-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="361ae-122">DLL</span><span class="sxs-lookup"><span data-stu-id="361ae-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="361ae-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="361ae-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="361ae-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="361ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="361ae-125">**Sdbbeginschreitelisttag**</span><span class="sxs-lookup"><span data-stu-id="361ae-125">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="361ae-126">**Sdbclosedatabase**</span><span class="sxs-lookup"><span data-stu-id="361ae-126">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="361ae-127">**Sdbclosedatabasewrite**</span><span class="sxs-lookup"><span data-stu-id="361ae-127">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




