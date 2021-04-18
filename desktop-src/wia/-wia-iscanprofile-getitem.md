---
description: Ruft die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements ab, dem das Profil zugeordnet ist.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'Iscanprofile:: GetItem-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343728"
---
# <a name="iscanprofilegetitem-method"></a><span data-ttu-id="79715-103">Iscanprofile:: GetItem-Methode</span><span class="sxs-lookup"><span data-stu-id="79715-103">IScanProfile::GetItem method</span></span>

<span data-ttu-id="79715-104">Ruft die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements ab, dem das Profil zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="79715-104">Gets the GUID of the category of the Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="79715-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79715-105">Syntax</span></span>


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="79715-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79715-107">*pguidcategory* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="79715-107">*pguidCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79715-108">Geben Sie Folgendes ein: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="79715-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="79715-109">Ein Zeiger auf die GUID der Kategorie des WIA 2,0-Elements.</span><span class="sxs-lookup"><span data-stu-id="79715-109">A pointer to the GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="79715-110">Dabei handelt es sich immer um eine der WIA- \_ IPA- \_ Element \_ kategoriekonstanten.</span><span class="sxs-lookup"><span data-stu-id="79715-110">This is always one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79715-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79715-111">Return value</span></span>

<span data-ttu-id="79715-112">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="79715-112">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="79715-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="79715-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79715-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79715-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79715-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79715-115">Requirements</span></span>



| <span data-ttu-id="79715-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79715-116">Requirement</span></span> | <span data-ttu-id="79715-117">Wert</span><span class="sxs-lookup"><span data-stu-id="79715-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="79715-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79715-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79715-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79715-119">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="79715-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79715-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79715-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79715-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79715-122">Header</span><span class="sxs-lookup"><span data-stu-id="79715-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79715-123"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="79715-123"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="79715-124">IDL</span><span class="sxs-lookup"><span data-stu-id="79715-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79715-125"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79715-125"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79715-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79715-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79715-127">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="79715-127">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="79715-128">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="79715-128">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




