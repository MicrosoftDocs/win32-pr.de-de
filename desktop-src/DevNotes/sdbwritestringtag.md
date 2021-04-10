---
description: Schreibt eine Zeichenfolge in die angegebene Datenbank.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: Sdbschreitestringtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860887"
---
# <a name="sdbwritestringtag-function"></a><span data-ttu-id="e2338-103">Sdbschreitestringtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="e2338-103">SdbWriteStringTag function</span></span>

<span data-ttu-id="e2338-104">Schreibt eine Zeichenfolge in die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e2338-104">Writes a string to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2338-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2338-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a><span data-ttu-id="e2338-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2338-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2338-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2338-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e2338-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="e2338-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2338-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2338-110">Das-Tag für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e2338-110">The TAG for the entry.</span></span> <span data-ttu-id="e2338-111">Dieses Tag muss vom Typ " **\_ Tagtyp \_**" "".</span><span class="sxs-lookup"><span data-stu-id="e2338-111">This TAG must be of type **TAG\_TYPE\_STRINGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="e2338-112">*pwszdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2338-112">*pwszData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2338-113">Die NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e2338-113">The null-terminated string.</span></span> <span data-ttu-id="e2338-114">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e2338-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2338-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2338-115">Return value</span></span>

<span data-ttu-id="e2338-116">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2338-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2338-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2338-117">Requirements</span></span>



| <span data-ttu-id="e2338-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2338-118">Requirement</span></span> | <span data-ttu-id="e2338-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e2338-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2338-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2338-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2338-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2338-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e2338-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2338-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2338-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2338-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e2338-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e2338-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2338-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2338-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2338-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2338-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2338-127">**Sdbschreitebinarytag**</span><span class="sxs-lookup"><span data-stu-id="e2338-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="e2338-128">**Sdbschreitedwordtag**</span><span class="sxs-lookup"><span data-stu-id="e2338-128">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="e2338-129">**Sdbschreiteqwordtag**</span><span class="sxs-lookup"><span data-stu-id="e2338-129">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="e2338-130">**Sdbschreitewordtag**</span><span class="sxs-lookup"><span data-stu-id="e2338-130">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




