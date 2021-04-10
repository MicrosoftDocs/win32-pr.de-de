---
title: Create-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Erstellt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap) unter Verwendung der angegebenen Werte. Die neue RD \ 160; Die Obergrenze wird am oberen Rand des RD \ 160; eingefügt. Cap-Auswertungs Reihenfolge mit einem Order-Eigenschafts Wert von \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Create-Methode Remotedesktopdienste
- Create Method Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste, Methode erstellen
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040273"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="ddb50-107">Create-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="ddb50-107">Create method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="ddb50-108">Erstellt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP) mithilfe der angegebenen Werte.</span><span class="sxs-lookup"><span data-stu-id="ddb50-108">Creates a Remote Desktop connection authorization policy (RD CAP) by using the specified values.</span></span> <span data-ttu-id="ddb50-109">Die neue RD-Obergrenze wird am oberen Rand der Auswertungs Reihenfolge für die RD-CAP eingefügt, wobei der Wert für die **Order** -Eigenschaft "1" lautet.</span><span class="sxs-lookup"><span data-stu-id="ddb50-109">The new RD CAP will be inserted at the top of the RD CAP evaluation order, with an **Order** property value of "1".</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb50-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb50-110">Syntax</span></span>


```mof
uint32 Create(
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



## <a name="parameters"></a><span data-ttu-id="ddb50-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb50-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddb50-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-113">Name der RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="ddb50-113">Name of the RD CAP.</span></span> <span data-ttu-id="ddb50-114">Der Name muss 64 Zeichen oder kleiner, eindeutig (Groß-/Kleinschreibung wird ignoriert) sein und darf die folgenden reservierten Zeichen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="ddb50-114">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="ddb50-115"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="ddb50-115"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="ddb50-116">\*\[Registerkarte\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-116">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-117">*Usergroupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-117">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-118">Eine Liste von Benutzergruppen Namen, die durch Semikolons getrennt sind, für die neue RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="ddb50-118">List of user group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-119">*Computer groupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-120">Die Liste der Computer Gruppennamen, die durch Semikolons getrennt sind, für die neue RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="ddb50-120">List of computer group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-121">*Smartcard* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-121">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-122">Gibt an, ob Smartcards zum Authentifizieren beim RD-Gateway Server verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ddb50-122">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-123">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-123">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-124">Gibt an, ob Kenn Wörter verwendet werden können, um sich beim RD-Gateway Server zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="ddb50-124">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-125">*SecureID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-125">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-126">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ddb50-126">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-127">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-128">Gibt an, ob dieses RD-CAP aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ddb50-128">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-129">*Deviceredirectiontype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-129">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-130">Gibt an, welche Gerätetypen umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb50-130">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="ddb50-131">0</span><span class="sxs-lookup"><span data-stu-id="ddb50-131">0</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-132">Alle Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ddb50-132">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-133">1</span><span class="sxs-lookup"><span data-stu-id="ddb50-133">1</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-134">Keine Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ddb50-134">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-135">2</span><span class="sxs-lookup"><span data-stu-id="ddb50-135">2</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-136">Angegebene Geräte werden nicht umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ddb50-136">Specified devices will not be redirected.</span></span> <span data-ttu-id="ddb50-137">Die Parameter *diskdrivesdebug*, *printersdeaktiviert*, *serialportsdeaktiviert*, *clipboarddeaktiviert* und *plugandplaydevicesdeaktiviert* steuern, welche Geräte nicht umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb50-137">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ddb50-138">*Diskdrivesdeaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-138">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-139">Gibt an, ob die Laufwerk Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="ddb50-139">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-140">" *Printersdeaktiviert* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-140">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-141">Gibt an, ob die Drucker Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="ddb50-141">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-142">*Serialportsdeaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-142">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-143">Gibt an, ob die serielle Port Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.</span><span class="sxs-lookup"><span data-stu-id="ddb50-143">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-144">*Clipboarddeaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-144">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-145">Gibt an, ob die Zwischenablage Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.</span><span class="sxs-lookup"><span data-stu-id="ddb50-145">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-146">*Plugandplaydevicesdeaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-146">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-147">Gibt an, ob die Umleitung von Plug & Play Geräten deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.</span><span class="sxs-lookup"><span data-stu-id="ddb50-147">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-148">*IdleTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-148">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-149">Leerlauf Timeout Wert in Minuten</span><span class="sxs-lookup"><span data-stu-id="ddb50-149">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-150">*Sessiontimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-150">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-151">Sitzungs Timeout Wert in Minuten</span><span class="sxs-lookup"><span data-stu-id="ddb50-151">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-152">*Sessiontimeoutaction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-152">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-153">Sitzungs Timeout Aktion in Minuten</span><span class="sxs-lookup"><span data-stu-id="ddb50-153">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-154">" *Zuweisung der Server* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-154">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-155">Gibt an, ob Verbindungen nur für Server mit SZR zulässig sind</span><span class="sxs-lookup"><span data-stu-id="ddb50-155">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="ddb50-156">*Cookieauthentifizierung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ddb50-156">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb50-157">Gibt an, ob für die Verbindung mit dem Terminaldienstegateway-Server eine Cookie-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="ddb50-157">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddb50-158">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddb50-158">Return value</span></span>

<span data-ttu-id="ddb50-159">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ddb50-159">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ddb50-160">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ddb50-160">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ddb50-161">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ddb50-161">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb50-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddb50-162">Remarks</span></span>

<span data-ttu-id="ddb50-163">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ddb50-163">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ddb50-164">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="ddb50-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ddb50-165">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="ddb50-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ddb50-166">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddb50-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ddb50-167">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ddb50-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb50-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddb50-168">Requirements</span></span>



| <span data-ttu-id="ddb50-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddb50-169">Requirement</span></span> | <span data-ttu-id="ddb50-170">Wert</span><span class="sxs-lookup"><span data-stu-id="ddb50-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb50-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddb50-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb50-172">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ddb50-172">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ddb50-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddb50-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb50-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddb50-174">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ddb50-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddb50-175">Namespace</span></span><br/>                | <span data-ttu-id="ddb50-176">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ddb50-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ddb50-177">MOF</span><span class="sxs-lookup"><span data-stu-id="ddb50-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddb50-178"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="ddb50-178"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddb50-179">DLL</span><span class="sxs-lookup"><span data-stu-id="ddb50-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb50-180"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddb50-180"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ddb50-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddb50-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb50-182">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="ddb50-182">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

