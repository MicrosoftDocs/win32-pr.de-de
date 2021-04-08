---
description: Legt den Wert der angegebenen untergeordneten Eigenschaften im <Properties> -Element eines Scan Profils.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Iscanprofile:: SetProperty-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752856"
---
# <a name="iscanprofilesetproperty-method"></a><span data-ttu-id="88a8e-104">Iscanprofile:: SetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="88a8e-104">IScanProfile::SetProperty method</span></span>

<span data-ttu-id="88a8e-105">Legt den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils fest.</span><span class="sxs-lookup"><span data-stu-id="88a8e-105">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="88a8e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="88a8e-106">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="88a8e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="88a8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a8e-108">*NUM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88a8e-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88a8e-109">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="88a8e-109">Type: **ULONG**</span></span>

<span data-ttu-id="88a8e-110">Die Anzahl der Einträge in den Arrays, auf die von *PID* und *pvar* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="88a8e-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="88a8e-111">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88a8e-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88a8e-112">Geben Sie Folgendes ein: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="88a8e-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="88a8e-113">Ein Zeiger auf ein Array von Identifikationsnummern der festzulegenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88a8e-113">A pointer to an array of identification numbers of the properties to be set.</span></span> <span data-ttu-id="88a8e-114">Jeder Wert im Array ist eine [WIA-Eigenschafts Konstante](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="88a8e-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="88a8e-115">_pvar \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88a8e-115">_pvar\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88a8e-116">Typ: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="88a8e-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="88a8e-117">Ein Zeiger auf ein Array von Werten, die den Eigenschaften zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88a8e-117">A pointer to an array of values to be assigned to the properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a8e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88a8e-118">Return value</span></span>

<span data-ttu-id="88a8e-119">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="88a8e-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="88a8e-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="88a8e-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88a8e-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88a8e-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88a8e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88a8e-122">Remarks</span></span>

<span data-ttu-id="88a8e-123">Jeder Wert im Array, auf den die *PID* zeigt, ist eine der [WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="88a8e-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="88a8e-124">Sie können dieses Identifikationssystem erweitern.</span><span class="sxs-lookup"><span data-stu-id="88a8e-124">You can extend this identification system.</span></span> <span data-ttu-id="88a8e-125">Siehe [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="88a8e-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="88a8e-126">Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="88a8e-126">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="88a8e-127">Wenn zwei Anwendungen Überprüfungs Profil Objekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in das zugehörige Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) Last aufruft, auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="88a8e-127">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a8e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88a8e-128">Requirements</span></span>



| <span data-ttu-id="88a8e-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88a8e-129">Requirement</span></span> | <span data-ttu-id="88a8e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="88a8e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a8e-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88a8e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="88a8e-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88a8e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="88a8e-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88a8e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="88a8e-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88a8e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88a8e-135">Header</span><span class="sxs-lookup"><span data-stu-id="88a8e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="88a8e-136"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="88a8e-136"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="88a8e-137">IDL</span><span class="sxs-lookup"><span data-stu-id="88a8e-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88a8e-138"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88a8e-138"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88a8e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88a8e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88a8e-140">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="88a8e-140">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="88a8e-141">**Licher**</span><span class="sxs-lookup"><span data-stu-id="88a8e-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="88a8e-142">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="88a8e-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="88a8e-143">WIA-Eigenschafts Konstanten</span><span class="sxs-lookup"><span data-stu-id="88a8e-143">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="88a8e-144">Definieren von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88a8e-144">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
