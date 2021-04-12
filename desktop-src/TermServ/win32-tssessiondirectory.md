---
title: Win32_TSSessionDirectory-Klasse
description: Definiert die Konfigurationseinstellungen für den Remotedesktopverbindung Broker (RD-Verbindungsbroker) für die Win32- \_ Klasse "tssessiondirectorysetting".
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste
- Win32_TSSessionDirectory Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949730"
---
# <a name="win32_tssessiondirectory-class"></a><span data-ttu-id="3139a-105">Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="3139a-105">Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="3139a-106">Definiert die Konfigurationseinstellungen für den Remotedesktopverbindung Broker (RD-Verbindungsbroker) für die Win32-Klasse " [**\_ tssessiondirectorysetting**](win32-tssessiondirectorysetting.md) ".</span><span class="sxs-lookup"><span data-stu-id="3139a-106">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="3139a-107">In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) in "RD-Verbindungsbroker" geändert.</span><span class="sxs-lookup"><span data-stu-id="3139a-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="3139a-108">Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="3139a-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

<span data-ttu-id="3139a-109">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="3139a-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="3139a-110">Referenzinformationen zu Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="3139a-110">For reference information about methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="3139a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3139a-111">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a><span data-ttu-id="3139a-112">Member</span><span class="sxs-lookup"><span data-stu-id="3139a-112">Members</span></span>

<span data-ttu-id="3139a-113">Die Win32-Klasse " **\_ tssessiondirectory** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3139a-113">The **Win32\_TSSessionDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="3139a-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="3139a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="3139a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3139a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3139a-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="3139a-116">Methods</span></span>

<span data-ttu-id="3139a-117">Die Win32-Klasse " **\_ tssessiondirectory** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3139a-117">The **Win32\_TSSessionDirectory** class has these methods.</span></span>



| <span data-ttu-id="3139a-118">Methode</span><span class="sxs-lookup"><span data-stu-id="3139a-118">Method</span></span>                                                                                                  | <span data-ttu-id="3139a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3139a-119">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3139a-120">**"Buildeuserdisktemplate"**</span><span class="sxs-lookup"><span data-stu-id="3139a-120">**CreateUserDiskTemplate**</span></span>](createuserdisktemplate-win32-tssessiondirectory.md)                       | <span data-ttu-id="3139a-121">Erstellt eine Vorlage für Benutzer Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3139a-121">Creates a user disk template.</span></span><br/>                                                                     |
| [<span data-ttu-id="3139a-122">**Disableuservhd**</span><span class="sxs-lookup"><span data-stu-id="3139a-122">**DisableUserVhd**</span></span>](disableuservhd-win32-tssessiondirectory.md)                                       | <span data-ttu-id="3139a-123">Deaktiviert eine Benutzerprofil-VHD.</span><span class="sxs-lookup"><span data-stu-id="3139a-123">Disables a user profile VHD.</span></span><br/>                                                                      |
| [<span data-ttu-id="3139a-124">**Enableuservhd**</span><span class="sxs-lookup"><span data-stu-id="3139a-124">**EnableUserVhd**</span></span>](enableuservhd-win32-tssessiondirectory.md)                                         | <span data-ttu-id="3139a-125">Aktiviert eine Benutzerprofil-VHD auf einem RDSH-Server.</span><span class="sxs-lookup"><span data-stu-id="3139a-125">Enables a user profile VHD on an RDSH server.</span></span><br/>                                                     |
| [<span data-ttu-id="3139a-126">**Getcurrentredirectableadressen**</span><span class="sxs-lookup"><span data-stu-id="3139a-126">**GetCurrentRedirectableAddresses**</span></span>](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="3139a-127">Ruft die derzeit konfigurierte Liste der für den DNS berechtigten Adressen und den Umleitungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="3139a-127">Obtains the currently configured list of DNS eligible addresses, and the redirection type.</span></span><br/>        |
| [<span data-ttu-id="3139a-128">**Getredirectableadressen**</span><span class="sxs-lookup"><span data-stu-id="3139a-128">**GetRedirectableAddresses**</span></span>](getredirectableaddresses-win32-tssessiondirectory.md)                   | <span data-ttu-id="3139a-129">Ruft die gesamte Liste der für den DNS berechtigten Adressen ab.</span><span class="sxs-lookup"><span data-stu-id="3139a-129">Obtains the entire list of DNS eligible addresses.</span></span><br/>                                                |
| [<span data-ttu-id="3139a-130">**Pingsessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="3139a-130">**PingSessionDirectory**</span></span>](pingsessiondirectory-win32-tssessiondirectory.md)                           | <span data-ttu-id="3139a-131">Überprüft, ob der RD-Verbindungsbroker Server verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3139a-131">Checks whether the RD Connection Broker server is available.</span></span><br/>                                      |
| [<span data-ttu-id="3139a-132">**Setcurrentredirectableadressen**</span><span class="sxs-lookup"><span data-stu-id="3139a-132">**SetCurrentRedirectableAddresses**</span></span>](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="3139a-133">Legt die konfigurierte Liste der für den DNS berechtigten Adressen und den Umleitungstyp fest.</span><span class="sxs-lookup"><span data-stu-id="3139a-133">Sets the configured list of DNS eligible addresses, and the redirection type.</span></span><br/>                     |
| [<span data-ttu-id="3139a-134">**Setloadbalancingstate**</span><span class="sxs-lookup"><span data-stu-id="3139a-134">**SetLoadBalancingState**</span></span>](setloadbalancingstate-win32-tssessiondirectory.md)                         | <span data-ttu-id="3139a-135">Legt den Wert fest, mit dem angegeben wird, ob der Server an RD-Verbindungsbroker Lastenausgleich beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="3139a-135">Sets the value to indicate if the server will participate in RD Connection Broker load balancing.</span></span><br/> |
| [<span data-ttu-id="3139a-136">**Setserverweight**</span><span class="sxs-lookup"><span data-stu-id="3139a-136">**SetServerWeight**</span></span>](setserverweight-win32-tssessiondirectory.md)                                     | <span data-ttu-id="3139a-137">Legt den Server Gewichtungswert für RD-Verbindungsbroker Lastenausgleich fest.</span><span class="sxs-lookup"><span data-stu-id="3139a-137">Sets the server weight value for RD Connection Broker load balancing.</span></span><br/>                             |
| [<span data-ttu-id="3139a-138">**"-Essiondirector"**</span><span class="sxs-lookup"><span data-stu-id="3139a-138">**SetSessionDirectoryActive**</span></span>](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | <span data-ttu-id="3139a-139">Deaktiviert und aktiviert die RD-Verbindungsbroker.</span><span class="sxs-lookup"><span data-stu-id="3139a-139">Disables and enables the RD Connection Broker.</span></span><br/>                                                    |
| [<span data-ttu-id="3139a-140">**"Server-Sitzungs Verzeichnis-IP"**</span><span class="sxs-lookup"><span data-stu-id="3139a-140">**SetSessionDirectoryExposeServerIP**</span></span>](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | <span data-ttu-id="3139a-141">Legt die **sessiondirectoriyexposeserverip-** Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3139a-141">Sets the **SessionDirectoryExposeServerIP** property.</span></span><br/>                                             |
| [<span data-ttu-id="3139a-142">**"Gensessiondirectoriyproperty"**</span><span class="sxs-lookup"><span data-stu-id="3139a-142">**SetSessionDirectoryProperty**</span></span>](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | <span data-ttu-id="3139a-143">Legt die **sessiondirector yLocation** -Eigenschaft oder die **sessiondirectoriyclustername** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3139a-143">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property.</span></span><br/>   |
| [<span data-ttu-id="3139a-144">**Settsredirector Mode**</span><span class="sxs-lookup"><span data-stu-id="3139a-144">**SetTSRedirectorMode**</span></span>](settsredirectormode-win32-tssessiondirectory.md)                             | <span data-ttu-id="3139a-145">Diese Methode ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3139a-145">This method is not available.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="3139a-146">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3139a-146">Properties</span></span>

<span data-ttu-id="3139a-147">Die Win32-Klasse " **\_ tssessiondirectory** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3139a-147">The **Win32\_TSSessionDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3139a-148">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3139a-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3139a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3139a-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3139a-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3139a-152">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3139a-152">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="3139a-153">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3139a-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3139a-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3139a-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3139a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-157">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3139a-157">Description of the object.</span></span>

<span data-ttu-id="3139a-158">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3139a-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3139a-159">**Getloadbalancingstate**</span><span class="sxs-lookup"><span data-stu-id="3139a-159">**GetLoadBalancingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-162">Gibt an, ob der Server für die Teilnahme an RD-Verbindungsbroker Lastenausgleich konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3139a-162">Indicates if the server is configured to participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="3139a-163">0</span><span class="sxs-lookup"><span data-stu-id="3139a-163">0</span></span>
</dt> <dd>

<span data-ttu-id="3139a-164">Der Server ist nicht für die Teilnahme an RD-Verbindungsbroker Lastenausgleich konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3139a-164">The server is not configured to participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="3139a-165">1</span><span class="sxs-lookup"><span data-stu-id="3139a-165">1</span></span>
</dt> <dd>

<span data-ttu-id="3139a-166">Der Server ist so konfiguriert, dass er an RD-Verbindungsbroker Lastenausgleich beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="3139a-166">The server is configured to participate in RD Connection Broker load balancing.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-167">**Getserverweight**</span><span class="sxs-lookup"><span data-stu-id="3139a-167">**GetServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-170">Ruft den Wert für den Server Gewichtungswert ab, der in RD-Verbindungsbroker Lastenausgleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-170">Retrieves the server weight value that is used in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="3139a-171">**Gettsredirector Mode**</span><span class="sxs-lookup"><span data-stu-id="3139a-171">**GetTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-174">Gibt an, ob der Server so konfiguriert ist, dass er als Remotedesktopdienste Redirector fungiert.</span><span class="sxs-lookup"><span data-stu-id="3139a-174">Indicates if the server is configured to act as a Remote Desktop Services redirector.</span></span>

<dt>

<span data-ttu-id="3139a-175">0</span><span class="sxs-lookup"><span data-stu-id="3139a-175">0</span></span>
</dt> <dd>

<span data-ttu-id="3139a-176">Der Server ist so konfiguriert, dass er als Remotedesktopdienste Redirector fungiert.</span><span class="sxs-lookup"><span data-stu-id="3139a-176">The server is configured to act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="3139a-177">1</span><span class="sxs-lookup"><span data-stu-id="3139a-177">1</span></span>
</dt> <dd>

<span data-ttu-id="3139a-178">Der Server ist nicht so konfiguriert, dass er als Remotedesktopdienste Redirector fungiert.</span><span class="sxs-lookup"><span data-stu-id="3139a-178">The server is not configured to act as a Remote Desktop Services redirector.</span></span>

</dd> </dl>

<span data-ttu-id="3139a-179">**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3139a-179">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="3139a-180">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3139a-180">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-181">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3139a-181">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3139a-183">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="3139a-183">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="3139a-184">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3139a-184">The date the object was installed.</span></span> <span data-ttu-id="3139a-185">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3139a-185">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3139a-186">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3139a-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3139a-187">**Name**</span><span class="sxs-lookup"><span data-stu-id="3139a-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3139a-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-190">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3139a-190">The name of the object.</span></span>

<span data-ttu-id="3139a-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3139a-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3139a-192">**Policysourceloadbalancing**</span><span class="sxs-lookup"><span data-stu-id="3139a-192">**PolicySourceLoadBalancing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-193">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-195">Gibt an, ob die **getloadbalancingstate** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-195">Indicates if the **GetLoadBalancingState** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="3139a-196">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3139a-196">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-197">Server</span><span class="sxs-lookup"><span data-stu-id="3139a-197">Server</span></span>

</dd> <dt>

<span data-ttu-id="3139a-198">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3139a-198">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-199">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3139a-199">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-200">**Policysourcesessiondirectorialactive**</span><span class="sxs-lookup"><span data-stu-id="3139a-200">**PolicySourceSessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-203">Gibt an, ob die **sessiondirectoryactive** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-203">Indicates if the **SessionDirectoryActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="3139a-204">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3139a-204">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-205">Server</span><span class="sxs-lookup"><span data-stu-id="3139a-205">Server</span></span>

</dd> <dt>

<span data-ttu-id="3139a-206">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3139a-206">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-207">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3139a-207">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-208">**Policysourcesessiondirectoriyclustername**</span><span class="sxs-lookup"><span data-stu-id="3139a-208">**PolicySourceSessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-209">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-211">Gibt an, ob die **SessionDirectoryClusterName** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-211">Indicates if the **SessionDirectoryClusterName** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="3139a-212">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3139a-212">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-213">Server</span><span class="sxs-lookup"><span data-stu-id="3139a-213">Server</span></span>

</dd> <dt>

<span data-ttu-id="3139a-214">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3139a-214">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-215">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3139a-215">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-216">**Policysourcesessiondirectoriyexposeserverip**</span><span class="sxs-lookup"><span data-stu-id="3139a-216">**PolicySourceSessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-217">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-219">Gibt an, ob die **SessionDirectoryExposeServerIP-** Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-219">Indicates if the **SessionDirectoryExposeServerIP** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="3139a-220">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3139a-220">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-221">Server</span><span class="sxs-lookup"><span data-stu-id="3139a-221">Server</span></span>

</dd> <dt>

<span data-ttu-id="3139a-222">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3139a-222">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-223">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3139a-223">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-224">**Policysourcesessiondirectoriylocation**</span><span class="sxs-lookup"><span data-stu-id="3139a-224">**PolicySourceSessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-225">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-227">Gibt an, ob die **SessionDirectoryLocation** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-227">Indicates if the **SessionDirectoryLocation** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="3139a-228">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3139a-228">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-229">Server</span><span class="sxs-lookup"><span data-stu-id="3139a-229">Server</span></span>

</dd> <dt>

<span data-ttu-id="3139a-230">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3139a-230">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-231">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3139a-231">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-232">**Policysourcetsredirector Mode**</span><span class="sxs-lookup"><span data-stu-id="3139a-232">**PolicySourceTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-233">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-235">Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3139a-235">This property is not available.</span></span>

<span data-ttu-id="3139a-236">**Windows Server 2008 R2:** Gibt an, ob die **gettsredirectormode** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-236">**Windows Server 2008 R2:** Indicates if the **GetTSRedirectorMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="3139a-237">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3139a-237">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-238">Server</span><span class="sxs-lookup"><span data-stu-id="3139a-238">Server</span></span>

</dd> <dt>

<span data-ttu-id="3139a-239">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3139a-239">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3139a-240">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3139a-240">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-241">**Sessiondirectorialactive**</span><span class="sxs-lookup"><span data-stu-id="3139a-241">**SessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-242">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3139a-244">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3139a-244">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3139a-245">Gibt an, ob Remotedesktopdienste an der RD-Verbindungsbroker teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="3139a-245">Specifies if Remote Desktop Services participates in the RD Connection Broker.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3139a-246"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3139a-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3139a-247">Remotedesktopdienste Teilnahme am RD-Verbindungsbroker ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3139a-247">Remote Desktop Services participation in the RD Connection Broker is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3139a-248"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3139a-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3139a-249">Remotedesktopdienste Teilnahme am RD-Verbindungsbroker aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3139a-249">Remote Desktop Services participation in the RD Connection Broker is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-250">**Sessiondirectoriyclustername**</span><span class="sxs-lookup"><span data-stu-id="3139a-250">**SessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3139a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-253">Die virtuelle IP-Adresse des Clusters, zu dem der RD-Sitzungshost-Server gehört.</span><span class="sxs-lookup"><span data-stu-id="3139a-253">The virtual IP address of the cluster to which the RD Session Host server belongs.</span></span>

</dd> <dt>

<span data-ttu-id="3139a-254">**Sessiondirectoriyexposeserverip**</span><span class="sxs-lookup"><span data-stu-id="3139a-254">**SessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-255">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3139a-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-257">Gibt an, ob das Abrufen der IP-Adresse des RD-Verbindungsbroker zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3139a-257">Specifies if retrieval of the IP address of the RD Connection Broker is allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3139a-258"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3139a-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3139a-259">Der Abruf wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="3139a-259">Retrieval is denied.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3139a-260"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3139a-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3139a-261">Der Abruf ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="3139a-261">Retrieval is allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3139a-262">**Sessiondirector yipaddress**</span><span class="sxs-lookup"><span data-stu-id="3139a-262">**SessionDirectoryIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3139a-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-264">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3139a-264">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3139a-265">Die IP-Adresse des vom Sitzungs Verzeichnis verwendeten LAN-Adapters.</span><span class="sxs-lookup"><span data-stu-id="3139a-265">The IP address of the LAN adapter used by the session directory.</span></span>

</dd> <dt>

<span data-ttu-id="3139a-266">**Sessiondirectoriylocation**</span><span class="sxs-lookup"><span data-stu-id="3139a-266">**SessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3139a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3139a-269">Der Netzwerk-DNS-Name oder die IP-Adresse des Servers, auf dem der RD-Verbindungsbroker-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-269">The network DNS name or IP address of the server where the RD Connection Broker service is running.</span></span>

</dd> <dt>

<span data-ttu-id="3139a-270">**Status**</span><span class="sxs-lookup"><span data-stu-id="3139a-270">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3139a-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3139a-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3139a-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3139a-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3139a-273">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="3139a-273">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="3139a-274">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3139a-274">Current status of the object.</span></span> <span data-ttu-id="3139a-275">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3139a-275">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3139a-276">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="3139a-276">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3139a-277">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="3139a-277">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3139a-278">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3139a-278">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3139a-279">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="3139a-279">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3139a-280">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3139a-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="3139a-281">("OK")</span><span class="sxs-lookup"><span data-stu-id="3139a-281">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3139a-282">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="3139a-282">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3139a-283">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="3139a-283">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3139a-284">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3139a-284">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3139a-285">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3139a-285">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3139a-286">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="3139a-286">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3139a-287">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="3139a-287">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3139a-288">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="3139a-288">("Service")</span></span>


<span data-ttu-id="3139a-289"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3139a-289"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3139a-290">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3139a-290">Remarks</span></span>

<span data-ttu-id="3139a-291">Zum Herstellen einer Verbindung mit dem \\ \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="3139a-291">To connect to the \\\\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="3139a-292">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="3139a-292">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="3139a-293">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von sechs.</span><span class="sxs-lookup"><span data-stu-id="3139a-293">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="3139a-294">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3139a-294">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="3139a-295">In Windows Server 2008 wurde der Name des Terminaldienste-Sitzungs Verzeichnis Features in Terminaldienste-Sitzungs Broker geändert.</span><span class="sxs-lookup"><span data-stu-id="3139a-295">In Windows Server 2008, the name of the Terminal Services Session Directory feature was changed to Terminal Services Session Broker.</span></span>

<span data-ttu-id="3139a-296">In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Broker Features in Remotedesktopverbindung Broker geändert.</span><span class="sxs-lookup"><span data-stu-id="3139a-296">In Windows Server 2008 R2, the name of the Terminal Services Session Broker feature was changed to Remote Desktop Connection Broker.</span></span>

<span data-ttu-id="3139a-297">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3139a-297">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3139a-298">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="3139a-298">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3139a-299">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3139a-299">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3139a-300">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3139a-300">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3139a-301">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3139a-301">Requirements</span></span>



| <span data-ttu-id="3139a-302">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3139a-302">Requirement</span></span> | <span data-ttu-id="3139a-303">Wert</span><span class="sxs-lookup"><span data-stu-id="3139a-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3139a-304">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3139a-304">Minimum supported client</span></span><br/> | <span data-ttu-id="3139a-305">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3139a-305">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3139a-306">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3139a-306">Minimum supported server</span></span><br/> | <span data-ttu-id="3139a-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3139a-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3139a-308">Namespace</span><span class="sxs-lookup"><span data-stu-id="3139a-308">Namespace</span></span><br/>                | <span data-ttu-id="3139a-309">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3139a-309">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3139a-310">MOF</span><span class="sxs-lookup"><span data-stu-id="3139a-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3139a-311"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3139a-311"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3139a-312">DLL</span><span class="sxs-lookup"><span data-stu-id="3139a-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3139a-313"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3139a-313"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3139a-314">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3139a-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3139a-315">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="3139a-315">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="3139a-316">**Win32- \_ tssessiondirectorysetting**</span><span class="sxs-lookup"><span data-stu-id="3139a-316">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

