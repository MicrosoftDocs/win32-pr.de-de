---
description: Gibt die GUID des Profils zurück.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'Iscanprofile:: GetGuid-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344009"
---
# <a name="iscanprofilegetguid-method"></a><span data-ttu-id="baa8f-103">Iscanprofile:: GetGuid-Methode</span><span class="sxs-lookup"><span data-stu-id="baa8f-103">IScanProfile::GetGUID method</span></span>

<span data-ttu-id="baa8f-104">Gibt die GUID des Profils zurück.</span><span class="sxs-lookup"><span data-stu-id="baa8f-104">Returns the GUID of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="baa8f-105">Syntax</span></span>


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a><span data-ttu-id="baa8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="baa8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa8f-107">*retval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="baa8f-107">*retVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="baa8f-108">Geben Sie Folgendes ein: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="baa8f-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="baa8f-109">Ein Zeiger auf die GUID des Profils.</span><span class="sxs-lookup"><span data-stu-id="baa8f-109">A pointer to the GUID of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa8f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baa8f-110">Return value</span></span>

<span data-ttu-id="baa8f-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="baa8f-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="baa8f-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="baa8f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="baa8f-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="baa8f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="baa8f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="baa8f-114">Remarks</span></span>

<span data-ttu-id="baa8f-115">Die GUID für ein Profil wird automatisch generiert, wenn das Profil mit " [**kreateprofile**](-wia-iscanprofilemgr-createprofile.md)" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="baa8f-115">The GUID for a profile is automatically generated when the profile is created with [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="baa8f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baa8f-116">Requirements</span></span>



| <span data-ttu-id="baa8f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baa8f-117">Requirement</span></span> | <span data-ttu-id="baa8f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="baa8f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa8f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="baa8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="baa8f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baa8f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="baa8f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="baa8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="baa8f-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baa8f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="baa8f-123">Header</span><span class="sxs-lookup"><span data-stu-id="baa8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="baa8f-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="baa8f-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="baa8f-125">IDL</span><span class="sxs-lookup"><span data-stu-id="baa8f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="baa8f-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="baa8f-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa8f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baa8f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa8f-128">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="baa8f-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="baa8f-129">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="baa8f-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




