---
description: Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Iscanprofile:: getallpropids-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349052"
---
# <a name="iscanprofilegetallpropids-method"></a><span data-ttu-id="28246-103">Iscanprofile:: getallpropids-Methode</span><span class="sxs-lookup"><span data-stu-id="28246-103">IScanProfile::GetAllPropIDs method</span></span>

<span data-ttu-id="28246-104">Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.</span><span class="sxs-lookup"><span data-stu-id="28246-104">Gets all available property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="28246-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28246-105">Syntax</span></span>


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a><span data-ttu-id="28246-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28246-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28246-107">*NUM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28246-107">*num* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28246-108">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="28246-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="28246-109">Die Anzahl der angeforderten oder zurückgegebenen Eigenschaften-IDs.</span><span class="sxs-lookup"><span data-stu-id="28246-109">The number of property IDs requested or returned.</span></span>

</dd> <dt>

<span data-ttu-id="28246-110">_ppid \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="28246-110">_ppid\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28246-111">Geben Sie Folgendes ein: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="28246-111">Type: \**PROPID\** _</span></span>

<span data-ttu-id="28246-112">Ein Zeiger auf ein Array von Eigenschaften-IDs.</span><span class="sxs-lookup"><span data-stu-id="28246-112">A pointer to an array of property IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28246-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28246-113">Return value</span></span>

<span data-ttu-id="28246-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="28246-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="28246-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="28246-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28246-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28246-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="28246-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28246-117">Requirements</span></span>



| <span data-ttu-id="28246-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28246-118">Requirement</span></span> | <span data-ttu-id="28246-119">Wert</span><span class="sxs-lookup"><span data-stu-id="28246-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="28246-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28246-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28246-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28246-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="28246-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28246-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28246-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28246-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28246-124">Header</span><span class="sxs-lookup"><span data-stu-id="28246-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="28246-125"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="28246-125"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="28246-126">IDL</span><span class="sxs-lookup"><span data-stu-id="28246-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28246-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28246-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28246-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28246-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28246-129">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="28246-129">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="28246-130">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="28246-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




