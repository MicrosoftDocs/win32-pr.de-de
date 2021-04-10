---
description: Schreibt einen DWORD-Wert in die angegebene Datenbank.
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: Sdbschreitedwordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5b549a91037aa308b5b88d0e3e2a51e153002bd5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214096"
---
# <a name="sdbwritedwordtag-function"></a><span data-ttu-id="c6294-103">Sdbschreitedwordtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="c6294-103">SdbWriteDWORDTag function</span></span>

<span data-ttu-id="c6294-104">Schreibt einen **DWORD** -Wert in die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c6294-104">Writes a **DWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6294-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6294-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
);
```



## <a name="parameters"></a><span data-ttu-id="c6294-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6294-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6294-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6294-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c6294-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="c6294-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6294-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6294-110">Das-Tag für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="c6294-110">The TAG for the entry.</span></span> <span data-ttu-id="c6294-111">Dieses Tag muss den Typ " **Tag \_ Type \_ DWORD**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c6294-111">This TAG must be of type **TAG\_TYPE\_DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="c6294-112">*dwdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6294-112">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6294-113">Der Wert.</span><span class="sxs-lookup"><span data-stu-id="c6294-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6294-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6294-114">Return value</span></span>

<span data-ttu-id="c6294-115">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c6294-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6294-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6294-116">Requirements</span></span>



| <span data-ttu-id="c6294-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6294-117">Requirement</span></span> | <span data-ttu-id="c6294-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c6294-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6294-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6294-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6294-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6294-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6294-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6294-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6294-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6294-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c6294-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c6294-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6294-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6294-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6294-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6294-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6294-126">**Sdbschreitebinarytag**</span><span class="sxs-lookup"><span data-stu-id="c6294-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="c6294-127">**Sdbschreiteqwordtag**</span><span class="sxs-lookup"><span data-stu-id="c6294-127">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="c6294-128">**Sdbschreitestringtag**</span><span class="sxs-lookup"><span data-stu-id="c6294-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="c6294-129">**Sdbschreitewordtag**</span><span class="sxs-lookup"><span data-stu-id="c6294-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




