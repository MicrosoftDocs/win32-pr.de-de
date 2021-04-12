---
description: Schreibt einen Word-Wert in die angegebene Datenbank.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: Sdbschreitewordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523315"
---
# <a name="sdbwritewordtag-function"></a><span data-ttu-id="a62fc-103">Sdbschreitewordtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="a62fc-103">SdbWriteWORDTag function</span></span>

<span data-ttu-id="a62fc-104">Schreibt einen **Word** -Wert in die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a62fc-104">Writes a **WORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a62fc-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a><span data-ttu-id="a62fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a62fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a62fc-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a62fc-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62fc-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a62fc-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="a62fc-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a62fc-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62fc-110">Das-Tag für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a62fc-110">The TAG for the entry.</span></span> <span data-ttu-id="a62fc-111">Dieses Tag muss vom Typ " **\_ Tagtyp \_ Wort**" sein.</span><span class="sxs-lookup"><span data-stu-id="a62fc-111">This TAG must be of type **TAG\_TYPE\_WORD**.</span></span>

</dd> <dt>

<span data-ttu-id="a62fc-112">*wdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a62fc-112">*wData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62fc-113">Der Wert.</span><span class="sxs-lookup"><span data-stu-id="a62fc-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a62fc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a62fc-114">Return value</span></span>

<span data-ttu-id="a62fc-115">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="a62fc-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a62fc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a62fc-116">Requirements</span></span>



| <span data-ttu-id="a62fc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a62fc-117">Requirement</span></span> | <span data-ttu-id="a62fc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a62fc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a62fc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a62fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a62fc-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a62fc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a62fc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a62fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a62fc-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a62fc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a62fc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a62fc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a62fc-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a62fc-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a62fc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a62fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62fc-126">**Sdbschreitebinarytag**</span><span class="sxs-lookup"><span data-stu-id="a62fc-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="a62fc-127">**Sdbschreitedwordtag**</span><span class="sxs-lookup"><span data-stu-id="a62fc-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="a62fc-128">**Sdbschreiteqwordtag**</span><span class="sxs-lookup"><span data-stu-id="a62fc-128">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="a62fc-129">**Sdbschreitestringtag**</span><span class="sxs-lookup"><span data-stu-id="a62fc-129">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> </dl>

 

 




