---
title: Addaccount-Methode der Win32_TSPermissionsSetting-Klasse (faxcomex. h)
description: Die addaccount-Methode bereitet das Hinzufügen eines Kontos zum Terminal mit dem angegebenen Berechtigungs Satz vor. Sie können Benutzer, Gruppen oder Computer hinzufügen.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Addaccount-Methode Remotedesktopdienste
- Addaccount-Methode Remotedesktopdienste, Win32_TSPermissionsSetting-Klasse
- Win32_TSPermissionsSetting-Klasse Remotedesktopdienste, addaccount-Methode
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477697"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="17f05-107">Addaccount-Methode der Win32 \_ tspermissionssetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="17f05-107">AddAccount method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="17f05-108">Die **addaccount** -Methode bereitet das Hinzufügen eines Kontos zum Terminal mit dem angegebenen Berechtigungs Satz vor.</span><span class="sxs-lookup"><span data-stu-id="17f05-108">The **AddAccount** method prepares to add an account to the terminal with the specified permission set.</span></span> <span data-ttu-id="17f05-109">Sie können Benutzer, Gruppen oder Computer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="17f05-109">You can add users, groups, or computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f05-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="17f05-110">Syntax</span></span>


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a><span data-ttu-id="17f05-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="17f05-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f05-112">*Accountname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17f05-112">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17f05-113">Der Name des Kontos, das dem Terminal hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17f05-113">The name of the account to add to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="17f05-114">*Permissionvoreinstellung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17f05-114">*PermissionPreSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17f05-115">Der Satz von Berechtigungen, die dem angegebenen Konto zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17f05-115">The set of permissions to associate with the specified account.</span></span> <span data-ttu-id="17f05-116">Dieser Parameter kann einen oder alle der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="17f05-116">This parameter can be any or all of the following values.</span></span> <span data-ttu-id="17f05-117">Weitere Informationen finden Sie unter [Remotedesktopdienste Berechtigungen](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="17f05-117">For more information, see [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span data-ttu-id="17f05-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WinStation \_ Gast \_ Zugriff** (0)</span><span class="sxs-lookup"><span data-stu-id="17f05-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION\_GUEST\_ACCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="17f05-119">Das Konto verfügt über die Berechtigung "Anmelden".</span><span class="sxs-lookup"><span data-stu-id="17f05-119">The account has Logon permission.</span></span>

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span data-ttu-id="17f05-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WinStation \_ Benutzer \_ Zugriff** (1)</span><span class="sxs-lookup"><span data-stu-id="17f05-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION\_USER\_ACCESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="17f05-121">Das Konto verfügt über die folgenden Berechtigungen: Anmeldung, Abfrage Informationen, Nachricht senden und verbinden.</span><span class="sxs-lookup"><span data-stu-id="17f05-121">The account has the following permissions: Logon, Query Information, Send Message, and Connect.</span></span>

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span data-ttu-id="17f05-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WinStation \_ Alle \_ Zugriffs** Rechte (2)</span><span class="sxs-lookup"><span data-stu-id="17f05-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION\_ALL\_ACCESS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="17f05-123">Das Konto verfügt über alle Remotedesktopdienste Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="17f05-123">The account has all Remote Desktop Services Permissions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17f05-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17f05-124">Return value</span></span>

<span data-ttu-id="17f05-125">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17f05-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="17f05-126">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="17f05-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="17f05-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17f05-127">Remarks</span></span>

<span data-ttu-id="17f05-128">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="17f05-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17f05-129">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="17f05-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="17f05-130">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="17f05-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17f05-131">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="17f05-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="17f05-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17f05-132">Requirements</span></span>



| <span data-ttu-id="17f05-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17f05-133">Requirement</span></span> | <span data-ttu-id="17f05-134">Wert</span><span class="sxs-lookup"><span data-stu-id="17f05-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17f05-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17f05-135">Minimum supported client</span></span><br/> | <span data-ttu-id="17f05-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17f05-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17f05-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17f05-137">Minimum supported server</span></span><br/> | <span data-ttu-id="17f05-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17f05-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17f05-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="17f05-139">Namespace</span></span><br/>                | <span data-ttu-id="17f05-140">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="17f05-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="17f05-141">Header</span><span class="sxs-lookup"><span data-stu-id="17f05-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="17f05-142"><dt>Faxcomex. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f05-142"><dt>Faxcomex.h</dt></span></span> </dl>   |
| <span data-ttu-id="17f05-143">MOF</span><span class="sxs-lookup"><span data-stu-id="17f05-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17f05-144"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="17f05-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="17f05-145">DLL</span><span class="sxs-lookup"><span data-stu-id="17f05-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17f05-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17f05-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f05-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17f05-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f05-148">**Win32- \_ tspermissionssetting**</span><span class="sxs-lookup"><span data-stu-id="17f05-148">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

