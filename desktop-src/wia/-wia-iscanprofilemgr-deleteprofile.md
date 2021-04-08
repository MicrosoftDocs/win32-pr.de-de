---
description: Löscht das angegebene Überprüfungs Profil.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: Iscanprofilemgr::D eleteprofile-Methode (scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959822"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a><span data-ttu-id="49733-103">Iscanprofilemgr::D eleteprofile-Methode</span><span class="sxs-lookup"><span data-stu-id="49733-103">IScanProfileMgr::DeleteProfile method</span></span>

<span data-ttu-id="49733-104">Löscht das angegebene Überprüfungs Profil.</span><span class="sxs-lookup"><span data-stu-id="49733-104">Deletes the specified scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="49733-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49733-105">Syntax</span></span>


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="49733-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49733-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49733-107">*pscanprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49733-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49733-108">Geben Sie Folgendes ein: \**[**iscanprofile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="49733-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="49733-109">Ein Zeiger auf das Profil.</span><span class="sxs-lookup"><span data-stu-id="49733-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49733-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49733-110">Return value</span></span>

<span data-ttu-id="49733-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="49733-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="49733-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="49733-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49733-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49733-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49733-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49733-114">Remarks</span></span>

<span data-ttu-id="49733-115">**Iscanprofilemgr::D eleteprofile** löscht das Profil von der Festplatte und zerstört das Profil Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="49733-115">**IScanProfileMgr::DeleteProfile** deletes the profile from disk and destroys the profile object in memory.</span></span>

<span data-ttu-id="49733-116">Verwenden Sie die [**iscanprofilemgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) -Methode, wenn mehrere [**iscanprofilemgr**](-wia-iscanprofilemgr.md) -Objekte gleichzeitig Profile erstellen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="49733-116">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="49733-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49733-117">Requirements</span></span>



| <span data-ttu-id="49733-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49733-118">Requirement</span></span> | <span data-ttu-id="49733-119">Wert</span><span class="sxs-lookup"><span data-stu-id="49733-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="49733-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49733-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49733-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49733-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="49733-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49733-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49733-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49733-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49733-124">Header</span><span class="sxs-lookup"><span data-stu-id="49733-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49733-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="49733-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="49733-126">IDL</span><span class="sxs-lookup"><span data-stu-id="49733-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49733-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49733-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49733-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49733-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49733-129">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="49733-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="49733-130">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="49733-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




