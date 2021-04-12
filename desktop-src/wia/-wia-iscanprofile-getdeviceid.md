---
description: Gibt die ID des Geräts zurück.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'Iscanprofile:: getdeviceid-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344018"
---
# <a name="iscanprofilegetdeviceid-method"></a><span data-ttu-id="06e8d-103">Iscanprofile:: getdeviceid-Methode</span><span class="sxs-lookup"><span data-stu-id="06e8d-103">IScanProfile::GetDeviceID method</span></span>

<span data-ttu-id="06e8d-104">Gibt die ID des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="06e8d-104">Returns the ID of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e8d-105">Syntax</span></span>


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="06e8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06e8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e8d-107">*pbstraude viceid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="06e8d-107">*pbstrDeviceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06e8d-108">Geben Sie Folgendes ein: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="06e8d-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="06e8d-109">Ein Zeiger auf die Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="06e8d-109">A pointer to the device ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e8d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06e8d-110">Return value</span></span>

<span data-ttu-id="06e8d-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="06e8d-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="06e8d-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="06e8d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06e8d-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06e8d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e8d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06e8d-114">Requirements</span></span>



| <span data-ttu-id="06e8d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06e8d-115">Requirement</span></span> | <span data-ttu-id="06e8d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="06e8d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e8d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06e8d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06e8d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06e8d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="06e8d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06e8d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06e8d-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06e8d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06e8d-121">Header</span><span class="sxs-lookup"><span data-stu-id="06e8d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="06e8d-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="06e8d-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="06e8d-123">IDL</span><span class="sxs-lookup"><span data-stu-id="06e8d-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06e8d-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06e8d-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e8d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06e8d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e8d-126">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="06e8d-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="06e8d-127">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="06e8d-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




