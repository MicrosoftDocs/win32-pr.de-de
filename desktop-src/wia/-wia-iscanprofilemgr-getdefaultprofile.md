---
description: Ruft das Standard Überprüfungs Profil ab.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'Iscanprofilemgr:: getdefaultprofile-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e058094fc29510d6e073abc0b05374403a2b5cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348452"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a><span data-ttu-id="a7b64-103">Iscanprofilemgr:: getdefaultprofile-Methode</span><span class="sxs-lookup"><span data-stu-id="a7b64-103">IScanProfileMgr::GetDefaultProfile method</span></span>

<span data-ttu-id="a7b64-104">Ruft das Standard Überprüfungs Profil ab.</span><span class="sxs-lookup"><span data-stu-id="a7b64-104">Gets the default scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b64-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7b64-105">Syntax</span></span>


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="a7b64-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7b64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b64-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7b64-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b64-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a7b64-108">Type: **BSTR**</span></span>

<span data-ttu-id="a7b64-109">Die ID des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a7b64-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="a7b64-110">*ppscanprofile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7b64-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b64-111">Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a7b64-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="a7b64-112">Die Adresse eines Zeigers auf das Standardprofil des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a7b64-112">The address of a pointer to the device's default profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b64-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7b64-113">Return value</span></span>

<span data-ttu-id="a7b64-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7b64-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a7b64-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7b64-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7b64-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7b64-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b64-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7b64-117">Remarks</span></span>

<span data-ttu-id="a7b64-118">Das Standardprofil weist ein- `<Default>` Element auf.</span><span class="sxs-lookup"><span data-stu-id="a7b64-118">The default profile has a `<Default>` element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b64-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7b64-119">Requirements</span></span>



| <span data-ttu-id="a7b64-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7b64-120">Requirement</span></span> | <span data-ttu-id="a7b64-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a7b64-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b64-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7b64-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b64-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7b64-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a7b64-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7b64-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b64-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7b64-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7b64-126">Header</span><span class="sxs-lookup"><span data-stu-id="a7b64-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b64-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b64-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="a7b64-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a7b64-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7b64-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7b64-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b64-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7b64-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b64-131">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="a7b64-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="a7b64-132">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="a7b64-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




