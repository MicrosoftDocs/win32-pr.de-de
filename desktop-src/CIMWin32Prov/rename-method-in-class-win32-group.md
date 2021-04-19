---
description: Ermöglicht, dass der Gruppenname geändert wird.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Rename-Methode der Win32_Group-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345606"
---
# <a name="rename-method-of-the-win32_group-class"></a><span data-ttu-id="8b762-103">Rename-Methode der Win32- \_ Gruppenklasse</span><span class="sxs-lookup"><span data-stu-id="8b762-103">Rename method of the Win32\_Group class</span></span>

<span data-ttu-id="8b762-104">Die Methode zum **Umbenennen** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) ermöglicht, dass der Gruppenname geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8b762-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows the group name to be changed.</span></span>

<span data-ttu-id="8b762-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b762-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8b762-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8b762-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b762-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b762-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="8b762-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b762-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b762-109">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b762-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b762-110">Der Name des Windows-Benutzerkontos in der Domäne, die durch die **Domänen** Eigenschaft dieser Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b762-110">Name of the Windows user account on the domain specified by the **Domain** property of this class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b762-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b762-111">Return value</span></span>

<span data-ttu-id="8b762-112">Die **Rename** -Methode kann die in der folgenden Liste aufgeführten Fehlercodes zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8b762-112">The **Rename** method can return the error codes listed in the following list.</span></span> <span data-ttu-id="8b762-113">Weitere ganzzahlige Werte als die aufgeführten Werte finden Sie unter [WMI- \_ Rückgabe Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span><span class="sxs-lookup"><span data-stu-id="8b762-113">For integer values other than those listed, refer to [WMI\_Return Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8b762-114">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="8b762-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-115">0</span><span class="sxs-lookup"><span data-stu-id="8b762-115">0</span></span>

<span data-ttu-id="8b762-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="8b762-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8b762-117">**Instanz nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="8b762-117">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-118">1</span><span class="sxs-lookup"><span data-stu-id="8b762-118">1</span></span>

</dd> <dt>

<span data-ttu-id="8b762-119">**Instanz erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8b762-119">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-120">2</span><span class="sxs-lookup"><span data-stu-id="8b762-120">2</span></span>

</dd> <dt>

<span data-ttu-id="8b762-121">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="8b762-121">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-122">3</span><span class="sxs-lookup"><span data-stu-id="8b762-122">3</span></span>

</dd> <dt>

<span data-ttu-id="8b762-123">**Gruppe nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="8b762-123">**Group not found**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-124">4</span><span class="sxs-lookup"><span data-stu-id="8b762-124">4</span></span>

</dd> <dt>

<span data-ttu-id="8b762-125">**Domäne nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="8b762-125">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-126">5</span><span class="sxs-lookup"><span data-stu-id="8b762-126">5</span></span>

</dd> <dt>

<span data-ttu-id="8b762-127">**Der Vorgang ist nur auf dem primären Domänen Controller der Domäne zulässig.**</span><span class="sxs-lookup"><span data-stu-id="8b762-127">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-128">6</span><span class="sxs-lookup"><span data-stu-id="8b762-128">6</span></span>

</dd> <dt>

<span data-ttu-id="8b762-129">**Der Vorgang ist für angegebene Sondergruppen nicht zulässig. Benutzer, Administrator, lokal oder Gast.**</span><span class="sxs-lookup"><span data-stu-id="8b762-129">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-130">7</span><span class="sxs-lookup"><span data-stu-id="8b762-130">7</span></span>

</dd> <dt>

<span data-ttu-id="8b762-131">**Anderer API-Fehler**</span><span class="sxs-lookup"><span data-stu-id="8b762-131">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-132">8</span><span class="sxs-lookup"><span data-stu-id="8b762-132">8</span></span>

</dd> <dt>

<span data-ttu-id="8b762-133">**Interner Fehler.**</span><span class="sxs-lookup"><span data-stu-id="8b762-133">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="8b762-134">9</span><span class="sxs-lookup"><span data-stu-id="8b762-134">9</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b762-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b762-135">Requirements</span></span>



| <span data-ttu-id="8b762-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b762-136">Requirement</span></span> | <span data-ttu-id="8b762-137">Wert</span><span class="sxs-lookup"><span data-stu-id="8b762-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b762-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b762-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8b762-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b762-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b762-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b762-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8b762-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b762-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b762-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b762-142">Namespace</span></span><br/>                | <span data-ttu-id="8b762-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8b762-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b762-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8b762-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b762-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b762-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b762-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8b762-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b762-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b762-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b762-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b762-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b762-149">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b762-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8b762-150">**Win32- \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="8b762-150">**Win32\_Group**</span></span>](win32-group.md)
</dt> <dt>

[<span data-ttu-id="8b762-151">**Win32 \_ logicalfilesecuritysetting**</span><span class="sxs-lookup"><span data-stu-id="8b762-151">**Win32\_LogicalFileSecuritySetting**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

