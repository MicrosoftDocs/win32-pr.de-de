---
description: Deklariert einen neuen Index in der angegebenen Datenbank.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Sdbdeclareingedex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343181"
---
# <a name="sdbdeclareindex-function"></a><span data-ttu-id="378cd-103">Sdbdeclareingedex-Funktion</span><span class="sxs-lookup"><span data-stu-id="378cd-103">SdbDeclareIndex function</span></span>

<span data-ttu-id="378cd-104">Deklariert einen neuen Index in der angegebenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="378cd-104">Declares a new index in the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="378cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="378cd-105">Syntax</span></span>


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a><span data-ttu-id="378cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="378cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="378cd-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378cd-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378cd-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="378cd-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="378cd-109">*TDas* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378cd-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378cd-110">Dieser Parameter muss eine **\_ Tagtyp \_ Liste** sein.</span><span class="sxs-lookup"><span data-stu-id="378cd-110">This parameter must be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="378cd-111">*TKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378cd-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378cd-112">Das-Tag, das den Typ angibt, der als Schlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="378cd-112">The TAG that specifies the type to be used as the key.</span></span> <span data-ttu-id="378cd-113">Dieser Parameter kann keine **\_ Tagtyp \_ Liste** sein.</span><span class="sxs-lookup"><span data-stu-id="378cd-113">This parameter cannot be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="378cd-114">*dwentries* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378cd-114">*dwEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378cd-115">Die Anzahl der Einträge, die im Index zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="378cd-115">The number of entries to allocate in the index.</span></span>

</dd> <dt>

<span data-ttu-id="378cd-116">*buniquekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378cd-116">*bUniqueKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378cd-117">Wenn dieser Parameter **true** ist, ist der Index ein Index mit einem eindeutigen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="378cd-117">If this parameter is **TRUE**, the index is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="378cd-118">*piiindex* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="378cd-118">*piiIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="378cd-119">Die resultierende **IndexID** des neu deklarierten Indexes.</span><span class="sxs-lookup"><span data-stu-id="378cd-119">The resulting **INDEXID** of the newly declared index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="378cd-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="378cd-120">Return value</span></span>

<span data-ttu-id="378cd-121">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="378cd-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="378cd-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="378cd-122">Remarks</span></span>

<span data-ttu-id="378cd-123">Diese Funktion wird aufgerufen, bevor Tags in den neuen Index geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="378cd-123">Call this function before writing tags to the new index.</span></span>

## <a name="requirements"></a><span data-ttu-id="378cd-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="378cd-124">Requirements</span></span>



| <span data-ttu-id="378cd-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="378cd-125">Requirement</span></span> | <span data-ttu-id="378cd-126">Wert</span><span class="sxs-lookup"><span data-stu-id="378cd-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="378cd-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="378cd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="378cd-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="378cd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="378cd-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="378cd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="378cd-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="378cd-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="378cd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="378cd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="378cd-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378cd-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="378cd-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="378cd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378cd-134">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="378cd-134">**INDEXID**</span></span>](indexid.md)
</dt> <dt>

[<span data-ttu-id="378cd-135">**Sdbcommitindexes**</span><span class="sxs-lookup"><span data-stu-id="378cd-135">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="378cd-136">**Sdbstartindizierung**</span><span class="sxs-lookup"><span data-stu-id="378cd-136">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="378cd-137">**Sdbstopindizierung**</span><span class="sxs-lookup"><span data-stu-id="378cd-137">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




