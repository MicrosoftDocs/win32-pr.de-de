---
description: Sucht den ersten DWORD-Datensatz im angegebenen Index, der die angegebenen Kriterien erfüllt.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Sdbfindfirstdwordindexedtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522816"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a><span data-ttu-id="49d25-103">Sdbfindfirstdwordindexedtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="49d25-103">SdbFindFirstDWORDIndexedTag function</span></span>

<span data-ttu-id="49d25-104">Sucht den ersten **DWORD** -Datensatz im angegebenen Index, der die angegebenen Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="49d25-104">Finds the first **DWORD** record in the specified index that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="49d25-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49d25-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a><span data-ttu-id="49d25-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49d25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d25-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49d25-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d25-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="49d25-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="49d25-109">*TDas* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49d25-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d25-110">Der Indextyp.</span><span class="sxs-lookup"><span data-stu-id="49d25-110">The index type.</span></span> <span data-ttu-id="49d25-111">Eine Liste der Werte finden Sie unter [**Tag**](tag.md) .</span><span class="sxs-lookup"><span data-stu-id="49d25-111">See [**TAG**](tag.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="49d25-112">*TKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49d25-112">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d25-113">Der Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="49d25-113">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="49d25-114">*dwname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49d25-114">*dwName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d25-115">Der Name der Daten, die gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="49d25-115">The name of the data to be found.</span></span> <span data-ttu-id="49d25-116">Dieser Wert wird in einen Schlüssel konvertiert.</span><span class="sxs-lookup"><span data-stu-id="49d25-116">This value will be converted into a key.</span></span>

</dd> <dt>

<span data-ttu-id="49d25-117">*pfindinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="49d25-117">*pFindInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49d25-118">Eine [**Find \_ Info**](find-info.md) -Struktur, die den Datensatz empfängt.</span><span class="sxs-lookup"><span data-stu-id="49d25-118">A [**FIND\_INFO**](find-info.md) structure that receives the record.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49d25-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49d25-119">Return value</span></span>

<span data-ttu-id="49d25-120">Die **TagID** der ersten Entsprechung oder des **Tags \_ null** , wenn keine Entsprechung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="49d25-120">The **TAGID** of the first match or **TAG\_NULL** if no match is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d25-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49d25-121">Requirements</span></span>



| <span data-ttu-id="49d25-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49d25-122">Requirement</span></span> | <span data-ttu-id="49d25-123">Wert</span><span class="sxs-lookup"><span data-stu-id="49d25-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49d25-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49d25-124">Minimum supported client</span></span><br/> | <span data-ttu-id="49d25-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49d25-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="49d25-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49d25-126">Minimum supported server</span></span><br/> | <span data-ttu-id="49d25-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49d25-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="49d25-128">DLL</span><span class="sxs-lookup"><span data-stu-id="49d25-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49d25-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49d25-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d25-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49d25-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d25-131">**Sdbfindfirsttag**</span><span class="sxs-lookup"><span data-stu-id="49d25-131">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> </dl>

 

 




