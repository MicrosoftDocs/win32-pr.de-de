---
description: Ruft die Anzahl der Eigenschaften-IDs in einem Profil ab.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'Iscanprofile:: getnumpropids-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130029"
---
# <a name="iscanprofilegetnumpropids-method"></a><span data-ttu-id="e4e5d-103">Iscanprofile:: getnumpropids-Methode</span><span class="sxs-lookup"><span data-stu-id="e4e5d-103">IScanProfile::GetNumPropIDS method</span></span>

<span data-ttu-id="e4e5d-104">Ruft die Anzahl der Eigenschaften-IDs in einem Profil ab.</span><span class="sxs-lookup"><span data-stu-id="e4e5d-104">Gets the number of property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e5d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4e5d-105">Syntax</span></span>


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a><span data-ttu-id="e4e5d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4e5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e5d-107">*NUM* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4e5d-107">*num* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5d-108">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="e4e5d-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="e4e5d-109">Die Anzahl der Eigenschaften-IDs im Profil.</span><span class="sxs-lookup"><span data-stu-id="e4e5d-109">The number of property IDs in the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e5d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4e5d-110">Return value</span></span>

<span data-ttu-id="e4e5d-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e4e5d-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e4e5d-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e4e5d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4e5d-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4e5d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e5d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4e5d-114">Requirements</span></span>



| <span data-ttu-id="e4e5d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4e5d-115">Requirement</span></span> | <span data-ttu-id="e4e5d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e4e5d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e5d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4e5d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e5d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4e5d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e4e5d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4e5d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e5d-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4e5d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4e5d-121">Header</span><span class="sxs-lookup"><span data-stu-id="e4e5d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4e5d-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4e5d-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="e4e5d-123">IDL</span><span class="sxs-lookup"><span data-stu-id="e4e5d-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4e5d-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4e5d-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e5d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4e5d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e5d-126">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="e4e5d-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="e4e5d-127">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="e4e5d-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




