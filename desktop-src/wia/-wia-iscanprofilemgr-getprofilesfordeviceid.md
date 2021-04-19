---
description: Ruft alle einem Gerät zugeordneten Scan Profile ab.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'Iscanprofilemgr:: getprofilesfordeviceid-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349051"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a><span data-ttu-id="c902d-103">Iscanprofilemgr:: getprofilesfordeviceid-Methode</span><span class="sxs-lookup"><span data-stu-id="c902d-103">IScanProfileMgr::GetProfilesforDeviceID method</span></span>

<span data-ttu-id="c902d-104">Ruft alle einem Gerät zugeordneten Scan Profile ab.</span><span class="sxs-lookup"><span data-stu-id="c902d-104">Gets all the scan profiles associated with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c902d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c902d-105">Syntax</span></span>


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="c902d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c902d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c902d-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c902d-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c902d-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c902d-108">Type: **BSTR**</span></span>

<span data-ttu-id="c902d-109">Die ID des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c902d-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="c902d-110">*pulnumprofiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c902d-110">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c902d-111">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="c902d-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="c902d-112">Bei Übergabe ein Zeiger auf die maximale Anzahl von Profilen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c902d-112">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="c902d-113">Wenn die Rückgabe zurückgegeben wird, ist dies ein Zeiger auf die Anzahl der zurückgegebenen Profile.</span><span class="sxs-lookup"><span data-stu-id="c902d-113">When returned, the a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="c902d-114">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c902d-114">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c902d-115">Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c902d-115">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="c902d-116">Die Adresse eines Zeigers auf ein Array von Profilen.</span><span class="sxs-lookup"><span data-stu-id="c902d-116">The address of a pointer to an array of profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c902d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c902d-117">Return value</span></span>

<span data-ttu-id="c902d-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c902d-118">Type: **HRESULT**</span></span>

<span data-ttu-id="c902d-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c902d-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c902d-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c902d-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c902d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c902d-121">Remarks</span></span>

<span data-ttu-id="c902d-122">Wenn die Gesamtanzahl der Profile, die dem Gerät zugeordnet sind, kleiner ist als der an *pulnumprofiles* weiter gegebene Wert, gibt *pulnumprofiles* diese Summe zurück.</span><span class="sxs-lookup"><span data-stu-id="c902d-122">If the total number of profiles associated with the device is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="c902d-123">Andernfalls wird derselbe Wert zurückgegeben, der an ihn übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="c902d-123">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c902d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c902d-124">Requirements</span></span>



| <span data-ttu-id="c902d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c902d-125">Requirement</span></span> | <span data-ttu-id="c902d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c902d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c902d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c902d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c902d-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c902d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c902d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c902d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c902d-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c902d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c902d-131">Header</span><span class="sxs-lookup"><span data-stu-id="c902d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c902d-132"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="c902d-132"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="c902d-133">IDL</span><span class="sxs-lookup"><span data-stu-id="c902d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c902d-134"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c902d-134"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c902d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c902d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c902d-136">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="c902d-136">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="c902d-137">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="c902d-137">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




