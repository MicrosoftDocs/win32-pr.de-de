---
description: Ruft alle Überprüfungs Profile ab, die für den Benutzer im System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Iscanprofilemgr:: getprofiles-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756643"
---
# <a name="iscanprofilemgrgetprofiles-method"></a><span data-ttu-id="74d3a-103">Iscanprofilemgr:: getprofiles-Methode</span><span class="sxs-lookup"><span data-stu-id="74d3a-103">IScanProfileMgr::GetProfiles method</span></span>

<span data-ttu-id="74d3a-104">Ruft alle Überprüfungs Profile ab, die für den Benutzer im System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74d3a-104">Gets all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74d3a-105">Syntax</span></span>


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="74d3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74d3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d3a-107">*pulnumprofiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="74d3a-107">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74d3a-108">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="74d3a-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="74d3a-109">Bei Übergabe ein Zeiger auf die maximale Anzahl von Profilen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="74d3a-109">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="74d3a-110">Bei der Rückgabe ein Zeiger auf die Anzahl der zurückgegebenen Profile.</span><span class="sxs-lookup"><span data-stu-id="74d3a-110">When returned, a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="74d3a-111">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74d3a-111">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74d3a-112">Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="74d3a-112">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="74d3a-113">Die Adresse eines Arrays von Zeigern auf Profile.</span><span class="sxs-lookup"><span data-stu-id="74d3a-113">The address of an array of pointers to profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d3a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74d3a-114">Return value</span></span>

<span data-ttu-id="74d3a-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="74d3a-115">Type: **HRESULT**</span></span>

<span data-ttu-id="74d3a-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="74d3a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74d3a-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74d3a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74d3a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74d3a-118">Remarks</span></span>

<span data-ttu-id="74d3a-119">Wenn die Gesamtzahl der für den Benutzer verfügbaren Profile kleiner ist als der an *pulnumprofiles* weiter gegebene Wert, gibt *pulnumprofiles* diese Summe zurück.</span><span class="sxs-lookup"><span data-stu-id="74d3a-119">If the total number of profiles available for the user is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="74d3a-120">Andernfalls wird derselbe Wert zurückgegeben, der an ihn übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="74d3a-120">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="74d3a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74d3a-121">Requirements</span></span>



| <span data-ttu-id="74d3a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74d3a-122">Requirement</span></span> | <span data-ttu-id="74d3a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="74d3a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d3a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74d3a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="74d3a-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74d3a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="74d3a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74d3a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="74d3a-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74d3a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74d3a-128">Header</span><span class="sxs-lookup"><span data-stu-id="74d3a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d3a-129"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d3a-129"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="74d3a-130">IDL</span><span class="sxs-lookup"><span data-stu-id="74d3a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74d3a-131"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="74d3a-131"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74d3a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74d3a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d3a-133">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="74d3a-133">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="74d3a-134">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="74d3a-134">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




