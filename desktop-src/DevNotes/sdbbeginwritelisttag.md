---
description: Erstellt ein neues listentag für Schreibvorgänge.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: Sdbbeginschreitelisttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748745"
---
# <a name="sdbbeginwritelisttag-function"></a><span data-ttu-id="dffc1-103">Sdbbeginschreitelisttag-Funktion</span><span class="sxs-lookup"><span data-stu-id="dffc1-103">SdbBeginWriteListTag function</span></span>

<span data-ttu-id="dffc1-104">Erstellt ein neues listentag für Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="dffc1-104">Creates a new list TAG for write operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffc1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dffc1-105">Syntax</span></span>


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="dffc1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dffc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dffc1-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dffc1-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dffc1-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="dffc1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="dffc1-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dffc1-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dffc1-110">Das-Tag für den neuen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="dffc1-110">The TAG for the new entry.</span></span> <span data-ttu-id="dffc1-111">Dieser Wert muss vom Typ " **\_ Tagtyp \_ Liste**" sein.</span><span class="sxs-lookup"><span data-stu-id="dffc1-111">This value must be of type **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dffc1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dffc1-112">Return value</span></span>

<span data-ttu-id="dffc1-113">Die-Funktion gibt bei einem Fehler die [**TagID**](tagid.md) der neuen Liste bei Erfolg oder **TagID \_ null** zurück.</span><span class="sxs-lookup"><span data-stu-id="dffc1-113">The function returns the [**TAGID**](tagid.md) of the new list on success or **TAGID\_NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dffc1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dffc1-114">Requirements</span></span>



| <span data-ttu-id="dffc1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dffc1-115">Requirement</span></span> | <span data-ttu-id="dffc1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dffc1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dffc1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dffc1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dffc1-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dffc1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dffc1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dffc1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dffc1-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dffc1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dffc1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="dffc1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dffc1-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dffc1-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dffc1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dffc1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffc1-124">**Sdbclosedatabase**</span><span class="sxs-lookup"><span data-stu-id="dffc1-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="dffc1-125">**Sdbclosedatabasewrite**</span><span class="sxs-lookup"><span data-stu-id="dffc1-125">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> <dt>

[<span data-ttu-id="dffc1-126">**Sdbendschreitelisttag**</span><span class="sxs-lookup"><span data-stu-id="dffc1-126">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="dffc1-127">**Tag**</span><span class="sxs-lookup"><span data-stu-id="dffc1-127">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="dffc1-128">Tagtypen</span><span class="sxs-lookup"><span data-stu-id="dffc1-128">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="dffc1-129">**TagID**</span><span class="sxs-lookup"><span data-stu-id="dffc1-129">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




