---
description: Schreibt einen NULL-Eintrag in die angegebene Datenbank.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: Sdbschreitenulltag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214095"
---
# <a name="sdbwritenulltag-function"></a><span data-ttu-id="08cf1-103">Sdbschreitenulltag-Funktion</span><span class="sxs-lookup"><span data-stu-id="08cf1-103">SdbWriteNULLTag function</span></span>

<span data-ttu-id="08cf1-104">Schreibt einen **null** -Eintrag in die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="08cf1-104">Writes a **NULL** entry to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="08cf1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08cf1-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="08cf1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08cf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08cf1-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08cf1-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08cf1-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="08cf1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="08cf1-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08cf1-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08cf1-110">Das-Tag für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="08cf1-110">The TAG for the entry.</span></span> <span data-ttu-id="08cf1-111">Dieses Tag muss vom Typ " **\_ Tagtyp \_ null**" sein.</span><span class="sxs-lookup"><span data-stu-id="08cf1-111">This TAG must be of type **TAG\_TYPE\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08cf1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08cf1-112">Return value</span></span>

<span data-ttu-id="08cf1-113">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="08cf1-113">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="08cf1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08cf1-114">Requirements</span></span>



| <span data-ttu-id="08cf1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08cf1-115">Requirement</span></span> | <span data-ttu-id="08cf1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="08cf1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08cf1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08cf1-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08cf1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="08cf1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08cf1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08cf1-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08cf1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="08cf1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="08cf1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08cf1-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08cf1-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08cf1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08cf1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08cf1-124">**Sdbschreitebinarytag**</span><span class="sxs-lookup"><span data-stu-id="08cf1-124">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="08cf1-125">**Sdbschreitedwordtag**</span><span class="sxs-lookup"><span data-stu-id="08cf1-125">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="08cf1-126">**Sdbschreitestringtag**</span><span class="sxs-lookup"><span data-stu-id="08cf1-126">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="08cf1-127">**Sdbschreitewordtag**</span><span class="sxs-lookup"><span data-stu-id="08cf1-127">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




