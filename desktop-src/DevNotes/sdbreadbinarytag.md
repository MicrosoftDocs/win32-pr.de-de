---
Description: Ruft die Binärdaten für die angegebene TagID ab.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: Sdbreadbinarytag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337929"
---
# <a name="sdbreadbinarytag-function"></a><span data-ttu-id="93e1f-103">Sdbreadbinarytag-Funktion</span><span class="sxs-lookup"><span data-stu-id="93e1f-103">SdbReadBinaryTag function</span></span>

<span data-ttu-id="93e1f-104">Ruft die Binärdaten für die angegebene **TagID** ab.</span><span class="sxs-lookup"><span data-stu-id="93e1f-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93e1f-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="93e1f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93e1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e1f-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e1f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e1f-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="93e1f-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="93e1f-109">*tiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e1f-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e1f-110">Die **TagID** , die den abzurufenden Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="93e1f-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="93e1f-111">*pbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="93e1f-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93e1f-112">Der Puffer, der die Binärdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="93e1f-112">The buffer that receives the binary data.</span></span> <span data-ttu-id="93e1f-113">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="93e1f-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="93e1f-114">*dwbuffersize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e1f-114">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e1f-115">Die Größe des *pbuffer* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="93e1f-115">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e1f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93e1f-116">Return value</span></span>

<span data-ttu-id="93e1f-117">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="93e1f-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e1f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93e1f-118">Requirements</span></span>



| <span data-ttu-id="93e1f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93e1f-119">Requirement</span></span> | <span data-ttu-id="93e1f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="93e1f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93e1f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93e1f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93e1f-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93e1f-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="93e1f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93e1f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93e1f-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93e1f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="93e1f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="93e1f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93e1f-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e1f-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e1f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93e1f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e1f-128">**Sdbgetbinarytagdata**</span><span class="sxs-lookup"><span data-stu-id="93e1f-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="93e1f-129">**Sdbgetstringtagptr**</span><span class="sxs-lookup"><span data-stu-id="93e1f-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="93e1f-130">**Sdbreaddwordtag**</span><span class="sxs-lookup"><span data-stu-id="93e1f-130">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="93e1f-131">**Sdbreadstringtag**</span><span class="sxs-lookup"><span data-stu-id="93e1f-131">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




