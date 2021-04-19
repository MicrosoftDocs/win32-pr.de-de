---
description: Ruft die Binärdaten für die angegebene TagID ab.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Sdbgetbinarytagdata-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342587"
---
# <a name="sdbgetbinarytagdata-function"></a><span data-ttu-id="96e73-103">Sdbgetbinarytagdata-Funktion</span><span class="sxs-lookup"><span data-stu-id="96e73-103">SdbGetBinaryTagData function</span></span>

<span data-ttu-id="96e73-104">Ruft die Binärdaten für die angegebene **TagID** ab.</span><span class="sxs-lookup"><span data-stu-id="96e73-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e73-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96e73-105">Syntax</span></span>


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="96e73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96e73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e73-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e73-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e73-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="96e73-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="96e73-109">*tiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e73-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e73-110">Die **TagID** , die den abzurufenden Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="96e73-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e73-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96e73-111">Return value</span></span>

<span data-ttu-id="96e73-112">Die-Funktion gibt einen Zeiger auf die Binärdaten oder **null** zurück, wenn die **TagID** ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="96e73-112">The function returns a pointer to the binary data or **NULL** if the **TAGID** is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e73-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96e73-113">Requirements</span></span>



| <span data-ttu-id="96e73-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96e73-114">Requirement</span></span> | <span data-ttu-id="96e73-115">Wert</span><span class="sxs-lookup"><span data-stu-id="96e73-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96e73-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96e73-116">Minimum supported client</span></span><br/> | <span data-ttu-id="96e73-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96e73-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="96e73-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96e73-118">Minimum supported server</span></span><br/> | <span data-ttu-id="96e73-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96e73-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96e73-120">DLL</span><span class="sxs-lookup"><span data-stu-id="96e73-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96e73-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96e73-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e73-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96e73-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e73-123">**Sdbgetstringtagptr**</span><span class="sxs-lookup"><span data-stu-id="96e73-123">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="96e73-124">**Sdbreaddwordtag**</span><span class="sxs-lookup"><span data-stu-id="96e73-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="96e73-125">**Sdbreadqwordtag**</span><span class="sxs-lookup"><span data-stu-id="96e73-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="96e73-126">**Sdbreadstringtag**</span><span class="sxs-lookup"><span data-stu-id="96e73-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




