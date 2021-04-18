---
description: Ruft den Wert der angegebenen untergeordneten Eigenschaften in der ab. <Properties> -Element eines Scan Profils.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'Iscanprofile:: GetProperty-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345161"
---
# <a name="iscanprofilegetproperty-method"></a><span data-ttu-id="1972d-104">Iscanprofile:: GetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="1972d-104">IScanProfile::GetProperty method</span></span>

<span data-ttu-id="1972d-105">Ruft den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils ab.</span><span class="sxs-lookup"><span data-stu-id="1972d-105">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="1972d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1972d-106">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="1972d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1972d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1972d-108">*NUM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1972d-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1972d-109">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="1972d-109">Type: **ULONG**</span></span>

<span data-ttu-id="1972d-110">Die Anzahl der Einträge in den Arrays, auf die von *PID* und *pvar* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1972d-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="1972d-111">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1972d-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1972d-112">Geben Sie Folgendes ein: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="1972d-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="1972d-113">Ein Zeiger auf ein Array der Identifikationsnummern der festzulegenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1972d-113">A pointer to an array of the identification numbers of the properties to be set.</span></span> <span data-ttu-id="1972d-114">Jeder Wert im Array ist eine [WIA-Eigenschafts Konstante](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1972d-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1972d-115">_pvar \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1972d-115">_pvar\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1972d-116">Typ: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="1972d-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="1972d-117">Ein Zeiger auf ein Array von-Werten.</span><span class="sxs-lookup"><span data-stu-id="1972d-117">A pointer to an array of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1972d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1972d-118">Return value</span></span>

<span data-ttu-id="1972d-119">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1972d-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1972d-120">Gibt " \_ false" zurück, wenn einer der Eigenschaftswerte nicht verfügbar ist; andernfalls wird "s \_ OK" oder ein Standard-com-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1972d-120">Returns S\_FALSE if any of the property values is not available; otherwise, returns S\_OK or a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1972d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1972d-121">Remarks</span></span>

<span data-ttu-id="1972d-122">Der Typ jedes Werts muss dem Typ entsprechen, der mit dem [**iscanprofile:: SetProperty**](-wia-iscanprofile-setproperty.md)-aufrufen festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1972d-122">The type of each value must be the same type that was set with the call to [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).</span></span>

<span data-ttu-id="1972d-123">Jeder Wert im Array, auf den die *PID* zeigt, ist eine der [WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1972d-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="1972d-124">Sie können dieses Identifikationssystem erweitern.</span><span class="sxs-lookup"><span data-stu-id="1972d-124">You can extend this identification system.</span></span> <span data-ttu-id="1972d-125">Siehe [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1972d-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1972d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1972d-126">Requirements</span></span>



| <span data-ttu-id="1972d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1972d-127">Requirement</span></span> | <span data-ttu-id="1972d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1972d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1972d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1972d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1972d-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1972d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1972d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1972d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1972d-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1972d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1972d-133">Header</span><span class="sxs-lookup"><span data-stu-id="1972d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1972d-134"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1972d-134"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="1972d-135">IDL</span><span class="sxs-lookup"><span data-stu-id="1972d-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1972d-136"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1972d-136"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1972d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1972d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1972d-138">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="1972d-138">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="1972d-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="1972d-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1972d-140">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="1972d-140">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="1972d-141">WIA-Eigenschafts Konstanten</span><span class="sxs-lookup"><span data-stu-id="1972d-141">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="1972d-142">Definieren von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1972d-142">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
