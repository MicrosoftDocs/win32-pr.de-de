---
description: Ruft die Anzahl der Scan Profile für das Gerät ab.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Iscanprofilemgr:: getnumprofilesfordeviceid-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214830"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a><span data-ttu-id="0733c-103">Iscanprofilemgr:: getnumprofilesfordeviceid-Methode</span><span class="sxs-lookup"><span data-stu-id="0733c-103">IScanProfileMgr::GetNumProfilesforDeviceID method</span></span>

<span data-ttu-id="0733c-104">Ruft die Anzahl der Scan Profile für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="0733c-104">Gets the number of scan profiles for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0733c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0733c-105">Syntax</span></span>


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="0733c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0733c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0733c-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0733c-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0733c-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0733c-108">Type: **BSTR**</span></span>

<span data-ttu-id="0733c-109">Die ID des Geräts.</span><span class="sxs-lookup"><span data-stu-id="0733c-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="0733c-110">*pulnumprofiles* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0733c-110">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0733c-111">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="0733c-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="0733c-112">Ein Zeiger auf die Anzahl der für das Gerät verfügbaren Profile.</span><span class="sxs-lookup"><span data-stu-id="0733c-112">A pointer to the number of profiles available for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0733c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0733c-113">Return value</span></span>

<span data-ttu-id="0733c-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0733c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0733c-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0733c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0733c-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0733c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0733c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0733c-117">Requirements</span></span>



| <span data-ttu-id="0733c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0733c-118">Requirement</span></span> | <span data-ttu-id="0733c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0733c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0733c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0733c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0733c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0733c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0733c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0733c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0733c-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0733c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0733c-124">Header</span><span class="sxs-lookup"><span data-stu-id="0733c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0733c-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="0733c-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="0733c-126">IDL</span><span class="sxs-lookup"><span data-stu-id="0733c-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0733c-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0733c-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0733c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0733c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0733c-129">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="0733c-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="0733c-130">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="0733c-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




