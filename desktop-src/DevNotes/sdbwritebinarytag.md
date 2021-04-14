---
description: Schreibt Binärdaten in die angegebene Datenbank.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: Sdbschreitebinarytag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523323"
---
# <a name="sdbwritebinarytag-function"></a><span data-ttu-id="e3244-103">Sdbschreitebinarytag-Funktion</span><span class="sxs-lookup"><span data-stu-id="e3244-103">SdbWriteBinaryTag function</span></span>

<span data-ttu-id="e3244-104">Schreibt Binärdaten in die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e3244-104">Writes binary data to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3244-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3244-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a><span data-ttu-id="e3244-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3244-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3244-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3244-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e3244-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="e3244-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3244-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3244-110">Das-Tag für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e3244-110">The TAG for the entry.</span></span> <span data-ttu-id="e3244-111">Dieses Tag muss vom Typ " **Tag \_ Type \_ Binary**" sein.</span><span class="sxs-lookup"><span data-stu-id="e3244-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="e3244-112">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3244-112">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3244-113">Der Puffer, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e3244-113">The buffer that contains the data.</span></span> <span data-ttu-id="e3244-114">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e3244-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3244-115">*dwSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3244-115">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3244-116">Die Größe des *pbuffer* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e3244-116">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3244-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3244-117">Return value</span></span>

<span data-ttu-id="e3244-118">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="e3244-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3244-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3244-119">Requirements</span></span>



| <span data-ttu-id="e3244-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3244-120">Requirement</span></span> | <span data-ttu-id="e3244-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e3244-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3244-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3244-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e3244-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3244-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e3244-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3244-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e3244-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3244-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e3244-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e3244-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3244-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3244-127"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3244-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3244-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3244-129">**Sdbschreitebinarytagfromfile**</span><span class="sxs-lookup"><span data-stu-id="e3244-129">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
</dt> <dt>

[<span data-ttu-id="e3244-130">**Sdbschreitedwordtag**</span><span class="sxs-lookup"><span data-stu-id="e3244-130">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="e3244-131">**Sdbschreiteqwordtag**</span><span class="sxs-lookup"><span data-stu-id="e3244-131">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="e3244-132">**Sdbschreitestringtag**</span><span class="sxs-lookup"><span data-stu-id="e3244-132">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="e3244-133">**Sdbschreitewordtag**</span><span class="sxs-lookup"><span data-stu-id="e3244-133">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




