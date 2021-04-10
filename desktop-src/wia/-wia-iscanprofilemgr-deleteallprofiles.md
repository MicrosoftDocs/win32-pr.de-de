---
description: Löscht alle Überprüfungs Profile, die dem angegebenen Gerät zugeordnet sind.
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: Iscanprofilemgr::D eleteallprofiles-Methode (scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042281"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a><span data-ttu-id="2c7ef-103">Iscanprofilemgr::D eleteallprofiles-Methode</span><span class="sxs-lookup"><span data-stu-id="2c7ef-103">IScanProfileMgr::DeleteAllProfiles method</span></span>

<span data-ttu-id="2c7ef-104">Löscht alle Überprüfungs Profile, die dem angegebenen Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-104">Deletes all the scan profiles associated with the specified device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c7ef-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="2c7ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c7ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c7ef-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c7ef-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c7ef-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2c7ef-108">Type: **BSTR**</span></span>

<span data-ttu-id="2c7ef-109">Die ID des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-109">The ID of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c7ef-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c7ef-110">Return value</span></span>

<span data-ttu-id="2c7ef-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2c7ef-111">Type: **HRESULT**</span></span>

<span data-ttu-id="2c7ef-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c7ef-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c7ef-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c7ef-114">Requirements</span></span>



| <span data-ttu-id="2c7ef-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c7ef-115">Requirement</span></span> | <span data-ttu-id="2c7ef-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2c7ef-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7ef-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c7ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7ef-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c7ef-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2c7ef-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c7ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7ef-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c7ef-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c7ef-121">Header</span><span class="sxs-lookup"><span data-stu-id="2c7ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c7ef-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c7ef-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="2c7ef-123">IDL</span><span class="sxs-lookup"><span data-stu-id="2c7ef-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c7ef-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c7ef-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c7ef-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c7ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7ef-126">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="2c7ef-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="2c7ef-127">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="2c7ef-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




