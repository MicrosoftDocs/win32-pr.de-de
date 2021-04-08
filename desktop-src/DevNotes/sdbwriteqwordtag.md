---
description: Schreibt einen QWORD-Wert in die angegebene Datenbank.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: Sdbschreiteqwordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748089"
---
# <a name="sdbwriteqwordtag-function"></a><span data-ttu-id="0b327-103">Sdbschreiteqwordtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="0b327-103">SdbWriteQWORDTag function</span></span>

<span data-ttu-id="0b327-104">Schreibt einen **QWORD** -Wert in die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0b327-104">Writes a **QWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b327-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b327-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a><span data-ttu-id="0b327-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b327-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b327-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b327-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0b327-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0b327-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b327-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b327-110">Das-Tag für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0b327-110">The TAG for the entry.</span></span> <span data-ttu-id="0b327-111">Dieses Tag muss den Typ " **\_ Tagtyp \_ QWORD**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0b327-111">This TAG must be of type **TAG\_TYPE\_QWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="0b327-112">*qwdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b327-112">*qwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b327-113">Der Wert.</span><span class="sxs-lookup"><span data-stu-id="0b327-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b327-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b327-114">Return value</span></span>

<span data-ttu-id="0b327-115">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="0b327-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b327-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b327-116">Requirements</span></span>



| <span data-ttu-id="0b327-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b327-117">Requirement</span></span> | <span data-ttu-id="0b327-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0b327-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b327-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b327-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b327-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b327-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0b327-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b327-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b327-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b327-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b327-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0b327-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b327-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b327-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b327-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b327-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b327-126">**Sdbschreitebinarytag**</span><span class="sxs-lookup"><span data-stu-id="0b327-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="0b327-127">**Sdbschreitedwordtag**</span><span class="sxs-lookup"><span data-stu-id="0b327-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="0b327-128">**Sdbschreitestringtag**</span><span class="sxs-lookup"><span data-stu-id="0b327-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="0b327-129">**Sdbschreitewordtag**</span><span class="sxs-lookup"><span data-stu-id="0b327-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




