---
title: Win32_TSGatewayServerSettings-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren von Remotedesktop Gateway-Servereinstellungen (RD-Gateway) bereit.
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478813"
---
# <a name="win32_tsgatewayserversettings-class"></a><span data-ttu-id="609be-105">Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="609be-105">Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="609be-106">Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren von Remotedesktop Gateway-Servereinstellungen (RD-Gateway) bereit.</span><span class="sxs-lookup"><span data-stu-id="609be-106">Provides methods and properties to view and configure Remote Desktop Gateway (RD Gateway) server settings.</span></span> <span data-ttu-id="609be-107">Administratoren können diese Klasse verwenden, um einen Satz von Protokollen, den Satz von Ereignissen, die in das Ereignisprotokoll geschrieben werden, und die maximale Anzahl von Verbindungen durch RD-Gateway zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="609be-107">An administrator can use this class to configure a set of protocols, the set of events that will be written to the event log, and the maximum number of connections through RD Gateway.</span></span>

## <a name="syntax"></a><span data-ttu-id="609be-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="609be-108">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a><span data-ttu-id="609be-109">Member</span><span class="sxs-lookup"><span data-stu-id="609be-109">Members</span></span>

<span data-ttu-id="609be-110">Die Win32-Klasse "t- **\_ gatewayserversettings** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="609be-110">The **Win32\_TSGatewayServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="609be-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="609be-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="609be-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="609be-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="609be-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="609be-113">Methods</span></span>

<span data-ttu-id="609be-114">Die Win32-Klasse "t- **\_ gatewayserversettings** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="609be-114">The **Win32\_TSGatewayServerSettings** class has these methods.</span></span>



| <span data-ttu-id="609be-115">Methode</span><span class="sxs-lookup"><span data-stu-id="609be-115">Method</span></span>                                                                                                                                             | <span data-ttu-id="609be-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="609be-116">Description</span></span>                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="609be-117">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="609be-117">**Configure**</span></span>](configure-win32-tsgatewayserversettings.md)                                                                                       | <span data-ttu-id="609be-118">Konfiguriert die IIS-und RPC-Einstellungen, die für den RD-Gateway-Dienst erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="609be-118">Configures the IIS and RPC settings required by the RD Gateway service.</span></span><br/> <span data-ttu-id="609be-119">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-119">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                               |
| [<span data-ttu-id="609be-120">**Enablecentralcap**</span><span class="sxs-lookup"><span data-stu-id="609be-120">**EnableCentralCAP**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="609be-121">Aktiviert oder deaktiviert die **centralcapused** -Eigenschaft, mit der gesteuert wird, ob Zentrale Remotedesktop Verbindungs Autorisierungs Richtlinien-Server (RD-CAP) zum Steuern von Verbindungs Autorisierungs Richtlinien für diesen Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="609be-121">Enables or disables the **CentralCAPEnabled** property, which controls whether central Remote Desktop connection authorization policy (RD CAP) servers are used for controlling connection authorization policies for this server.</span></span><br/>                    |
| [<span data-ttu-id="609be-122">**Enablelogevent**</span><span class="sxs-lookup"><span data-stu-id="609be-122">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="609be-123">Aktiviert oder deaktiviert die Protokollierung des angegebenen Ereignis Typs.</span><span class="sxs-lookup"><span data-stu-id="609be-123">Enables or disables logging of the specified event type.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="609be-124">**Enableonlygenehmicapableclients**</span><span class="sxs-lookup"><span data-stu-id="609be-124">**EnableOnlyConsentCapableClients**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | <span data-ttu-id="609be-125">Legt die **onlygenehmicapableclients** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="609be-125">Sets the **OnlyConsentCapableClients** property.</span></span><br/> <span data-ttu-id="609be-126">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-126">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="609be-127">**Enablerequestsoh**</span><span class="sxs-lookup"><span data-stu-id="609be-127">**EnableRequestSOH**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | <span data-ttu-id="609be-128">Diese Methode wird ab Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="609be-128">This method is not supported starting with Windows Server 2016.</span></span><br/> <span data-ttu-id="609be-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008:** Aktiviert oder deaktiviert Anforderungen für ein Statement of Health (SoH).</span><span class="sxs-lookup"><span data-stu-id="609be-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:** Enables or disables requests for a Statement of Health (SoH).</span></span><br/> <br/> |
| [<span data-ttu-id="609be-130">**Enabletransport**</span><span class="sxs-lookup"><span data-stu-id="609be-130">**EnableTransport**</span></span>](enabletransport-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="609be-131">Aktiviert oder deaktiviert den angegebenen Transport.</span><span class="sxs-lookup"><span data-stu-id="609be-131">Enables or disables the specified transport.</span></span><br/> <span data-ttu-id="609be-132">**Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-132">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="609be-133">**Enumauthenticationplugins**</span><span class="sxs-lookup"><span data-stu-id="609be-133">**EnumAuthenticationPlugins**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | <span data-ttu-id="609be-134">Listet alle registrierten Authentifizierungs-Plug-Ins auf.</span><span class="sxs-lookup"><span data-stu-id="609be-134">Enumerates all registered authentication plug-ins.</span></span><br/> <span data-ttu-id="609be-135">**Windows Server 2008:** Diese Methode ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-135">**Windows Server 2008:** This method is not available.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="609be-136">**Enumauthorizationplugins**</span><span class="sxs-lookup"><span data-stu-id="609be-136">**EnumAuthorizationPlugins**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="609be-137">Listet alle registrierten Autorisierungs-Plug-Ins auf.</span><span class="sxs-lookup"><span data-stu-id="609be-137">Enumerates all registered authorization plug-ins.</span></span><br/> <span data-ttu-id="609be-138">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="609be-139">**Getipandport**</span><span class="sxs-lookup"><span data-stu-id="609be-139">**GetIPAndPort**</span></span>](getipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="609be-140">Ruft die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport ab.</span><span class="sxs-lookup"><span data-stu-id="609be-140">Obtains the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="609be-141">**Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-141">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                 |
| [<span data-ttu-id="609be-142">**Getlogeventname**</span><span class="sxs-lookup"><span data-stu-id="609be-142">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="609be-143">Gibt den Protokoll Ereignis Namen für den angegebenen Protokoll Ereignis Index zurück.</span><span class="sxs-lookup"><span data-stu-id="609be-143">Returns the log event name for the specified log event index.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="609be-144">**Getprotocolname**</span><span class="sxs-lookup"><span data-stu-id="609be-144">**GetProtocolName**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="609be-145">Gibt den Protokollnamen für den angegebenen Protokoll Index zurück.</span><span class="sxs-lookup"><span data-stu-id="609be-145">Returns the protocol name for the specified protocol index.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="609be-146">**Islogeventaktivierte**</span><span class="sxs-lookup"><span data-stu-id="609be-146">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="609be-147">Gibt an, ob der angegebene Ereignis protokolllistyp aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="609be-147">Indicates whether the specified event log type is enabled.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="609be-148">**Istransportenabled**</span><span class="sxs-lookup"><span data-stu-id="609be-148">**IsTransportEnabled**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="609be-149">Bestimmt, ob der angegebene Transport aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="609be-149">Determines whether the specified transport is enabled.</span></span><br/> <span data-ttu-id="609be-150">**Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-150">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                        |
| [<span data-ttu-id="609be-151">**Querycertcontext**</span><span class="sxs-lookup"><span data-stu-id="609be-151">**QueryCertContext**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | <span data-ttu-id="609be-152">Gibt an, ob das angegebene Zertifikat installiert ist.</span><span class="sxs-lookup"><span data-stu-id="609be-152">Indicates whether the specified certificate is installed.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="609be-153">**Recyclerpcapplicationpools**</span><span class="sxs-lookup"><span data-stu-id="609be-153">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | <span data-ttu-id="609be-154">Wiederverwendungen der RPC-Anwendungs Pools in IIS.</span><span class="sxs-lookup"><span data-stu-id="609be-154">Recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="609be-155">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-155">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="609be-156">**Aktualisierbaren Kontext**</span><span class="sxs-lookup"><span data-stu-id="609be-156">**RefreshCertContext**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | <span data-ttu-id="609be-157">Aktualisiert das Zertifikat, das vom RD-Gateway-Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="609be-157">Refreshes the certificate that is used by the RD Gateway server.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="609be-158">**Setauthenticationplugin**</span><span class="sxs-lookup"><span data-stu-id="609be-158">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | <span data-ttu-id="609be-159">Legt das aktuelle Authentifizierungs-Plug-in für den RD-Gateway Server fest.</span><span class="sxs-lookup"><span data-stu-id="609be-159">Sets the current authentication plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="609be-160">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-160">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="609be-161">**Setauthenticationpluginandrecyclerpcapplicationpools**</span><span class="sxs-lookup"><span data-stu-id="609be-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | <span data-ttu-id="609be-162">Legt das aktuelle Authentifizierungs-Plug-in für den RD-Gateway Server fest und wieder verwendet die RPC-Anwendungs Pools in IIS.</span><span class="sxs-lookup"><span data-stu-id="609be-162">Sets the current authentication plug-in for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="609be-163">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-163">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                      |
| [<span data-ttu-id="609be-164">**Setauthorizationplugin**</span><span class="sxs-lookup"><span data-stu-id="609be-164">**SetAuthorizationPlugin**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | <span data-ttu-id="609be-165">Legt das aktuelle Autorisierungs-Plug-in für den RD-Gateway Server fest.</span><span class="sxs-lookup"><span data-stu-id="609be-165">Sets the current authorization plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="609be-166">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-166">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                     |
| [<span data-ttu-id="609be-167">**SetCertificate**</span><span class="sxs-lookup"><span data-stu-id="609be-167">**SetCertificate**</span></span>](setcertificate-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="609be-168">Legt den Zertifikat Hash für die HTTPS-Bindung an Port 443 in IIS fest.</span><span class="sxs-lookup"><span data-stu-id="609be-168">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span><br/> <span data-ttu-id="609be-169">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                       |
| [<span data-ttu-id="609be-170">**Setcertificateacl**</span><span class="sxs-lookup"><span data-stu-id="609be-170">**SetCertificateACL**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="609be-171">Legt die Zertifikat-Zugriffs Steuerungs Listen (ACLs) für diesen Server fest.</span><span class="sxs-lookup"><span data-stu-id="609be-171">Sets the certificate access control lists (ACLs) for this server.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="609be-172">**Setdefaultpluginsandrecyclerpcapplicationpools**</span><span class="sxs-lookup"><span data-stu-id="609be-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | <span data-ttu-id="609be-173">Legt die aktuellen Authentifizierungs-und Autorisierungs-Plug-Ins für den RD-Gateway Server fest und wieder verwendet die RPC-Anwendungs Pools in IIS.</span><span class="sxs-lookup"><span data-stu-id="609be-173">Sets the current authentication and authorization plug-ins for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="609be-174">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-174">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                   |
| [<span data-ttu-id="609be-175">**"Tenforcechannelbinding"**</span><span class="sxs-lookup"><span data-stu-id="609be-175">**SetEnforceChannelBinding**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="609be-176">Legt die **enforcechannelbinding** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="609be-176">Sets the **EnforceChannelBinding** property.</span></span><br/> <span data-ttu-id="609be-177">**Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-177">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="609be-178">**"Seetipandport"**</span><span class="sxs-lookup"><span data-stu-id="609be-178">**SetIPAndPort**</span></span>](setipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="609be-179">Legt die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport fest.</span><span class="sxs-lookup"><span data-stu-id="609be-179">Sets the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="609be-180">**Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-180">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                    |
| [<span data-ttu-id="609be-181">**Setmaxconnections**</span><span class="sxs-lookup"><span data-stu-id="609be-181">**SetMaxConnections**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="609be-182">Legt die maximale Anzahl zulässiger Verbindungen über RD-Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="609be-182">Sets the maximum number of allowed connections through RD Gateway.</span></span> <span data-ttu-id="609be-183">Mit dieser Methode werden die Eigenschaften " **MaxConnections** " und " **UnlimitedConnections** " geändert.</span><span class="sxs-lookup"><span data-stu-id="609be-183">This method changes the **MaxConnections** and **UnlimitedConnections** properties.</span></span><br/>                                                                                                |
| [<span data-ttu-id="609be-184">**Setsslbridging**</span><span class="sxs-lookup"><span data-stu-id="609be-184">**SetSslBridging**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="609be-185">Legt den Typ des SSL-Bridging fest, der vom RD-Gateway Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="609be-185">Sets the type of SSL bridging to be used by the RD Gateway server.</span></span><br/> <span data-ttu-id="609be-186">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-186">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="609be-187">**"T"**</span><span class="sxs-lookup"><span data-stu-id="609be-187">**TSGRemoveAdminMsg**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="609be-188">Entfernt die administrative Meldung für den Gatewayserver.</span><span class="sxs-lookup"><span data-stu-id="609be-188">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="609be-189">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-189">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="609be-190">**"T"**</span><span class="sxs-lookup"><span data-stu-id="609be-190">**TSGRemoveConsentMsg**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | <span data-ttu-id="609be-191">Entfernt die administrative Meldung für den Gatewayserver.</span><span class="sxs-lookup"><span data-stu-id="609be-191">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="609be-192">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-192">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="609be-193">**"GS storeadminmsg"**</span><span class="sxs-lookup"><span data-stu-id="609be-193">**TSGStoreAdminMsg**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="609be-194">Aktualisiert die administrative Meldung für den Gatewayserver.</span><span class="sxs-lookup"><span data-stu-id="609be-194">Updates the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="609be-195">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-195">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="609be-196">**"GS-storeconsentmsg"**</span><span class="sxs-lookup"><span data-stu-id="609be-196">**TSGStoreConsentMsg**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="609be-197">Aktualisiert die Zustimmungs Nachricht für den Gatewayserver.</span><span class="sxs-lookup"><span data-stu-id="609be-197">Updates the consent message for the gateway server.</span></span><br/> <span data-ttu-id="609be-198">**Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-198">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="609be-199">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="609be-199">Properties</span></span>

<span data-ttu-id="609be-200">Die Win32-Klasse "t- **\_ gatewayserversettings** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="609be-200">The **Win32\_TSGatewayServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="609be-201">**adminmessageendtime**</span><span class="sxs-lookup"><span data-stu-id="609be-201">**adminMessageEndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-204">Die Endzeit der administrativen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="609be-204">The administrative message end time.</span></span>

<span data-ttu-id="609be-205">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-205">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-206">**adminmessagestarttime**</span><span class="sxs-lookup"><span data-stu-id="609be-206">**adminMessageStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-209">Die Startzeit der administrativen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="609be-209">The administrative message start time.</span></span>

<span data-ttu-id="609be-210">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-210">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-211">**adminmessagetext**</span><span class="sxs-lookup"><span data-stu-id="609be-211">**adminMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-214">Der Text der administrativen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="609be-214">The administrative message text.</span></span>

<span data-ttu-id="609be-215">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-215">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-216">**Authenticationpluginclsid**</span><span class="sxs-lookup"><span data-stu-id="609be-216">**AuthenticationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-219">Die CLSID des aktuellen Authentifizierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="609be-219">The CLSID of the current authentication plug-in.</span></span>

<span data-ttu-id="609be-220">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-220">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-221">**Authenticationplugindescription**</span><span class="sxs-lookup"><span data-stu-id="609be-221">**AuthenticationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-224">Die Beschreibung des aktuellen Authentifizierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="609be-224">The description of the current authentication plug-in.</span></span>

<span data-ttu-id="609be-225">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-225">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-226">**Authenticationpluginname**</span><span class="sxs-lookup"><span data-stu-id="609be-226">**AuthenticationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-229">Der Name des aktuellen Authentifizierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="609be-229">The name of the current authentication plug-in.</span></span>

<span data-ttu-id="609be-230">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-230">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-231">**Authorizationpluginclsid**</span><span class="sxs-lookup"><span data-stu-id="609be-231">**AuthorizationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-234">Die CLSID des aktuellen Autorisierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="609be-234">The CLSID of the current authorization plug-in.</span></span>

<span data-ttu-id="609be-235">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-235">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-236">**Authorizationplugindescription**</span><span class="sxs-lookup"><span data-stu-id="609be-236">**AuthorizationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-239">Die Beschreibung des aktuellen Autorisierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="609be-239">The description of the current authorization plug-in.</span></span>

<span data-ttu-id="609be-240">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-240">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-241">**Authorizationpluginname**</span><span class="sxs-lookup"><span data-stu-id="609be-241">**AuthorizationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-244">Der Name des aktuellen Autorisierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="609be-244">The name of the current authorization plug-in.</span></span>

<span data-ttu-id="609be-245">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-245">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-246">**Centralcapaktivierte**</span><span class="sxs-lookup"><span data-stu-id="609be-246">**CentralCAPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-247">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="609be-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="609be-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-249">Gibt an, ob zentrale RD-CAP-Server zum Steuern dieses Servers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="609be-249">Specifies whether central RD CAP servers are used for controlling this server.</span></span> <span data-ttu-id="609be-250">Diese Eigenschaft kann durch Aufrufen der [**enablecentralcap**](enablecentralcap-win32-tsgatewayserversettings.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="609be-250">This property can be changed by calling the [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="609be-251">**CertHash**</span><span class="sxs-lookup"><span data-stu-id="609be-251">**CertHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-252">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="609be-252">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="609be-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-254">Gibt den Zertifikat Hash für die HTTPS-Bindung an Port 443 in IIS an.</span><span class="sxs-lookup"><span data-stu-id="609be-254">Specifies the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

<span data-ttu-id="609be-255">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-255">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-256">**genehmimessagetext**</span><span class="sxs-lookup"><span data-stu-id="609be-256">**consentMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-259">Der Zustimmungs Meldungs Text.</span><span class="sxs-lookup"><span data-stu-id="609be-259">The consent message text.</span></span>

<span data-ttu-id="609be-260">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-260">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-261">**Enforcechannelbinding**</span><span class="sxs-lookup"><span data-stu-id="609be-261">**EnforceChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-262">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="609be-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="609be-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-264">Gibt an, ob die kanalbindung für den HTTP-Transport erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="609be-264">Indicates if channel binding is enforced for the HTTP transport.</span></span> <span data-ttu-id="609be-265">Dieser Eigenschafts Wert kann mithilfe der Methode " [**settenforcechannelbinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="609be-265">This property value can be changed by using the [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) method.</span></span>

<span data-ttu-id="609be-266">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-266">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available before Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="609be-267">**IsConfigured**</span><span class="sxs-lookup"><span data-stu-id="609be-267">**IsConfigured**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-268">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="609be-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="609be-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-270">Gibt an, ob die für den RD-Gateway Dienst erforderlichen IIS-und RPC-Einstellungen konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="609be-270">Specifies if IIS and RPC settings required by the RD Gateway service are configured.</span></span>

<span data-ttu-id="609be-271">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-271">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="609be-272">**MaxConnections**</span><span class="sxs-lookup"><span data-stu-id="609be-272">**MaxConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-273">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="609be-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="609be-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="609be-275">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="609be-275">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="609be-276">Gibt die maximale Anzahl von Verbindungen zurück, die durch RD-Gateway zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="609be-276">Returns the maximum number of connections that are allowed through RD Gateway.</span></span> <span data-ttu-id="609be-277">Diese Eigenschaft kann mit der [**setmaxconnections**](setmaxconnections-win32-tsgatewayserversettings.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="609be-277">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="609be-278">**Maximumallowedconnectionsbysku**</span><span class="sxs-lookup"><span data-stu-id="609be-278">**MaximumAllowedConnectionsBySku**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-279">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="609be-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="609be-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-281">Maximale Anzahl von Verbindungen, die die Stock Keeping Unit (SKU) zulässt.</span><span class="sxs-lookup"><span data-stu-id="609be-281">Maximum number of connections that the stock-keeping unit (SKU) allows.</span></span>

</dd> <dt>

<span data-ttu-id="609be-282">**Maxlogevents**</span><span class="sxs-lookup"><span data-stu-id="609be-282">**MaxLogEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="609be-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="609be-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-285">Gibt die maximale Anzahl von Protokoll Ereignissen zurück.</span><span class="sxs-lookup"><span data-stu-id="609be-285">Returns the maximum number of log events.</span></span>

</dd> <dt>

<span data-ttu-id="609be-286">**Maxprotokolle**</span><span class="sxs-lookup"><span data-stu-id="609be-286">**MaxProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-287">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="609be-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="609be-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-289">Anzahl von Protokollen, die von RD-Gateway unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="609be-289">Number of protocols supported by RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="609be-290">**Onlygenehmicapableclients**</span><span class="sxs-lookup"><span data-stu-id="609be-290">**OnlyConsentCapableClients**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-291">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="609be-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="609be-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-293">Gibt an, ob nur Clients, die Nachrichten unterstützen können, eine Verbindung mit dem RD-Gateway herstellen dürfen.</span><span class="sxs-lookup"><span data-stu-id="609be-293">Specifies if only clients capable of consent messages are allowed to connect to the RD Gateway.</span></span>

<span data-ttu-id="609be-294">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-294">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="609be-295">ungleich NULL</span><span class="sxs-lookup"><span data-stu-id="609be-295">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="609be-296">Nur Genehmigungs Nachrichten fähige Clients können eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="609be-296">Only consent message capable clients can connect.</span></span>

</dd> <dt>

<span data-ttu-id="609be-297">Null</span><span class="sxs-lookup"><span data-stu-id="609be-297">zero</span></span>
</dt> <dd>

<span data-ttu-id="609be-298">Clients, die keine Zustimmungs Nachrichten fähig sind, können auch eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="609be-298">Clients that are not consent message capable can also connect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="609be-299">**Requestsoh**</span><span class="sxs-lookup"><span data-stu-id="609be-299">**RequestSOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-300">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="609be-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="609be-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-302">Diese Eigenschaft wird ab Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="609be-302">This property is not supported starting with Windows Server 2016.</span></span>

<span data-ttu-id="609be-303">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="609be-303">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="609be-304">Gibt an, ob der Server ein Statement of Health (SoH) vom Client anfordern muss.</span><span class="sxs-lookup"><span data-stu-id="609be-304">Specifies whether the server must request a Statement of Health (SoH) from the client.</span></span> <span data-ttu-id="609be-305">Diese Eigenschaft kann mithilfe der [**enablerequestsoh**](win32-tsgatewayserversettings-enablerequestsoh.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="609be-305">This property can be changed by using the [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="609be-306">**SkuName**</span><span class="sxs-lookup"><span data-stu-id="609be-306">**SkuName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="609be-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="609be-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-309">Name der SKU</span><span class="sxs-lookup"><span data-stu-id="609be-309">Name of the SKU.</span></span>

</dd> <dt>

<span data-ttu-id="609be-310">**Sslbridging**</span><span class="sxs-lookup"><span data-stu-id="609be-310">**SslBridging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-311">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="609be-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="609be-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-313">Gibt an, welcher Typ von SSL-Bridging vom RD-Gateway Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="609be-313">Specifies which type of SSL bridging to be used by the RD Gateway server.</span></span> <span data-ttu-id="609be-314">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="609be-314">This can be one of the following values.</span></span>

<span data-ttu-id="609be-315">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="609be-315">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="609be-316">0</span><span class="sxs-lookup"><span data-stu-id="609be-316">0</span></span>
</dt> <dd>

<span data-ttu-id="609be-317">Keine SSL-Überbrückung.</span><span class="sxs-lookup"><span data-stu-id="609be-317">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="609be-318">1</span><span class="sxs-lookup"><span data-stu-id="609be-318">1</span></span>
</dt> <dd>

<span data-ttu-id="609be-319">HTTPS-zu-HTTP-Bridging.</span><span class="sxs-lookup"><span data-stu-id="609be-319">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="609be-320">2</span><span class="sxs-lookup"><span data-stu-id="609be-320">2</span></span>
</dt> <dd>

<span data-ttu-id="609be-321">HTTPS-zu-HTTPS-Bridging.</span><span class="sxs-lookup"><span data-stu-id="609be-321">HTTPS to HTTPS bridging.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="609be-322">**UnlimitedConnections**</span><span class="sxs-lookup"><span data-stu-id="609be-322">**UnlimitedConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="609be-323">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="609be-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="609be-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="609be-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="609be-325">Gibt an, ob eine unbegrenzte Anzahl von Verbindungen durch RD-Gateway zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="609be-325">Indicates whether an unlimited number of connections are allowed through RD Gateway.</span></span> <span data-ttu-id="609be-326">Diese Eigenschaft kann mit der [**setmaxconnections**](setmaxconnections-win32-tsgatewayserversettings.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="609be-326">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="609be-327">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="609be-327">Remarks</span></span>

<span data-ttu-id="609be-328">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="609be-328">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="609be-329">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="609be-329">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="609be-330">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="609be-330">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="609be-331">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="609be-331">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="609be-332">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="609be-332">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="609be-333">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="609be-333">Requirements</span></span>



| <span data-ttu-id="609be-334">Anforderung</span><span class="sxs-lookup"><span data-stu-id="609be-334">Requirement</span></span> | <span data-ttu-id="609be-335">Wert</span><span class="sxs-lookup"><span data-stu-id="609be-335">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="609be-336">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="609be-336">Minimum supported client</span></span><br/> | <span data-ttu-id="609be-337">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="609be-337">None supported</span></span><br/>                                                                |
| <span data-ttu-id="609be-338">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="609be-338">Minimum supported server</span></span><br/> | <span data-ttu-id="609be-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="609be-339">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="609be-340">Namespace</span><span class="sxs-lookup"><span data-stu-id="609be-340">Namespace</span></span><br/>                | <span data-ttu-id="609be-341">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="609be-341">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="609be-342">MOF</span><span class="sxs-lookup"><span data-stu-id="609be-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="609be-343"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="609be-343"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="609be-344">DLL</span><span class="sxs-lookup"><span data-stu-id="609be-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="609be-345"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="609be-345"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="609be-346">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="609be-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609be-347">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="609be-347">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="609be-348">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="609be-348">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="609be-349">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="609be-349">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="609be-350">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="609be-350">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="609be-351">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="609be-351">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="609be-352">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="609be-352">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

