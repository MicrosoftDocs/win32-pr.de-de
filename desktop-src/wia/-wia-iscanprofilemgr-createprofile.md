---
description: Erstellt ein leeres Überprüfungs Profil und ordnet es einem Scanner oder einem anderen Windows-Abbild Erfassungs Element (WIA) 2,0 zu.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Iscanprofilemgr:: kreateprofile-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485294"
---
# <a name="iscanprofilemgrcreateprofile-method"></a><span data-ttu-id="6b1df-103">Iscanprofilemgr:: kreateprofile-Methode</span><span class="sxs-lookup"><span data-stu-id="6b1df-103">IScanProfileMgr::CreateProfile method</span></span>

<span data-ttu-id="6b1df-104">Erstellt ein leeres Überprüfungs Profil und ordnet es einem Scanner oder einem anderen Windows-Abbild Erfassungs Element (WIA) 2,0 zu.</span><span class="sxs-lookup"><span data-stu-id="6b1df-104">Creates an empty scan profile and associates it with a scanner or other Windows Image Acquisition (WIA) 2.0 item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b1df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b1df-105">Syntax</span></span>


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="6b1df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b1df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b1df-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b1df-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1df-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6b1df-108">Type: **BSTR**</span></span>

<span data-ttu-id="6b1df-109">Die ID des Geräts oder des WIA-2,0-Elements.</span><span class="sxs-lookup"><span data-stu-id="6b1df-109">The ID of the device or WIA 2.0 item.</span></span>

</dd> <dt>

<span data-ttu-id="6b1df-110">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b1df-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1df-111">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6b1df-111">Type: **BSTR**</span></span>

<span data-ttu-id="6b1df-112">Der Anzeige Name des neuen Profils.</span><span class="sxs-lookup"><span data-stu-id="6b1df-112">The friendly name of the new profile.</span></span>

</dd> <dt>

<span data-ttu-id="6b1df-113">*guidcategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b1df-113">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1df-114">Typ: **GUID**</span><span class="sxs-lookup"><span data-stu-id="6b1df-114">Type: **GUID**</span></span>

<span data-ttu-id="6b1df-115">Der GUID der Kategorie des Geräts oder eines WIA-2,0-Elements.</span><span class="sxs-lookup"><span data-stu-id="6b1df-115">The GUID of the category of the device or WIA 2.0 item.</span></span> <span data-ttu-id="6b1df-116">Dabei muss es sich um eine der WIA- \_ IPA- \_ Element Kategorie- \_ Konstanten handeln.</span><span class="sxs-lookup"><span data-stu-id="6b1df-116">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> <dt>

<span data-ttu-id="6b1df-117">*ppscanprofile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b1df-117">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1df-118">Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6b1df-118">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="6b1df-119">Die Adresse eines Zeigers auf das neue Profil.</span><span class="sxs-lookup"><span data-stu-id="6b1df-119">The address of a pointer to the new profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b1df-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b1df-120">Return value</span></span>

<span data-ttu-id="6b1df-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6b1df-121">Type: **HRESULT**</span></span>

<span data-ttu-id="6b1df-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b1df-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6b1df-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b1df-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b1df-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b1df-124">Remarks</span></span>

<span data-ttu-id="6b1df-125">**Iscanprofilemgr:: kreateprofile** ordnet das angegebene Gerät dem neuen Überprüfungs Profil zu.</span><span class="sxs-lookup"><span data-stu-id="6b1df-125">**IScanProfileMgr::CreateProfile** associates the specified device with the new scan profile.</span></span>

<span data-ttu-id="6b1df-126">**Iscanprofilemgr:: kreateprofile** generiert automatisch eine GUID für das neue Profil.</span><span class="sxs-lookup"><span data-stu-id="6b1df-126">**IScanProfileMgr::CreateProfile** automatically generates a GUID for the new profile.</span></span> <span data-ttu-id="6b1df-127">Holen Sie sich die GUID mit [**GetGuid**](-wia-iscanprofile-getguid.md).</span><span class="sxs-lookup"><span data-stu-id="6b1df-127">Get the GUID with [**GetGUID**](-wia-iscanprofile-getguid.md).</span></span>

<span data-ttu-id="6b1df-128">Verwenden Sie die [**iscanprofilemgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) -Methode, wenn mehrere [**iscanprofilemgr**](-wia-iscanprofilemgr.md) -Objekte gleichzeitig Profile erstellen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="6b1df-128">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1df-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b1df-129">Requirements</span></span>



| <span data-ttu-id="6b1df-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b1df-130">Requirement</span></span> | <span data-ttu-id="6b1df-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6b1df-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1df-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b1df-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6b1df-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b1df-133">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6b1df-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b1df-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6b1df-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b1df-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b1df-136">Header</span><span class="sxs-lookup"><span data-stu-id="6b1df-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b1df-137"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1df-137"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="6b1df-138">IDL</span><span class="sxs-lookup"><span data-stu-id="6b1df-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b1df-139"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b1df-139"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1df-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b1df-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1df-141">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="6b1df-141">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="6b1df-142">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="6b1df-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




