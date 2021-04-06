---
title: Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Beschreibt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap). RD \ 160; Mithilfe von Caps kann festgestellt werden, ob ein Benutzer eine Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) herstellen darf.
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858838"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="f99ae-106">Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="f99ae-106">Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="f99ae-107">Beschreibt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP).</span><span class="sxs-lookup"><span data-stu-id="f99ae-107">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="f99ae-108">RD-CAPs werden verwendet, um zu bestimmen, ob ein Benutzer eine Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="f99ae-108">RD CAPs are used to determine whether a user is allowed to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99ae-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f99ae-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a><span data-ttu-id="f99ae-110">Member</span><span class="sxs-lookup"><span data-stu-id="f99ae-110">Members</span></span>

<span data-ttu-id="f99ae-111">Die Win32-Klasse " **\_ zgatewayconnectionauthorizationpolicy** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f99ae-111">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="f99ae-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f99ae-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f99ae-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f99ae-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f99ae-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="f99ae-114">Methods</span></span>

<span data-ttu-id="f99ae-115">Die Win32-Klasse " **\_ zgatewayconnectionauthorizationpolicy** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-115">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="f99ae-116">Methode</span><span class="sxs-lookup"><span data-stu-id="f99ae-116">Method</span></span>                                                                                                                | <span data-ttu-id="f99ae-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f99ae-117">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f99ae-118">**Addcomputergroupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-118">**AddComputerGroupNames**</span></span>](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="f99ae-119">Fügt die angegebenen Computer Gruppennamen der **computergroupnames** -Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="f99ae-119">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span><br/>                                                                                      |
| [<span data-ttu-id="f99ae-120">**Addusergroupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-120">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="f99ae-121">Fügt die angegebenen Benutzergruppen Namen der **usergroupnames** -Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="f99ae-121">Adds the specified user group names to the **UserGroupNames** property.</span></span><br/>                                                                                              |
| [<span data-ttu-id="f99ae-122">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="f99ae-122">**Create**</span></span>](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="f99ae-123">Erstellt eine RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="f99ae-123">Creates an RD CAP.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="f99ae-124">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="f99ae-124">**Delete**</span></span>](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="f99ae-125">Löscht die aktuelle RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="f99ae-125">Deletes the current RD CAP.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="f99ae-126">**Disableclipboard**</span><span class="sxs-lookup"><span data-stu-id="f99ae-126">**DisableClipboard**</span></span>](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | <span data-ttu-id="f99ae-127">Legt die **clipboarddeaktiviert** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-127">Sets the **ClipboardDisabled** property.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="f99ae-128">**Disablediskdrives**</span><span class="sxs-lookup"><span data-stu-id="f99ae-128">**DisableDiskDrives**</span></span>](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="f99ae-129">Legt die **diskdrivesdeaktivierte** Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-129">Sets the **DiskDrivesDisabled** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="f99ae-130">**Disableplugandplaydevices**</span><span class="sxs-lookup"><span data-stu-id="f99ae-130">**DisablePlugAndPlayDevices**</span></span>](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | <span data-ttu-id="f99ae-131">Legt die **plugandplaydevicesdeaktiviert** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-131">Sets the **PlugAndPlayDevicesDisabled** property.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="f99ae-132">**Disableprinter**</span><span class="sxs-lookup"><span data-stu-id="f99ae-132">**DisablePrinters**</span></span>](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | <span data-ttu-id="f99ae-133">Legt die **printersdeaktiviert** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-133">Sets the **PrintersDisabled** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f99ae-134">**Disableserialports**</span><span class="sxs-lookup"><span data-stu-id="f99ae-134">**DisableSerialPorts**</span></span>](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="f99ae-135">Legt die **serialportsdeaktiviert** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-135">Sets the **SerialPortsDisabled** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="f99ae-136">**Enablezugewonlysdrservers**</span><span class="sxs-lookup"><span data-stu-id="f99ae-136">**EnableAllowOnlySDRServers**</span></span>](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | <span data-ttu-id="f99ae-137">Dient **zum Umschalten der Eigenschaft** "" der Eigenschaft "Eigenschaft".</span><span class="sxs-lookup"><span data-stu-id="f99ae-137">Used to toggle the **AllowOnlySDRServers** property</span></span><br/> <span data-ttu-id="f99ae-138">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                  |
| [<span data-ttu-id="f99ae-139">**Nach unten**</span><span class="sxs-lookup"><span data-stu-id="f99ae-139">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | <span data-ttu-id="f99ae-140">Verschiebt die aktuelle RD-Obergrenze in der Liste um eine Position nach unten.</span><span class="sxs-lookup"><span data-stu-id="f99ae-140">Moves the current RD CAP one position down in the list.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f99ae-141">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="f99ae-141">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="f99ae-142">Verschiebt die aktuelle RD-Obergrenze in der Liste um eine Position nach oben.</span><span class="sxs-lookup"><span data-stu-id="f99ae-142">Moves the current RD CAP one position up in the list.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="f99ae-143">**Removecomputergroupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-143">**RemoveComputerGroupNames**</span></span>](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="f99ae-144">Entfernt die angegebenen Computer Gruppennamen aus der **computergroupnames** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f99ae-144">Removes the specified computer group names from the **ComputerGroupNames** property.</span></span><br/>                                                                                 |
| [<span data-ttu-id="f99ae-145">**Removeusergroupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-145">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | <span data-ttu-id="f99ae-146">Entfernt die angegebenen Benutzergruppen Namen aus der **usergroupnames** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f99ae-146">Removes specified user group names from the **UserGroupNames** property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="f99ae-147">**Setcomputergroupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-147">**SetComputerGroupNames**</span></span>](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="f99ae-148">Legt die **computergroupnames** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-148">Sets the **ComputerGroupNames** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="f99ae-149">**Setcookieauthenticationallowed**</span><span class="sxs-lookup"><span data-stu-id="f99ae-149">**SetCookieAuthenticationAllowed**</span></span>](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | <span data-ttu-id="f99ae-150">Legt die **cookieauthenticationallowed** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-150">Sets the **CookieAuthenticationAllowed** property.</span></span><br/> <span data-ttu-id="f99ae-151">**Windows Server 2008:** Diese Methode ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-151">**Windows Server 2008:** This method is not available.</span></span><br/>                                                 |
| [<span data-ttu-id="f99ae-152">**Setdeviceredirectiontype**</span><span class="sxs-lookup"><span data-stu-id="f99ae-152">**SetDeviceRedirectionType**</span></span>](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="f99ae-153">Legt die **deviceredirectiontype** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-153">Sets the **DeviceRedirectionType** property.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="f99ae-154">**Abgeleitete**</span><span class="sxs-lookup"><span data-stu-id="f99ae-154">**SetEnabled**</span></span>](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | <span data-ttu-id="f99ae-155">Aktiviert oder deaktiviert das aktuelle RD-CAP.</span><span class="sxs-lookup"><span data-stu-id="f99ae-155">Enables or disables the current RD CAP.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f99ae-156">**"-Timeout"**</span><span class="sxs-lookup"><span data-stu-id="f99ae-156">**SetIdleTimeout**</span></span>](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | <span data-ttu-id="f99ae-157">Legt die **IdleTimeout** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-157">Sets the **IdleTimeout** property.</span></span><br/> <span data-ttu-id="f99ae-158">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-158">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                   |
| [<span data-ttu-id="f99ae-159">**SetName**</span><span class="sxs-lookup"><span data-stu-id="f99ae-159">**SetName**</span></span>](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | <span data-ttu-id="f99ae-160">Legt einen neuen Namen für diese RD-Obergrenze fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-160">Sets a new name for this RD CAP.</span></span> <span data-ttu-id="f99ae-161">Mit dieser Methode wird sichergestellt, dass die Namen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="f99ae-161">This method ensures that names will be unique.</span></span><br/>                                                                                      |
| [<span data-ttu-id="f99ae-162">**Setpasswordallowed**</span><span class="sxs-lookup"><span data-stu-id="f99ae-162">**SetPasswordAllowed**</span></span>](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="f99ae-163">Legt die **passwordallowed** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-163">Sets the **PasswordAllowed** property.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="f99ae-164">**Setsecureidallowed zulässig**</span><span class="sxs-lookup"><span data-stu-id="f99ae-164">**SetSecureIdAllowed**</span></span>](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="f99ae-165">Legt die Eigenschaft " **secureidallowed** " fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-165">Sets the **SecureIdAllowed** property.</span></span><br/> <span data-ttu-id="f99ae-166">**Windows Server 2008:** Diese Methode ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f99ae-166">**Windows Server 2008:** This method is reserved for future use.</span></span><br/>                                                   |
| [<span data-ttu-id="f99ae-167">**-Sitzungs Timeout**</span><span class="sxs-lookup"><span data-stu-id="f99ae-167">**SetSessionTimeout**</span></span>](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="f99ae-168">Legt die Eigenschaften **sessiontimeout** und **sessiontimeoutaction** fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-168">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span><br/> <span data-ttu-id="f99ae-169">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/> |
| [<span data-ttu-id="f99ae-170">**"Abkto" ist zulässig.**</span><span class="sxs-lookup"><span data-stu-id="f99ae-170">**SetSmartcardAllowed**</span></span>](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | <span data-ttu-id="f99ae-171">Legt die **smartcardallowed** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-171">Sets the **SmartcardAllowed** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f99ae-172">**Setusergroupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-172">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="f99ae-173">Legt die **usergroupnames** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f99ae-173">Sets the **UserGroupNames** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="f99ae-174">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="f99ae-174">**Update**</span></span>](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="f99ae-175">Aktualisiert das aktuelle RD-CAP.</span><span class="sxs-lookup"><span data-stu-id="f99ae-175">Updates the current RD CAP.</span></span><br/>                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="f99ae-176">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f99ae-176">Properties</span></span>

<span data-ttu-id="f99ae-177">Die Win32-Klasse "t- **\_ gatewayconnectionauthorizationpolicy** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f99ae-177">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f99ae-178">**"Zuweisung der Server"**</span><span class="sxs-lookup"><span data-stu-id="f99ae-178">**AllowOnlySDRServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-179">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-181">Gibt an, ob Verbindungen nur für die Sicherung von RDS-Servern (Geräte Umleitung) zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f99ae-181">Indicates whether connections allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="f99ae-182">Diese Eigenschaft kann mithilfe der [**enablezugewonlysdrservers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-182">This property can be set using the [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) method.</span></span>

<span data-ttu-id="f99ae-183">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-183">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-184">**Clipboarddeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="f99ae-184">**ClipboardDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-185">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-187">Gibt an, ob die Umleitung der Zwischenablage deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f99ae-187">Indicates if clipboard redirection will be disabled.</span></span> <span data-ttu-id="f99ae-188">Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="f99ae-188">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-189">**Computer groupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-189">**ComputerGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f99ae-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-192">Liste von durch Semikolons getrennten Computer Gruppennamen.</span><span class="sxs-lookup"><span data-stu-id="f99ae-192">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="f99ae-193">Dieser Wert kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="f99ae-193">This value can be empty.</span></span> <span data-ttu-id="f99ae-194">Die Namen weisen das Format *Domäne \\ computergroupname* auf.</span><span class="sxs-lookup"><span data-stu-id="f99ae-194">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="f99ae-195">Wenn ein Wert angegeben wird, muss der Client Computer zu einer dieser Computer Gruppen gehören, damit der Benutzer auf den RD-Gateway Server zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f99ae-195">If a value is specified, then the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-196">**Cookieauthenticationallowed**</span><span class="sxs-lookup"><span data-stu-id="f99ae-196">**CookieAuthenticationAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-197">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-199">Gibt an, ob eine Cookie-Authentifizierung zum Herstellen einer Verbindung mit dem RD-Gateway Server verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f99ae-199">Indicates if cookie authentication can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="f99ae-200">Diese Eigenschaft kann mit der [**setcookieauthenticationallowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-200">This property can be set by using the [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="f99ae-201">**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-201">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-202">**Deviceredirectiontype**</span><span class="sxs-lookup"><span data-stu-id="f99ae-202">**DeviceRedirectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-203">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f99ae-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-205">Gibt an, welche Geräte umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-205">Specifies which devices will be redirected.</span></span>

<dt>

<span data-ttu-id="f99ae-206">0</span><span class="sxs-lookup"><span data-stu-id="f99ae-206">0</span></span>
</dt> <dd>

<span data-ttu-id="f99ae-207">Alle Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f99ae-207">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-208">1</span><span class="sxs-lookup"><span data-stu-id="f99ae-208">1</span></span>
</dt> <dd>

<span data-ttu-id="f99ae-209">Keine Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f99ae-209">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-210">2</span><span class="sxs-lookup"><span data-stu-id="f99ae-210">2</span></span>
</dt> <dd>

<span data-ttu-id="f99ae-211">Angegebene Geräte werden nicht umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f99ae-211">Specified devices will not be redirected.</span></span> <span data-ttu-id="f99ae-212">Die Eigenschaften **diskdrivesdeaktiviert**, **printersdeaktiviert**, **serialportsdeaktiviert**, **clipboarddeaktiviert** und **plugandplaydevicesdeaktiviert** steuern, welche Geräte nicht umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-212">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f99ae-213">**Diskdrivesdeaktivierte**</span><span class="sxs-lookup"><span data-stu-id="f99ae-213">**DiskDrivesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-214">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-216">Gibt an, ob die Laufwerk Umleitung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f99ae-216">Indicates if disk drive redirection will be disabled.</span></span> <span data-ttu-id="f99ae-217">Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="f99ae-217">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-218">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="f99ae-218">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-221">Gibt an, ob dieses RD-CAP zum Auswerten eines Benutzers für die Autorisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f99ae-221">Indicates whether this RD CAP will be used to evaluate a user for authorization.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-222">**Hasnapattributes**</span><span class="sxs-lookup"><span data-stu-id="f99ae-222">**HasNapAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-223">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-225">Gibt an, ob die RD-Abdeckung Network Access Protection (NAP)-Attribute verwendet.</span><span class="sxs-lookup"><span data-stu-id="f99ae-225">Indicates if the RD CAP uses Network Access Protection (NAP) attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-226">**IdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="f99ae-226">**IdleTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-227">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f99ae-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-229">Der Wert für das Leerlauf Timeout (in Minuten).</span><span class="sxs-lookup"><span data-stu-id="f99ae-229">The idle timeout value, in minutes.</span></span> <span data-ttu-id="f99ae-230">Der Wert 0 bedeutet, dass kein Timeout vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f99ae-230">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="f99ae-231">Diese Eigenschaft kann mit der [**setidletimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-231">This property can be set by using the [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="f99ae-232">**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-232">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-233">**Name**</span><span class="sxs-lookup"><span data-stu-id="f99ae-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f99ae-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-236">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f99ae-236">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-237">Name der RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="f99ae-237">Name of the RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-238">**Order**</span><span class="sxs-lookup"><span data-stu-id="f99ae-238">**Order**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-239">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f99ae-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-241">Auswertungs Reihenfolge für die RD-CAP.</span><span class="sxs-lookup"><span data-stu-id="f99ae-241">Evaluation order of the RD CAP.</span></span> <span data-ttu-id="f99ae-242">Das erste ausgewertete RD-CAP weist den Wert "1" auf.</span><span class="sxs-lookup"><span data-stu-id="f99ae-242">The first RD CAP evaluated has a value of "1".</span></span> <span data-ttu-id="f99ae-243">Die **Order** -Eigenschaft kann geändert werden, wenn die Methoden [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**moveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)oder [**muvedown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-243">The **Order** property can be changed when the [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md), or [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-244">**Passwordallowed**</span><span class="sxs-lookup"><span data-stu-id="f99ae-244">**PasswordAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-245">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-247">Gibt an, ob ein Kennwort zum Herstellen einer Verbindung mit dem RD-Gateway Server verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f99ae-247">Indicates if a password can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="f99ae-248">Diese Eigenschaft kann mithilfe der [**setpasswordallowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-248">This property can be changed by using the [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-249">**Plugandplaydevicesdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="f99ae-249">**PlugAndPlayDevicesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-250">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-252">Gibt an, ob die Umleitung von Plug & Play Geräten deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f99ae-252">Indicates if redirection of Plug and Play devices will be disabled.</span></span> <span data-ttu-id="f99ae-253">Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="f99ae-253">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-254">**"Printersdeaktiviert"**</span><span class="sxs-lookup"><span data-stu-id="f99ae-254">**PrintersDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-255">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-257">Gibt an, ob die Drucker Umleitung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f99ae-257">Indicates if printer redirection will be disabled.</span></span> <span data-ttu-id="f99ae-258">Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="f99ae-258">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-259">**Secureidallowed zulässig**</span><span class="sxs-lookup"><span data-stu-id="f99ae-259">**SecureIdAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-260">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-260">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-262">Gibt an, ob ein sicherer Bezeichner verwendet werden kann, um eine Verbindung mit dem RD-Gateway-Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f99ae-262">Indicates if a secure identifier can be used to connect to the RD Gateway server.</span></span>

<span data-ttu-id="f99ae-263">**Windows Server 2008:** Diese Eigenschaft wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f99ae-263">**Windows Server 2008:** This property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-264">**Serialportsdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="f99ae-264">**SerialPortsDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-265">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-267">Gibt an, ob die serielle Port Umleitung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f99ae-267">Indicates if serial port redirection will be disabled.</span></span> <span data-ttu-id="f99ae-268">Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="f99ae-268">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-269">**SessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="f99ae-269">**SessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-270">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f99ae-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-272">Der Sitzungs Timeout Wert (in Minuten).</span><span class="sxs-lookup"><span data-stu-id="f99ae-272">The session timeout value, in minutes.</span></span> <span data-ttu-id="f99ae-273">Der Wert 0 bedeutet, dass kein Timeout vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f99ae-273">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="f99ae-274">Diese Eigenschaft kann mit der [**sezessiontimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-274">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="f99ae-275">**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-275">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-276">**Sessiontimeoutaction**</span><span class="sxs-lookup"><span data-stu-id="f99ae-276">**SessionTimeoutAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-277">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f99ae-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-279">Gibt die Aktion an, die bei einem Sitzungs Timeout durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f99ae-279">Specifies the action to be taken in the case of a session timeout.</span></span> <span data-ttu-id="f99ae-280">Diese Eigenschaft kann mit der [**sezessiontimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-280">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="f99ae-281">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="f99ae-281">This can be one of the following values.</span></span>

<span data-ttu-id="f99ae-282">**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f99ae-282">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="f99ae-283">0</span><span class="sxs-lookup"><span data-stu-id="f99ae-283">0</span></span>
</dt> <dd>

<span data-ttu-id="f99ae-284">Trennen Sie die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f99ae-284">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-285">1</span><span class="sxs-lookup"><span data-stu-id="f99ae-285">1</span></span>
</dt> <dd>

<span data-ttu-id="f99ae-286">Versuchen Sie, die Sitzung erneut zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="f99ae-286">Attempt to re-authorize the session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f99ae-287">**Smartcardzulässig**</span><span class="sxs-lookup"><span data-stu-id="f99ae-287">**SmartcardAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-288">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-290">Gibt an, ob eine Smartcard verwendet werden kann, um eine Verbindung mit dem RD-Gateway-Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f99ae-290">Indicates if a smart card can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="f99ae-291">Diese Eigenschaft kann mithilfe der Methode "\* [**zmartcardallowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f99ae-291">This property can be changed by using the [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f99ae-292">**Usergroupnames**</span><span class="sxs-lookup"><span data-stu-id="f99ae-292">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99ae-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f99ae-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f99ae-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f99ae-295">Liste von durch Semikolon getrennten Benutzergruppen Namen.</span><span class="sxs-lookup"><span data-stu-id="f99ae-295">List of semicolon-separated user group names.</span></span> <span data-ttu-id="f99ae-296">Die Namen weisen das Format *Domäne \\ usergroupname* auf.</span><span class="sxs-lookup"><span data-stu-id="f99ae-296">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="f99ae-297">Wenn der Benutzer zu einer dieser Benutzergruppen gehört, erhält der Benutzer Zugriff auf den RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="f99ae-297">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f99ae-298">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f99ae-298">Remarks</span></span>

<span data-ttu-id="f99ae-299">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="f99ae-299">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="f99ae-300">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f99ae-300">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f99ae-301">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f99ae-301">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f99ae-302">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f99ae-302">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f99ae-303">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f99ae-303">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f99ae-304">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f99ae-304">Requirements</span></span>



| <span data-ttu-id="f99ae-305">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f99ae-305">Requirement</span></span> | <span data-ttu-id="f99ae-306">Wert</span><span class="sxs-lookup"><span data-stu-id="f99ae-306">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f99ae-307">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f99ae-307">Minimum supported client</span></span><br/> | <span data-ttu-id="f99ae-308">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f99ae-308">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f99ae-309">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f99ae-309">Minimum supported server</span></span><br/> | <span data-ttu-id="f99ae-310">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f99ae-310">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f99ae-311">Namespace</span><span class="sxs-lookup"><span data-stu-id="f99ae-311">Namespace</span></span><br/>                | <span data-ttu-id="f99ae-312">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f99ae-312">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f99ae-313">MOF</span><span class="sxs-lookup"><span data-stu-id="f99ae-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f99ae-314"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="f99ae-314"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f99ae-315">DLL</span><span class="sxs-lookup"><span data-stu-id="f99ae-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f99ae-316"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f99ae-316"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f99ae-317">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f99ae-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99ae-318">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="f99ae-318">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="f99ae-319">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="f99ae-319">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="f99ae-320">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="f99ae-320">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="f99ae-321">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="f99ae-321">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="f99ae-322">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="f99ae-322">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="f99ae-323">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="f99ae-323">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

