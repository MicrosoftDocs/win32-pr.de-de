---
title: Modifyberechtigungs-Methode der Win32_TSAccount-Klasse
description: Legt eine Berechtigung für das angegebene Konto fest.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Modifyberechtigungs-Methode Remotedesktopdienste
- Modifyberechtigungs Methode Remotedesktopdienste, Win32_TSAccount-Klasse
- Win32_TSAccount-Klasse Remotedesktopdienste, modifyberechtigungs Methode
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339565"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="221d1-106">Modifyberechtigungs-Methode der Win32- \_ Klasse "zaccount"</span><span class="sxs-lookup"><span data-stu-id="221d1-106">ModifyPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="221d1-107">Legt eine Berechtigung für das angegebene Konto fest.</span><span class="sxs-lookup"><span data-stu-id="221d1-107">Sets a permission for the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="221d1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="221d1-108">Syntax</span></span>


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a><span data-ttu-id="221d1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="221d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="221d1-110">*PermissionMask* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="221d1-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221d1-111">Die [Remotedesktop-Sitzungshost](terminal-services-permissions.md) festzulegende Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="221d1-111">The [Remote Desktop Session Host Permission](terminal-services-permissions.md) to set.</span></span>

<span data-ttu-id="221d1-112">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="221d1-112">The possible values are:</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="221d1-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WinStation \_ Abfrage** (0)</span><span class="sxs-lookup"><span data-stu-id="221d1-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-114">Berechtigung zum Abfragen von Informationen über eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="221d1-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="221d1-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WinStation \_ Set** (1)</span><span class="sxs-lookup"><span data-stu-id="221d1-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-116">Berechtigung zum Ändern von Verbindungsparametern.</span><span class="sxs-lookup"><span data-stu-id="221d1-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="221d1-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WinStation \_ Zurücksetzen** (6)</span><span class="sxs-lookup"><span data-stu-id="221d1-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-118">Berechtigung zum Zurücksetzen oder Beenden einer Sitzung oder einer Verbindung.</span><span class="sxs-lookup"><span data-stu-id="221d1-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="221d1-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WinStation \_ \| \_ \_ Erforderliche virtuelle Standard Rechte** (3)</span><span class="sxs-lookup"><span data-stu-id="221d1-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-120">Berechtigung zum Verwenden von virtuellen Kanälen.</span><span class="sxs-lookup"><span data-stu-id="221d1-120">Permission to use virtual channels.</span></span> <span data-ttu-id="221d1-121">Virtuelle Kanäle ermöglichen den Zugriff von einem Serverprogramm auf Client Geräte.</span><span class="sxs-lookup"><span data-stu-id="221d1-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="221d1-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WinStation \_ Schatten** (4)</span><span class="sxs-lookup"><span data-stu-id="221d1-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-123">Berechtigung, um die Sitzung eines anderen Benutzers zu überschatten oder Remote zu steuern.</span><span class="sxs-lookup"><span data-stu-id="221d1-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="221d1-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WinStation \_ Anmelden** (5)</span><span class="sxs-lookup"><span data-stu-id="221d1-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-125">Berechtigung zum Anmelden bei einer Sitzung auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="221d1-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="221d1-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WinStation \_ Abmeldung (2** )</span><span class="sxs-lookup"><span data-stu-id="221d1-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-127">Berechtigung zum Abmelden eines Benutzers von einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="221d1-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="221d1-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WinStation \_ Meldung (7** )</span><span class="sxs-lookup"><span data-stu-id="221d1-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-129">Die Berechtigung zum Senden einer Nachricht an die Sitzung eines anderen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="221d1-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="221d1-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WinStation \_ Verbinden** (8)</span><span class="sxs-lookup"><span data-stu-id="221d1-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-131">Berechtigung zum Herstellen einer Verbindung mit einer anderen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="221d1-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="221d1-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WinStation \_ Trennen** (9)</span><span class="sxs-lookup"><span data-stu-id="221d1-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="221d1-133">Berechtigung zum Trennen einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="221d1-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="221d1-134">*Zulassen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="221d1-134">*Allow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221d1-135">Gibt an, ob die Berechtigung im *PermissionMask* -Parameter zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="221d1-135">Specifies whether the permission in the *PermissionMask* parameter is allowed or denied.</span></span>

<span data-ttu-id="221d1-136">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="221d1-136">The possible values are:</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="221d1-137"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="221d1-137"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="221d1-138">Der angegebene Berechtigungs Satz ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="221d1-138">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="221d1-139"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="221d1-139"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="221d1-140">Der angegebene Berechtigungs Satz wird verweigert.</span><span class="sxs-lookup"><span data-stu-id="221d1-140">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="221d1-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="221d1-141">Return value</span></span>

<span data-ttu-id="221d1-142">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="221d1-142">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="221d1-143">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="221d1-143">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="221d1-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="221d1-144">Remarks</span></span>

<span data-ttu-id="221d1-145">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="221d1-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="221d1-146">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="221d1-146">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="221d1-147">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="221d1-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="221d1-148">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="221d1-148">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="221d1-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="221d1-149">Requirements</span></span>



| <span data-ttu-id="221d1-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="221d1-150">Requirement</span></span> | <span data-ttu-id="221d1-151">Wert</span><span class="sxs-lookup"><span data-stu-id="221d1-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="221d1-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="221d1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="221d1-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="221d1-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="221d1-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="221d1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="221d1-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="221d1-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="221d1-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="221d1-156">Namespace</span></span><br/>                | <span data-ttu-id="221d1-157">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="221d1-157">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="221d1-158">MOF</span><span class="sxs-lookup"><span data-stu-id="221d1-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="221d1-159"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="221d1-159"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="221d1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="221d1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="221d1-161"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="221d1-161"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="221d1-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="221d1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="221d1-163">**Win32- \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="221d1-163">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

