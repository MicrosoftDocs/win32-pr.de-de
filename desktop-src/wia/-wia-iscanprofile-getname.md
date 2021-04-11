---
description: Ruft den anzeigen amen des Profils ab.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: 'Iscanprofile:: GetName-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214832"
---
# <a name="iscanprofilegetname-method"></a><span data-ttu-id="b45a7-103">Iscanprofile:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="b45a7-103">IScanProfile::GetName method</span></span>

<span data-ttu-id="b45a7-104">Ruft den anzeigen amen des Profils ab.</span><span class="sxs-lookup"><span data-stu-id="b45a7-104">Gets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b45a7-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="b45a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b45a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45a7-107">*pbstrinname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b45a7-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b45a7-108">Geben Sie Folgendes ein: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="b45a7-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="b45a7-109">Der Anzeige Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="b45a7-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45a7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b45a7-110">Return value</span></span>

<span data-ttu-id="b45a7-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b45a7-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b45a7-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b45a7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b45a7-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b45a7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b45a7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b45a7-114">Remarks</span></span>

<span data-ttu-id="b45a7-115">Diese Methode ist erforderlich, da die GUID eines Profils nicht verwendet werden kann, um dem Benutzer das Überprüfungs Profil anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b45a7-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

## <a name="requirements"></a><span data-ttu-id="b45a7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b45a7-116">Requirements</span></span>



| <span data-ttu-id="b45a7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b45a7-117">Requirement</span></span> | <span data-ttu-id="b45a7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b45a7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45a7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b45a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b45a7-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b45a7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b45a7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b45a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b45a7-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b45a7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b45a7-123">Header</span><span class="sxs-lookup"><span data-stu-id="b45a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b45a7-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45a7-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="b45a7-125">IDL</span><span class="sxs-lookup"><span data-stu-id="b45a7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b45a7-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b45a7-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b45a7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b45a7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45a7-128">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="b45a7-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="b45a7-129">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="b45a7-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




