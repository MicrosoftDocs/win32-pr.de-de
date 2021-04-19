---
description: Öffnet ein Überprüfungs Profil, das als XML-Datei auf einem Datenträger gespeichert wurde.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'Iscanprofilemgr:: openprofile-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349237"
---
# <a name="iscanprofilemgropenprofile-method"></a><span data-ttu-id="1092b-103">Iscanprofilemgr:: openprofile-Methode</span><span class="sxs-lookup"><span data-stu-id="1092b-103">IScanProfileMgr::OpenProfile method</span></span>

<span data-ttu-id="1092b-104">Öffnet ein Überprüfungs Profil, das als XML-Datei auf einem Datenträger gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="1092b-104">Opens a scan profile that has been saved to disk as an XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1092b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1092b-105">Syntax</span></span>


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="1092b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1092b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1092b-107">*GUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1092b-107">*guid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1092b-108">Typ: **GUID**</span><span class="sxs-lookup"><span data-stu-id="1092b-108">Type: **GUID**</span></span>

<span data-ttu-id="1092b-109">Die GUID des Profils.</span><span class="sxs-lookup"><span data-stu-id="1092b-109">The GUID of the profile.</span></span>

</dd> <dt>

<span data-ttu-id="1092b-110">*ppscanprofile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1092b-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1092b-111">Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1092b-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="1092b-112">Die Adresse eines Zeigers auf das Profil.</span><span class="sxs-lookup"><span data-stu-id="1092b-112">The address of a pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1092b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1092b-113">Return value</span></span>

<span data-ttu-id="1092b-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1092b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1092b-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1092b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1092b-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1092b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1092b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1092b-117">Remarks</span></span>

<span data-ttu-id="1092b-118">Wenn ein Überprüfungs Profil mithilfe der [**Save**](-wia-iscanprofile-save.md) -Methode gespeichert wird, wird es als XML-Datei unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1092b-118">If a scan profile is saved using the [**Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="1092b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1092b-119">Requirements</span></span>



| <span data-ttu-id="1092b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1092b-120">Requirement</span></span> | <span data-ttu-id="1092b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1092b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1092b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1092b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1092b-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1092b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1092b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1092b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1092b-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1092b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1092b-126">Header</span><span class="sxs-lookup"><span data-stu-id="1092b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1092b-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="1092b-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="1092b-128">IDL</span><span class="sxs-lookup"><span data-stu-id="1092b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1092b-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1092b-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1092b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1092b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1092b-131">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="1092b-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="1092b-132">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="1092b-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




