---
description: Ruft einen Wert ab, der angibt, ob das Profil das Standard Überprüfungs Profil eines zugeordneten IWiaItem2-Geräts ist.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Iscanprofile:: IsDefault-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959089"
---
# <a name="iscanprofileisdefault-method"></a><span data-ttu-id="2197e-103">Iscanprofile:: IsDefault-Methode</span><span class="sxs-lookup"><span data-stu-id="2197e-103">IScanProfile::IsDefault method</span></span>

<span data-ttu-id="2197e-104">Ruft einen Wert ab, der angibt, ob das Profil das Standard Überprüfungs Profil eines zugeordneten [**IWiaItem2**](-wia-iwiaitem2.md) -Geräts ist.</span><span class="sxs-lookup"><span data-stu-id="2197e-104">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2197e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2197e-105">Syntax</span></span>


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a><span data-ttu-id="2197e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2197e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2197e-107">*pbdefault* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2197e-107">*pbDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2197e-108">Typ: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="2197e-108">Type: \**BOOL\** _</span></span>

<span data-ttu-id="2197e-109">Ein Zeiger auf einen _ \* bool \* \*.</span><span class="sxs-lookup"><span data-stu-id="2197e-109">A pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="2197e-110"><span id="TRUE"></span><span id="true"></span>**Fall**</span><span class="sxs-lookup"><span data-stu-id="2197e-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="2197e-111">Das Profil ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="2197e-111">The profile is the default.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="2197e-112"><span id="FALSE"></span><span id="false"></span>**Alarm**</span><span class="sxs-lookup"><span data-stu-id="2197e-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="2197e-113">Das Profil ist nicht die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="2197e-113">The profile is not the default.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2197e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2197e-114">Return value</span></span>

<span data-ttu-id="2197e-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2197e-115">Type: **HRESULT**</span></span>

<span data-ttu-id="2197e-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2197e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2197e-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2197e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2197e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2197e-118">Remarks</span></span>

<span data-ttu-id="2197e-119">*pbdefault* ist **true** , wenn das Profil ein- `<Default>` Element enthält.</span><span class="sxs-lookup"><span data-stu-id="2197e-119">*pbDefault* is **TRUE** if the profile contains a `<Default>` element.</span></span> <span data-ttu-id="2197e-120">Der Wert ist **false** , wenn kein solches Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2197e-120">It is **FALSE** if no such element is present.</span></span> <span data-ttu-id="2197e-121">Das Element hat keinen Wert.</span><span class="sxs-lookup"><span data-stu-id="2197e-121">The element has no value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2197e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2197e-122">Requirements</span></span>



| <span data-ttu-id="2197e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2197e-123">Requirement</span></span> | <span data-ttu-id="2197e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2197e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2197e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2197e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2197e-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2197e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2197e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2197e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2197e-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2197e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2197e-129">Header</span><span class="sxs-lookup"><span data-stu-id="2197e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2197e-130"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="2197e-130"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="2197e-131">IDL</span><span class="sxs-lookup"><span data-stu-id="2197e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2197e-132"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2197e-132"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2197e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2197e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2197e-134">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="2197e-134">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="2197e-135">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="2197e-135">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




