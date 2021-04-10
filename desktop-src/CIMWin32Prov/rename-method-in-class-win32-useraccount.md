---
description: Benennt einen Benutzerkonto Namen um.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Rename-Methode der Win32_UserAccount-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127364"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a><span data-ttu-id="e7cb4-103">Rename-Methode der Win32 \_ User Account-Klasse</span><span class="sxs-lookup"><span data-stu-id="e7cb4-103">Rename method of the Win32\_UserAccount class</span></span>

<span data-ttu-id="e7cb4-104">Die Methode zum **Umbenennen** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) benennt einen Benutzerkonto Namen um.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a user account name.</span></span>

<span data-ttu-id="e7cb4-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e7cb4-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e7cb4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7cb4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7cb4-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="e7cb4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7cb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7cb4-109">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7cb4-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-110">Neuer Kontoname.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-110">New account name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7cb4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7cb4-111">Return value</span></span>

<span data-ttu-id="e7cb4-112">Gibt einen der in der folgenden Liste aufgeführten Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-112">Returns one of the values listed in the following list.</span></span> <span data-ttu-id="e7cb4-113">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e7cb4-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e7cb4-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e7cb4-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e7cb4-115">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-116">0</span><span class="sxs-lookup"><span data-stu-id="e7cb4-116">0</span></span>

<span data-ttu-id="e7cb4-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-118">**Instanz nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-118">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-119">1</span><span class="sxs-lookup"><span data-stu-id="e7cb4-119">1</span></span>

<span data-ttu-id="e7cb4-120">Die Instanz wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-120">Instance not found.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-121">**Instanz erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-121">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-122">2</span><span class="sxs-lookup"><span data-stu-id="e7cb4-122">2</span></span>

<span data-ttu-id="e7cb4-123">Die Instanz ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-123">Instance required.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-124">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-124">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-125">3</span><span class="sxs-lookup"><span data-stu-id="e7cb4-125">3</span></span>

<span data-ttu-id="e7cb4-126">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-126">Invalid parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-127">**User not found (Benutzer wurde nicht gefunden)**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-127">**User not found**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-128">4</span><span class="sxs-lookup"><span data-stu-id="e7cb4-128">4</span></span>

<span data-ttu-id="e7cb4-129">Der Benutzer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-129">User not found.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-130">**Domäne nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-130">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-131">5</span><span class="sxs-lookup"><span data-stu-id="e7cb4-131">5</span></span>

<span data-ttu-id="e7cb4-132">Die Domäne wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-132">Domain not found.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-133">**Der Vorgang ist nur auf dem primären Domänen Controller der Domäne zulässig.**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-133">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-134">6</span><span class="sxs-lookup"><span data-stu-id="e7cb4-134">6</span></span>

<span data-ttu-id="e7cb4-135">Der Vorgang ist nur auf dem primären Domänen Controller der Domäne zulässig.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-135">Operation is allowed only on the primary domain controller of the domain.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-136">**Der Vorgang ist für das letzte Administrator Konto nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-136">**Operation is not allowed on the last administrative account.**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-137">7</span><span class="sxs-lookup"><span data-stu-id="e7cb4-137">7</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-138">**Der Vorgang ist für angegebene Sondergruppen nicht zulässig. Benutzer, Administrator, lokal oder Gast.**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-138">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-139">8</span><span class="sxs-lookup"><span data-stu-id="e7cb4-139">8</span></span>

<span data-ttu-id="e7cb4-140">Der Vorgang ist für angegebene Sondergruppen nicht zulässig: Benutzer, Administrator, lokal oder Gast.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-140">Operation is not allowed on specified special groups: user, admin, local, or guest.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-141">**Anderer API-Fehler**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-141">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-142">9</span><span class="sxs-lookup"><span data-stu-id="e7cb4-142">9</span></span>

<span data-ttu-id="e7cb4-143">Anderer API-Fehler.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-143">Other API error.</span></span>

</dd> <dt>

<span data-ttu-id="e7cb4-144">**Interner Fehler.**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-144">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="e7cb4-145">10</span><span class="sxs-lookup"><span data-stu-id="e7cb4-145">10</span></span>

<span data-ttu-id="e7cb4-146">Interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-146">Internal error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7cb4-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7cb4-147">Remarks</span></span>

<span data-ttu-id="e7cb4-148">Diese Funktion wird als Methode implementiert, um einen separaten Kontext für den neuen Namen bereitzustellen, der für den Namen, der der zu ändernden Instanz zugeordnet ist, nicht vom Schlüssel Eigenschafts Wert unterschieden werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7cb4-148">This functionality is implemented as a method to provide a separate context for the new name that is distinguishable from the key property value for Name that is associated with the instance to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7cb4-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7cb4-149">Requirements</span></span>



| <span data-ttu-id="e7cb4-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7cb4-150">Requirement</span></span> | <span data-ttu-id="e7cb4-151">Wert</span><span class="sxs-lookup"><span data-stu-id="e7cb4-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7cb4-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7cb4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e7cb4-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7cb4-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7cb4-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7cb4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e7cb4-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7cb4-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7cb4-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7cb4-156">Namespace</span></span><br/>                | <span data-ttu-id="e7cb4-157">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7cb4-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7cb4-158">MOF</span><span class="sxs-lookup"><span data-stu-id="e7cb4-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7cb4-159"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb4-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7cb4-160">DLL</span><span class="sxs-lookup"><span data-stu-id="e7cb4-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7cb4-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb4-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7cb4-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7cb4-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7cb4-163">**Win32- \_ Benutzerkonto**</span><span class="sxs-lookup"><span data-stu-id="e7cb4-163">**Win32\_UserAccount**</span></span>](win32-useraccount.md)
</dt> <dt>

<span data-ttu-id="e7cb4-164">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7cb4-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

