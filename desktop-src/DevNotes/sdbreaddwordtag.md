---
Description: Ruft den DWORD-Wert für die angegebene TagID ab.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: Sdbreaddwordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105927"
---
# <a name="sdbreaddwordtag-function"></a><span data-ttu-id="ac5ad-103">Sdbreaddwordtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac5ad-103">SdbReadDWORDTag function</span></span>

<span data-ttu-id="ac5ad-104">Ruft den **DWORD** -Wert für die angegebene **TagID** ab.</span><span class="sxs-lookup"><span data-stu-id="ac5ad-104">Retrieves the **DWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac5ad-105">Syntax</span></span>


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="ac5ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac5ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac5ad-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5ad-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5ad-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="ac5ad-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ac5ad-109">*tiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5ad-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5ad-110">Die **TagID** , die den abzurufenden Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="ac5ad-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="ac5ad-111">*dwdefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5ad-111">*dwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5ad-112">Der Standardwert, der bei einem Fehler zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac5ad-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac5ad-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac5ad-113">Return value</span></span>

<span data-ttu-id="ac5ad-114">Die-Funktion gibt bei einem Fehler den Wert bei Erfolg oder *dwdefault* zurück.</span><span class="sxs-lookup"><span data-stu-id="ac5ad-114">The function returns the value on success or *dwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac5ad-115">Requirements</span></span>



| <span data-ttu-id="ac5ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac5ad-116">Requirement</span></span> | <span data-ttu-id="ac5ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ac5ad-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5ad-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac5ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5ad-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac5ad-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ac5ad-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac5ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5ad-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac5ad-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac5ad-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ac5ad-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac5ad-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac5ad-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac5ad-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac5ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5ad-125">**Sdbgetbinarytagdata**</span><span class="sxs-lookup"><span data-stu-id="ac5ad-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="ac5ad-126">**Sdbgetstringtagptr**</span><span class="sxs-lookup"><span data-stu-id="ac5ad-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="ac5ad-127">**Sdbreadqwordtag**</span><span class="sxs-lookup"><span data-stu-id="ac5ad-127">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="ac5ad-128">**Sdbreadstringtag**</span><span class="sxs-lookup"><span data-stu-id="ac5ad-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




