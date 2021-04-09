---
Description: Ruft die Zeichenfolge für die angegebene TagID ab.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Sdbreadstringtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957089"
---
# <a name="sdbreadstringtag-function"></a><span data-ttu-id="1dcb7-103">Sdbreadstringtag-Funktion</span><span class="sxs-lookup"><span data-stu-id="1dcb7-103">SdbReadStringTag function</span></span>

<span data-ttu-id="1dcb7-104">Ruft die Zeichenfolge für die angegebene **TagID** ab.</span><span class="sxs-lookup"><span data-stu-id="1dcb7-104">Retrieves the string for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dcb7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dcb7-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="1dcb7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dcb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dcb7-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dcb7-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcb7-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1dcb7-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="1dcb7-109">*tiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dcb7-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcb7-110">Die **TagID** , die den abzurufenden Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="1dcb7-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1dcb7-111">*pwszbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1dcb7-111">*pwszBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcb7-112">Der Puffer, der die Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="1dcb7-112">The buffer that receives the string.</span></span> <span data-ttu-id="1dcb7-113">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1dcb7-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1dcb7-114">*cchbuffersize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dcb7-114">*cchBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcb7-115">Die Größe des *pwszbuffer* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1dcb7-115">The size of the *pwszBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dcb7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dcb7-116">Return value</span></span>

<span data-ttu-id="1dcb7-117">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="1dcb7-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dcb7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dcb7-118">Requirements</span></span>



| <span data-ttu-id="1dcb7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dcb7-119">Requirement</span></span> | <span data-ttu-id="1dcb7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1dcb7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dcb7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1dcb7-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dcb7-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1dcb7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dcb7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1dcb7-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dcb7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1dcb7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1dcb7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dcb7-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dcb7-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dcb7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dcb7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dcb7-128">**Sdbgetbinarytagdata**</span><span class="sxs-lookup"><span data-stu-id="1dcb7-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="1dcb7-129">**Sdbgetstringtagptr**</span><span class="sxs-lookup"><span data-stu-id="1dcb7-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="1dcb7-130">**Sdbreadbinarytag**</span><span class="sxs-lookup"><span data-stu-id="1dcb7-130">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
</dt> <dt>

[<span data-ttu-id="1dcb7-131">**Sdbreaddwordtag**</span><span class="sxs-lookup"><span data-stu-id="1dcb7-131">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> </dl>

 

 




