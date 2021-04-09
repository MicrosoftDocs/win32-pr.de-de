---
description: Entfernt eine angegebene Liste von untergeordneten Eigenschaften im <Properties> -Element eines Scan Profils.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Iscanprofile:: RemoveProperty-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130025"
---
# <a name="iscanprofileremoveproperty-method"></a><span data-ttu-id="87a1e-104">Iscanprofile:: RemoveProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="87a1e-104">IScanProfile::RemoveProperty method</span></span>

<span data-ttu-id="87a1e-105">Entfernt eine angegebene Liste von untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils.</span><span class="sxs-lookup"><span data-stu-id="87a1e-105">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a1e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="87a1e-106">Syntax</span></span>


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a><span data-ttu-id="87a1e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="87a1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a1e-108">*NUM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87a1e-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a1e-109">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="87a1e-109">Type: **ULONG**</span></span>

<span data-ttu-id="87a1e-110">Die Anzahl der Einträge im Array, auf die die *PID* zeigt.</span><span class="sxs-lookup"><span data-stu-id="87a1e-110">The number of entries in the array that *pid* points to.</span></span>

</dd> <dt>

<span data-ttu-id="87a1e-111">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87a1e-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a1e-112">Geben Sie Folgendes ein: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="87a1e-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="87a1e-113">Ein Zeiger auf ein Array von Identifikationsnummern der zu löschenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="87a1e-113">A pointer to an array of identification numbers of the properties to be deleted.</span></span> <span data-ttu-id="87a1e-114">Jede ist eine [WIA-Eigenschafts Konstante](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="87a1e-114">Each is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a1e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87a1e-115">Return value</span></span>

<span data-ttu-id="87a1e-116">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="87a1e-116">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="87a1e-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="87a1e-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="87a1e-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87a1e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="87a1e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87a1e-119">Remarks</span></span>

<span data-ttu-id="87a1e-120">Jeder Wert im Array, auf den die *PID* zeigt, ist eine der [WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="87a1e-120">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="87a1e-121">Sie können dieses Identifikationssystem erweitern.</span><span class="sxs-lookup"><span data-stu-id="87a1e-121">You can extend this identification system.</span></span> <span data-ttu-id="87a1e-122">Siehe [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="87a1e-122">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="87a1e-123">Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="87a1e-123">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="87a1e-124">Wenn zwei Anwendungen Überprüfungs Profil Objekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in das zugehörige Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) Last aufruft, auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="87a1e-124">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a1e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87a1e-125">Requirements</span></span>



| <span data-ttu-id="87a1e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87a1e-126">Requirement</span></span> | <span data-ttu-id="87a1e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="87a1e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a1e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87a1e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87a1e-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87a1e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="87a1e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87a1e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87a1e-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87a1e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87a1e-132">Header</span><span class="sxs-lookup"><span data-stu-id="87a1e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="87a1e-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="87a1e-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="87a1e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="87a1e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87a1e-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87a1e-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a1e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87a1e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a1e-137">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="87a1e-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="87a1e-138">**Licher**</span><span class="sxs-lookup"><span data-stu-id="87a1e-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87a1e-139">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="87a1e-139">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="87a1e-140">WIA-Eigenschafts Konstanten</span><span class="sxs-lookup"><span data-stu-id="87a1e-140">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="87a1e-141">Definieren von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87a1e-141">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




