---
description: Legt das angegebene Überprüfungs Profil als Standardprofil fest.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Iscanprofilemgr:: SetDefault-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357772"
---
# <a name="iscanprofilemgrsetdefault-method"></a><span data-ttu-id="d38c2-103">Iscanprofilemgr:: SetDefault-Methode</span><span class="sxs-lookup"><span data-stu-id="d38c2-103">IScanProfileMgr::SetDefault method</span></span>

<span data-ttu-id="d38c2-104">Legt das angegebene Überprüfungs Profil als Standardprofil fest.</span><span class="sxs-lookup"><span data-stu-id="d38c2-104">Sets the specified scan profile as the default profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d38c2-105">Syntax</span></span>


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="d38c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d38c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d38c2-107">*pscanprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d38c2-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d38c2-108">Geben Sie Folgendes ein: \**[**iscanprofile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d38c2-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="d38c2-109">Ein Zeiger auf das Profil.</span><span class="sxs-lookup"><span data-stu-id="d38c2-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d38c2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d38c2-110">Return value</span></span>

<span data-ttu-id="d38c2-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d38c2-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d38c2-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d38c2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d38c2-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d38c2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d38c2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d38c2-114">Remarks</span></span>

<span data-ttu-id="d38c2-115">Verwenden Sie die **iscanprofilemgr:: SetDefault** -Methode, um dem Profil ein-Element hinzuzufügen `<Default>` oder dieses Element aus dem vorherigen Standardprofil des Geräts zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d38c2-115">Use the **IScanProfileMgr::SetDefault** method to add a `<Default>` element to the profile or to remove that element from the device's previous default profile.</span></span>

<span data-ttu-id="d38c2-116">Verwenden Sie die [**scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode, um das Standardprofil zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d38c2-116">Use the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method to change the default profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="d38c2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d38c2-117">Requirements</span></span>



| <span data-ttu-id="d38c2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d38c2-118">Requirement</span></span> | <span data-ttu-id="d38c2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d38c2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38c2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d38c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d38c2-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d38c2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d38c2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d38c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d38c2-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d38c2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d38c2-124">Header</span><span class="sxs-lookup"><span data-stu-id="d38c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d38c2-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="d38c2-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="d38c2-126">IDL</span><span class="sxs-lookup"><span data-stu-id="d38c2-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d38c2-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d38c2-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38c2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d38c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38c2-129">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="d38c2-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="d38c2-130">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="d38c2-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




