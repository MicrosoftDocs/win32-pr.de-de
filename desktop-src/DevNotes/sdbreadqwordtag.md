---
Description: Ruft den QWORD-Wert für die angegebene TagID ab.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: Sdbreadqwordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392182"
---
# <a name="sdbreadqwordtag-function"></a><span data-ttu-id="fa9ea-103">Sdbreadqwordtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="fa9ea-103">SdbReadQWORDTag function</span></span>

<span data-ttu-id="fa9ea-104">Ruft den **QWORD** -Wert für die angegebene **TagID** ab.</span><span class="sxs-lookup"><span data-stu-id="fa9ea-104">Retrieves the **QWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa9ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa9ea-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="fa9ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa9ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa9ea-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa9ea-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa9ea-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="fa9ea-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="fa9ea-109">*tiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa9ea-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa9ea-110">Die **TagID** , die den abzurufenden Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa9ea-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="fa9ea-111">*qwdefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa9ea-111">*qwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa9ea-112">Der Standardwert, der bei einem Fehler zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa9ea-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa9ea-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa9ea-113">Return value</span></span>

<span data-ttu-id="fa9ea-114">Die-Funktion gibt bei einem Fehler den Wert bei Erfolg oder *qwdefault* zurück.</span><span class="sxs-lookup"><span data-stu-id="fa9ea-114">The function returns the value on success or *qwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa9ea-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa9ea-115">Requirements</span></span>



| <span data-ttu-id="fa9ea-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa9ea-116">Requirement</span></span> | <span data-ttu-id="fa9ea-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fa9ea-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9ea-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa9ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fa9ea-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa9ea-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fa9ea-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa9ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fa9ea-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa9ea-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fa9ea-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fa9ea-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa9ea-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa9ea-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa9ea-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa9ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa9ea-125">**Sdbgetbinarytagdata**</span><span class="sxs-lookup"><span data-stu-id="fa9ea-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="fa9ea-126">**Sdbgetstringtagptr**</span><span class="sxs-lookup"><span data-stu-id="fa9ea-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="fa9ea-127">**Sdbreaddwordtag**</span><span class="sxs-lookup"><span data-stu-id="fa9ea-127">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="fa9ea-128">**Sdbreadstringtag**</span><span class="sxs-lookup"><span data-stu-id="fa9ea-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




