---
title: Restoredefaults-Methode der Win32_TSPermissionsSetting-Klasse (Netfw. h)
description: Stellt die standardmäßigen Berechtigungs Satz Werte für das Terminal wieder her.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Restoredefaults-Methode Remotedesktopdienste
- Restoredefaults-Methode Remotedesktopdienste, Win32_TSPermissionsSetting-Klasse
- Win32_TSPermissionsSetting-Klasse Remotedesktopdienste, restoredefaults-Methode
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858802"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="8ff5e-106">Restoredefaults-Methode der Win32 \_ tspermissionssetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="8ff5e-106">RestoreDefaults method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="8ff5e-107">Die **restoredefaults** -Methode stellt die standardmäßigen Berechtigungs Satz Werte für das Terminal wieder her.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-107">The **RestoreDefaults** method restores the default permission set values for the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff5e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ff5e-108">Syntax</span></span>


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a><span data-ttu-id="8ff5e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ff5e-109">Parameters</span></span>

<span data-ttu-id="8ff5e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ff5e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ff5e-111">Return value</span></span>

<span data-ttu-id="8ff5e-112">Gibt bei Erfolg Erfolg zurück, andernfalls fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-112">Returns Success on success, otherwise Failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff5e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ff5e-113">Remarks</span></span>

<span data-ttu-id="8ff5e-114">Die Standard Berechtigungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8ff5e-114">Default permissions are the following:</span></span>

-   <span data-ttu-id="8ff5e-115">Die Konten "Administratoren", "System" und "Remotedesktop Help Assistant" verfügen über alle [Remotedesktopdienste Berechtigungen](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8ff5e-115">The Administrators, System, and Remote Desktop Help Assistant accounts have all [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>
-   <span data-ttu-id="8ff5e-116">Das Remotedesktop Benutzerkonto verfügt über die Berechtigungen anmelden, verbinden, Abfrage Informationen und Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-116">The Remote Desktop Users account has Logon, Connect, Query Information, and Send Message permission.</span></span>
-   <span data-ttu-id="8ff5e-117">Die Konten "lokaler Dienst" und "Netzwerkdienst" verfügen über Abfrage Informationen und die Berechtigung "Nachricht senden".</span><span class="sxs-lookup"><span data-stu-id="8ff5e-117">The Local Service and Network Service accounts have Query Information, and Send Message permission.</span></span>

<span data-ttu-id="8ff5e-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8ff5e-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8ff5e-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8ff5e-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8ff5e-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff5e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ff5e-122">Requirements</span></span>



| <span data-ttu-id="8ff5e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ff5e-123">Requirement</span></span> | <span data-ttu-id="8ff5e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8ff5e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff5e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ff5e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff5e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ff5e-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ff5e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ff5e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff5e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ff5e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ff5e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ff5e-129">Namespace</span></span><br/>                | <span data-ttu-id="8ff5e-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8ff5e-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8ff5e-131">Header</span><span class="sxs-lookup"><span data-stu-id="8ff5e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ff5e-132"><dt>Netfw. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff5e-132"><dt>Netfw.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ff5e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8ff5e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ff5e-134"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8ff5e-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ff5e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8ff5e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ff5e-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ff5e-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff5e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ff5e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff5e-138">**Win32- \_ tspermissionssetting**</span><span class="sxs-lookup"><span data-stu-id="8ff5e-138">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

