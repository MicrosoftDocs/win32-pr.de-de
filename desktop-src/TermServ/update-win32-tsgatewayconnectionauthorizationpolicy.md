---
title: Update-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Aktualisiert die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Update-Methode Remotedesktopdienste
- Update-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, Update-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040682"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="b072b-106">Update-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="b072b-106">Update method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="b072b-107">Aktualisiert die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP).</span><span class="sxs-lookup"><span data-stu-id="b072b-107">Updates the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="b072b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b072b-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a><span data-ttu-id="b072b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b072b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b072b-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-111">Name der RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="b072b-111">Name of the RD CAP.</span></span> <span data-ttu-id="b072b-112">Der Name muss 64 Zeichen oder kleiner, eindeutig (Groß-/Kleinschreibung wird ignoriert) sein und darf die folgenden reservierten Zeichen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="b072b-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="b072b-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="b072b-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="b072b-114">\*\[Registerkarte\]</span><span class="sxs-lookup"><span data-stu-id="b072b-114">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="b072b-115">*Usergroupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-115">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-116">Liste von durch Semikolon getrennten Benutzergruppen Namen.</span><span class="sxs-lookup"><span data-stu-id="b072b-116">List of semicolon-separated user group names.</span></span> <span data-ttu-id="b072b-117">Die Namen weisen das Format *Domäne \\ usergroupname* auf.</span><span class="sxs-lookup"><span data-stu-id="b072b-117">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="b072b-118">Wenn der Benutzer zu einer dieser Benutzergruppen gehört, erhält der Benutzer Zugriff auf den RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="b072b-118">If the user belongs to any one of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-119">*Computer groupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-120">Liste von durch Semikolons getrennten Computer Gruppennamen.</span><span class="sxs-lookup"><span data-stu-id="b072b-120">List of semicolon-separated machine group names.</span></span> <span data-ttu-id="b072b-121">Dieser Wert kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="b072b-121">This value can be empty.</span></span> <span data-ttu-id="b072b-122">Die Namen weisen das Format *Domäne \\ computergroupname* auf.</span><span class="sxs-lookup"><span data-stu-id="b072b-122">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="b072b-123">Wenn ein Wert angegeben wird, muss der Client Computer zu einer dieser Computer Gruppen gehören, damit der Benutzer auf den RD-Gateway Server zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="b072b-123">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-124">*Smartcard* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-124">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-125">Gibt an, ob Smartcards zum Authentifizieren beim RD-Gateway Server verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b072b-125">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-126">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-126">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-127">Gibt an, ob Kenn Wörter verwendet werden können, um sich beim RD-Gateway Server zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="b072b-127">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-128">*SecureID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-128">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-129">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b072b-129">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-130">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-130">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-131">Gibt an, ob dieses RD-CAP aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b072b-131">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-132">*Deviceredirectiontype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-132">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-133">Gibt an, welche Gerätetypen umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b072b-133">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="b072b-134">0</span><span class="sxs-lookup"><span data-stu-id="b072b-134">0</span></span>
</dt> <dd>

<span data-ttu-id="b072b-135">Alle Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b072b-135">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-136">1</span><span class="sxs-lookup"><span data-stu-id="b072b-136">1</span></span>
</dt> <dd>

<span data-ttu-id="b072b-137">Keine Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b072b-137">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="b072b-138">2</span><span class="sxs-lookup"><span data-stu-id="b072b-138">2</span></span>
</dt> <dd>

<span data-ttu-id="b072b-139">Angegebene Geräte werden nicht umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b072b-139">Specified devices will not be redirected.</span></span> <span data-ttu-id="b072b-140">Die Parameter *diskdrivesdebug*, *printersdeaktiviert*, *serialportsdeaktiviert*, *clipboarddeaktiviert* und *plugandplaydevicesdeaktiviert* steuern, welche Geräte nicht umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b072b-140">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b072b-141">*Diskdrivesdeaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-141">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-142">Gibt an, ob die Laufwerk Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="b072b-142">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b072b-143">" *Printersdeaktiviert* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-143">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-144">Gibt an, ob die Drucker Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="b072b-144">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b072b-145">*Serialportsdeaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-145">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-146">Gibt an, ob die serielle Port Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.</span><span class="sxs-lookup"><span data-stu-id="b072b-146">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b072b-147">*Clipboarddeaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-147">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-148">Gibt an, ob die Zwischenablage Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.</span><span class="sxs-lookup"><span data-stu-id="b072b-148">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b072b-149">*Plugandplaydevicesdeaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-149">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-150">Gibt an, ob die Umleitung von Plug & Play Geräten deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.</span><span class="sxs-lookup"><span data-stu-id="b072b-150">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b072b-151">*IdleTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-151">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-152">Leerlauf Timeout Wert in Minuten</span><span class="sxs-lookup"><span data-stu-id="b072b-152">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="b072b-153">*Sessiontimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-153">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-154">Sitzungs Timeout Wert in Minuten</span><span class="sxs-lookup"><span data-stu-id="b072b-154">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="b072b-155">*Sessiontimeoutaction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-155">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-156">Sitzungs Timeout Aktion in Minuten</span><span class="sxs-lookup"><span data-stu-id="b072b-156">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="b072b-157">" *Zuweisung der Server* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-157">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-158">Gibt an, ob Verbindungen nur für Server mit SZR zulässig sind</span><span class="sxs-lookup"><span data-stu-id="b072b-158">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="b072b-159">*Cookieauthentifizierung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b072b-159">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b072b-160">Gibt an, ob für die Verbindung mit dem Terminaldienstegateway-Server eine Cookie-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="b072b-160">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b072b-161">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b072b-161">Return value</span></span>

<span data-ttu-id="b072b-162">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b072b-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b072b-163">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b072b-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b072b-164">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b072b-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b072b-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b072b-165">Remarks</span></span>

<span data-ttu-id="b072b-166">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b072b-166">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b072b-167">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b072b-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b072b-168">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b072b-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b072b-169">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b072b-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b072b-170">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b072b-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b072b-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b072b-171">Requirements</span></span>



| <span data-ttu-id="b072b-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b072b-172">Requirement</span></span> | <span data-ttu-id="b072b-173">Wert</span><span class="sxs-lookup"><span data-stu-id="b072b-173">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b072b-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b072b-174">Minimum supported client</span></span><br/> | <span data-ttu-id="b072b-175">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b072b-175">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b072b-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b072b-176">Minimum supported server</span></span><br/> | <span data-ttu-id="b072b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b072b-177">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b072b-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="b072b-178">Namespace</span></span><br/>                | <span data-ttu-id="b072b-179">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b072b-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b072b-180">MOF</span><span class="sxs-lookup"><span data-stu-id="b072b-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b072b-181"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b072b-181"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b072b-182">DLL</span><span class="sxs-lookup"><span data-stu-id="b072b-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b072b-183"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b072b-183"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b072b-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b072b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b072b-185">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="b072b-185">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

