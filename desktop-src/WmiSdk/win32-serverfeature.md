---
description: Die Win32 \_ Server Feature-Klasse stellt die Funktionen dar, die auf einem Computer mit Windows Server installiert sind.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Win32_ServerFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369834"
---
# <a name="win32_serverfeature-class"></a><span data-ttu-id="486be-103">Win32 \_ Server Feature-Klasse</span><span class="sxs-lookup"><span data-stu-id="486be-103">Win32\_ServerFeature class</span></span>

<span data-ttu-id="486be-104">\[Die **Win32 \_ Server Feature** -Klasse ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="486be-104">\[The **Win32\_ServerFeature** class is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="486be-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="486be-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="486be-106">Verwenden Sie stattdessen die [Anbieter Klassen von Server Manager deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span><span class="sxs-lookup"><span data-stu-id="486be-106">Instead, use the [ServerManager Deploymentprovider Provider Classes](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span></span>

<span data-ttu-id="486be-107">Die **Win32 \_ Server Feature** -Klasse stellt die Funktionen dar, die auf einem Computer mit Windows Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="486be-107">The **Win32\_ServerFeature** class represents the features installed on a computer running Windows Server.</span></span>

<span data-ttu-id="486be-108">Diese Klasse kann von Entwicklern und Administratoren verwendet werden, die den Prozess der Bestimmung der auf einer Gruppe von Server Computern installierten Features automatisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="486be-108">This class can be used by developers and administrators who need to automate the process of determining the features installed on a set of server computers.</span></span> <span data-ttu-id="486be-109">Instanzen dieser Klasse sind auf Client Computern nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="486be-109">Instances of this class are not available on client computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="486be-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="486be-110">Syntax</span></span>

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="486be-111">Member</span><span class="sxs-lookup"><span data-stu-id="486be-111">Members</span></span>

<span data-ttu-id="486be-112">Die **Win32 \_ Server Feature** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="486be-112">The **Win32\_ServerFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="486be-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="486be-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="486be-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="486be-114">Properties</span></span>

<span data-ttu-id="486be-115">Die **Win32 \_ Server Feature** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="486be-115">The **Win32\_ServerFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="486be-116">**ID**</span><span class="sxs-lookup"><span data-stu-id="486be-116">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="486be-117">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="486be-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="486be-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="486be-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="486be-119">Qualifizierer: [**Schlüssel**](key-qualifier.md), [**nicht \_ null**](optional-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="486be-119">Qualifiers: [**Key**](key-qualifier.md), [**Not\_Null**](optional-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="486be-120">ID der Server Funktion.</span><span class="sxs-lookup"><span data-stu-id="486be-120">Server feature ID.</span></span> <span data-ttu-id="486be-121">In der folgenden Liste werden die möglichen Werte der ID-Eigenschaft angezeigt:</span><span class="sxs-lookup"><span data-stu-id="486be-121">The following list shows the possible values of the ID property:</span></span>



<span data-ttu-id="486be-122">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-122">Value</span></span>

<span data-ttu-id="486be-123">Name</span><span class="sxs-lookup"><span data-stu-id="486be-123">Name</span></span>

<span data-ttu-id="486be-124">1</span><span class="sxs-lookup"><span data-stu-id="486be-124">1</span></span>

[<span data-ttu-id="486be-125">Anwendungsserver</span><span class="sxs-lookup"><span data-stu-id="486be-125">Application Server</span></span>](/windows)

<span data-ttu-id="486be-126">2</span><span class="sxs-lookup"><span data-stu-id="486be-126">2</span></span>

<span data-ttu-id="486be-127">Webserver (IIS)</span><span class="sxs-lookup"><span data-stu-id="486be-127">Web Server (IIS)</span></span>

<span data-ttu-id="486be-128">3</span><span class="sxs-lookup"><span data-stu-id="486be-128">3</span></span>

[<span data-ttu-id="486be-129">Streaming Media-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-129">Streaming Media Services</span></span>](/windows)

<span data-ttu-id="486be-130">5</span><span class="sxs-lookup"><span data-stu-id="486be-130">5</span></span>

<span data-ttu-id="486be-131">Faxserver</span><span class="sxs-lookup"><span data-stu-id="486be-131">Fax Server</span></span>

<span data-ttu-id="486be-132">6</span><span class="sxs-lookup"><span data-stu-id="486be-132">6</span></span>

<span data-ttu-id="486be-133">Datei- und iSCSI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-133">File and iSCSI Services</span></span><br/> [<span data-ttu-id="486be-134">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-134">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-135">7</span><span class="sxs-lookup"><span data-stu-id="486be-135">7</span></span>

<span data-ttu-id="486be-136">Druck- und Dokumentdienste</span><span class="sxs-lookup"><span data-stu-id="486be-136">Print and Document Services</span></span><br/> [<span data-ttu-id="486be-137">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-137">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-138">8</span><span class="sxs-lookup"><span data-stu-id="486be-138">8</span></span>

[<span data-ttu-id="486be-139">Active Directory-Verbunddienste (AD FS)</span><span class="sxs-lookup"><span data-stu-id="486be-139">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="486be-140">9</span><span class="sxs-lookup"><span data-stu-id="486be-140">9</span></span>

<span data-ttu-id="486be-141">Active Directory Lightweight Directory Services</span><span class="sxs-lookup"><span data-stu-id="486be-141">Active Directory Lightweight Directory Services</span></span>

<span data-ttu-id="486be-142">10</span><span class="sxs-lookup"><span data-stu-id="486be-142">10</span></span>

<span data-ttu-id="486be-143">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="486be-143">Active Directory Domain Services</span></span>

<span data-ttu-id="486be-144">11</span><span class="sxs-lookup"><span data-stu-id="486be-144">11</span></span>

[<span data-ttu-id="486be-145">UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-145">UDDI Services</span></span>](/windows)<br/>

<span data-ttu-id="486be-146">12</span><span class="sxs-lookup"><span data-stu-id="486be-146">12</span></span>

[<span data-ttu-id="486be-147">DHCP-Server</span><span class="sxs-lookup"><span data-stu-id="486be-147">DHCP Server</span></span>](/windows)

<span data-ttu-id="486be-148">13</span><span class="sxs-lookup"><span data-stu-id="486be-148">13</span></span>

[<span data-ttu-id="486be-149">DNS-Server</span><span class="sxs-lookup"><span data-stu-id="486be-149">DNS Server</span></span>](/windows)

<span data-ttu-id="486be-150">14</span><span class="sxs-lookup"><span data-stu-id="486be-150">14</span></span>

<span data-ttu-id="486be-151">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="486be-151">Network Policy and Access Services</span></span>

<span data-ttu-id="486be-152">16</span><span class="sxs-lookup"><span data-stu-id="486be-152">16</span></span>

<span data-ttu-id="486be-153">Active Directory-Zertifikatdienste</span><span class="sxs-lookup"><span data-stu-id="486be-153">Active Directory Certificate Services</span></span>

<span data-ttu-id="486be-154">17</span><span class="sxs-lookup"><span data-stu-id="486be-154">17</span></span>

<span data-ttu-id="486be-155">Active Directory-Rechteverwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="486be-155">Active Directory Rights Management Services</span></span>

<span data-ttu-id="486be-156">18</span><span class="sxs-lookup"><span data-stu-id="486be-156">18</span></span>

[<span data-ttu-id="486be-157">Remotedesktopdienste (RDS)</span><span class="sxs-lookup"><span data-stu-id="486be-157">Remote Desktop Services</span></span>](/windows)<br/> [<span data-ttu-id="486be-158">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-158">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-159">19</span><span class="sxs-lookup"><span data-stu-id="486be-159">19</span></span>

<span data-ttu-id="486be-160">Windows-Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="486be-160">Windows Deployment Services</span></span>

<span data-ttu-id="486be-161">20</span><span class="sxs-lookup"><span data-stu-id="486be-161">20</span></span>

<span data-ttu-id="486be-162">Hyper-V</span><span class="sxs-lookup"><span data-stu-id="486be-162">Hyper-V</span></span>

<span data-ttu-id="486be-163">21</span><span class="sxs-lookup"><span data-stu-id="486be-163">21</span></span>

[<span data-ttu-id="486be-164">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="486be-164">Windows Server Update Services</span></span>](/windows)

<span data-ttu-id="486be-165">33</span><span class="sxs-lookup"><span data-stu-id="486be-165">33</span></span>

[<span data-ttu-id="486be-166">Failoverclustering</span><span class="sxs-lookup"><span data-stu-id="486be-166">Failover Clustering</span></span>](/windows)

<span data-ttu-id="486be-167">34</span><span class="sxs-lookup"><span data-stu-id="486be-167">34</span></span>

[<span data-ttu-id="486be-168">Netzwerklastenausgleich</span><span class="sxs-lookup"><span data-stu-id="486be-168">Network Load Balancing</span></span>](/windows)

<span data-ttu-id="486be-169">36</span><span class="sxs-lookup"><span data-stu-id="486be-169">36</span></span>

[<span data-ttu-id="486be-170">.NET Framework 3.5.1-Features</span><span class="sxs-lookup"><span data-stu-id="486be-170">.NET Framework 3.5.1 Features</span></span>](/windows)<br/> [<span data-ttu-id="486be-171">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-171">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-172">37</span><span class="sxs-lookup"><span data-stu-id="486be-172">37</span></span>

[<span data-ttu-id="486be-173">Windows-Systemressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="486be-173">Windows System Resource Manager</span></span>](/windows)

<span data-ttu-id="486be-174">38</span><span class="sxs-lookup"><span data-stu-id="486be-174">38</span></span>

<span data-ttu-id="486be-175">WLAN-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-175">Wireless LAN Service</span></span>

<span data-ttu-id="486be-176">39</span><span class="sxs-lookup"><span data-stu-id="486be-176">39</span></span>

[<span data-ttu-id="486be-177">Windows Server-Sicherung Features</span><span class="sxs-lookup"><span data-stu-id="486be-177">Windows Server Backup Features</span></span>](/windows)

<span data-ttu-id="486be-178">40</span><span class="sxs-lookup"><span data-stu-id="486be-178">40</span></span>

<span data-ttu-id="486be-179">WINS-Server</span><span class="sxs-lookup"><span data-stu-id="486be-179">WINS Server</span></span>

<span data-ttu-id="486be-180">41</span><span class="sxs-lookup"><span data-stu-id="486be-180">41</span></span>

<span data-ttu-id="486be-181">Windows-Prozessaktivierungsdienst</span><span class="sxs-lookup"><span data-stu-id="486be-181">Windows Process Activation Service</span></span>

<span data-ttu-id="486be-182">42</span><span class="sxs-lookup"><span data-stu-id="486be-182">42</span></span>

[<span data-ttu-id="486be-183">Remoteunterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-183">Remote Assistance</span></span>](/windows)

<span data-ttu-id="486be-184">43</span><span class="sxs-lookup"><span data-stu-id="486be-184">43</span></span>

<span data-ttu-id="486be-185">Einfache TCP/IP-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-185">Simple TCP/IP Services</span></span>

<span data-ttu-id="486be-186">44</span><span class="sxs-lookup"><span data-stu-id="486be-186">44</span></span>

[<span data-ttu-id="486be-187">Telnet-Client</span><span class="sxs-lookup"><span data-stu-id="486be-187">Telnet Client</span></span>](/windows)

<span data-ttu-id="486be-188">45</span><span class="sxs-lookup"><span data-stu-id="486be-188">45</span></span>

[<span data-ttu-id="486be-189">Telnet-Server</span><span class="sxs-lookup"><span data-stu-id="486be-189">Telnet Server</span></span>](/windows)

<span data-ttu-id="486be-190">46</span><span class="sxs-lookup"><span data-stu-id="486be-190">46</span></span>

[<span data-ttu-id="486be-191">Subsystem für UNIX-basierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="486be-191">Subsystem For Unix-based Applications</span></span>](/windows)

<span data-ttu-id="486be-192">47</span><span class="sxs-lookup"><span data-stu-id="486be-192">47</span></span>

<span data-ttu-id="486be-193">RPC-über-HTTP-Proxy</span><span class="sxs-lookup"><span data-stu-id="486be-193">RPC Over HTTP Proxy</span></span>

<span data-ttu-id="486be-194">48</span><span class="sxs-lookup"><span data-stu-id="486be-194">48</span></span>

<span data-ttu-id="486be-195">SMTP-Server</span><span class="sxs-lookup"><span data-stu-id="486be-195">SMTP Server</span></span>

<span data-ttu-id="486be-196">49</span><span class="sxs-lookup"><span data-stu-id="486be-196">49</span></span>

<span data-ttu-id="486be-197">Message Queuing</span><span class="sxs-lookup"><span data-stu-id="486be-197">Message Queuing</span></span>

<span data-ttu-id="486be-198">51</span><span class="sxs-lookup"><span data-stu-id="486be-198">51</span></span>

[<span data-ttu-id="486be-199">Interne Windows-Datenbank</span><span class="sxs-lookup"><span data-stu-id="486be-199">Windows Internal Database</span></span>](/windows)

<span data-ttu-id="486be-200">52</span><span class="sxs-lookup"><span data-stu-id="486be-200">52</span></span>

[<span data-ttu-id="486be-201">Speicher-Manager für Sans</span><span class="sxs-lookup"><span data-stu-id="486be-201">Storage Manager For SANs</span></span>](/windows)

<span data-ttu-id="486be-202">53</span><span class="sxs-lookup"><span data-stu-id="486be-202">53</span></span>

<span data-ttu-id="486be-203">LPR-Portüberwachung</span><span class="sxs-lookup"><span data-stu-id="486be-203">LPR Port Monitor</span></span>

<span data-ttu-id="486be-204">55</span><span class="sxs-lookup"><span data-stu-id="486be-204">55</span></span>

[<span data-ttu-id="486be-205">Internet Storage Name Server</span><span class="sxs-lookup"><span data-stu-id="486be-205">Internet Storage Name Server</span></span>](/windows)

<span data-ttu-id="486be-206">57</span><span class="sxs-lookup"><span data-stu-id="486be-206">57</span></span>

[<span data-ttu-id="486be-207">Multipfad-e/a</span><span class="sxs-lookup"><span data-stu-id="486be-207">Multipath I/O</span></span>](/windows)

<span data-ttu-id="486be-208">58</span><span class="sxs-lookup"><span data-stu-id="486be-208">58</span></span>

<span data-ttu-id="486be-209">TFTP-Client</span><span class="sxs-lookup"><span data-stu-id="486be-209">TFTP Client</span></span>

<span data-ttu-id="486be-210">59</span><span class="sxs-lookup"><span data-stu-id="486be-210">59</span></span>

[<span data-ttu-id="486be-211">SNMP-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-211">SNMP Services</span></span>](/windows)

<span data-ttu-id="486be-212">60</span><span class="sxs-lookup"><span data-stu-id="486be-212">60</span></span>

[<span data-ttu-id="486be-213">Wechsel Speicher-Manager</span><span class="sxs-lookup"><span data-stu-id="486be-213">Removable Storage Manager</span></span>](/windows)

<span data-ttu-id="486be-214">61</span><span class="sxs-lookup"><span data-stu-id="486be-214">61</span></span>

<span data-ttu-id="486be-215">BitLocker-Laufwerkverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="486be-215">BitLocker Drive Encryption</span></span>

<span data-ttu-id="486be-216">62</span><span class="sxs-lookup"><span data-stu-id="486be-216">62</span></span>

[<span data-ttu-id="486be-217">Dienste für Netzwerkdatei System</span><span class="sxs-lookup"><span data-stu-id="486be-217">Services For Network File System</span></span>](/windows)

<span data-ttu-id="486be-218">63</span><span class="sxs-lookup"><span data-stu-id="486be-218">63</span></span>

<span data-ttu-id="486be-219">Internetdruckclient</span><span class="sxs-lookup"><span data-stu-id="486be-219">Internet Printing Client</span></span>

<span data-ttu-id="486be-220">64</span><span class="sxs-lookup"><span data-stu-id="486be-220">64</span></span>

[<span data-ttu-id="486be-221">Peer Name Resolution-Protokoll (PNRP)</span><span class="sxs-lookup"><span data-stu-id="486be-221">Peer Name Resolution Protocol</span></span>](/windows)

<span data-ttu-id="486be-222">65</span><span class="sxs-lookup"><span data-stu-id="486be-222">65</span></span>

<span data-ttu-id="486be-223">Verbindungs-Manager-Verwaltungskit</span><span class="sxs-lookup"><span data-stu-id="486be-223">Connection Manager Administration Kit</span></span>

<span data-ttu-id="486be-224">66</span><span class="sxs-lookup"><span data-stu-id="486be-224">66</span></span>

[<span data-ttu-id="486be-225">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-225">Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="486be-226">67</span><span class="sxs-lookup"><span data-stu-id="486be-226">67</span></span>

[<span data-ttu-id="486be-227">Remoteserver-Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="486be-227">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="486be-228">68</span><span class="sxs-lookup"><span data-stu-id="486be-228">68</span></span>

[<span data-ttu-id="486be-229">Verbessertes Windows-Audio-/Video-Streaming</span><span class="sxs-lookup"><span data-stu-id="486be-229">Quality Windows Audio Video Experience</span></span>](/windows)

<span data-ttu-id="486be-230">69</span><span class="sxs-lookup"><span data-stu-id="486be-230">69</span></span>

[<span data-ttu-id="486be-231">Gruppenrichtlinienverwaltung</span><span class="sxs-lookup"><span data-stu-id="486be-231">Group Policy Management</span></span>](/windows)

<span data-ttu-id="486be-232">71</span><span class="sxs-lookup"><span data-stu-id="486be-232">71</span></span>

[<span data-ttu-id="486be-233">Indexdienst</span><span class="sxs-lookup"><span data-stu-id="486be-233">Indexing Service</span></span>](/windows)

<span data-ttu-id="486be-234">72</span><span class="sxs-lookup"><span data-stu-id="486be-234">72</span></span>

[<span data-ttu-id="486be-235">Ressourcen-Manager für Dateiserver (File Server Resource Manager, FSRM)</span><span class="sxs-lookup"><span data-stu-id="486be-235">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="486be-236">73</span><span class="sxs-lookup"><span data-stu-id="486be-236">73</span></span>

<span data-ttu-id="486be-237">Remotedifferenzialkomprimierung</span><span class="sxs-lookup"><span data-stu-id="486be-237">Remote Differential Compression</span></span>

<span data-ttu-id="486be-238">310</span><span class="sxs-lookup"><span data-stu-id="486be-238">310</span></span>

<span data-ttu-id="486be-239">Freihand- und Handschriftdienste</span><span class="sxs-lookup"><span data-stu-id="486be-239">Ink and Handwriting Services</span></span><br/>

<span data-ttu-id="486be-240">320</span><span class="sxs-lookup"><span data-stu-id="486be-240">320</span></span>

[<span data-ttu-id="486be-241">Windows Server-Migrationstools</span><span class="sxs-lookup"><span data-stu-id="486be-241">Windows Server Migration Tools</span></span>](/windows)<br/>

<span data-ttu-id="486be-242">321</span><span class="sxs-lookup"><span data-stu-id="486be-242">321</span></span>

[<span data-ttu-id="486be-243">WinRM-IIS-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="486be-243">WinRM IIS Extension</span></span>](/windows)<br/>

<span data-ttu-id="486be-244">324</span><span class="sxs-lookup"><span data-stu-id="486be-244">324</span></span>

[<span data-ttu-id="486be-245">BranchCache</span><span class="sxs-lookup"><span data-stu-id="486be-245">BranchCache</span></span>](#branchcache)<br/>

<span data-ttu-id="486be-246">334</span><span class="sxs-lookup"><span data-stu-id="486be-246">334</span></span>

[<span data-ttu-id="486be-247">DirectAccess-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="486be-247">DirectAccess Management Console</span></span>](/windows)<br/>

<span data-ttu-id="486be-248">335</span><span class="sxs-lookup"><span data-stu-id="486be-248">335</span></span>

[<span data-ttu-id="486be-249">BITS (Background Intelligent Transfer Service, Intelligenter Hintergrundübertragungsdienst)</span><span class="sxs-lookup"><span data-stu-id="486be-249">Background Intelligent Transfer Service (BITS)</span></span>](/windows)<br/>

<span data-ttu-id="486be-250">338</span><span class="sxs-lookup"><span data-stu-id="486be-250">338</span></span>

[<span data-ttu-id="486be-251">XPS-Viewer</span><span class="sxs-lookup"><span data-stu-id="486be-251">XPS Viewer</span></span>](/windows)<br/>

<span data-ttu-id="486be-252">339</span><span class="sxs-lookup"><span data-stu-id="486be-252">339</span></span>

[<span data-ttu-id="486be-253">Windows-Biometrieframework</span><span class="sxs-lookup"><span data-stu-id="486be-253">Windows Biometric Framework</span></span>](/windows)<br/>

<span data-ttu-id="486be-254">340</span><span class="sxs-lookup"><span data-stu-id="486be-254">340</span></span>

<span data-ttu-id="486be-255">WoW64-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-255">WoW64 Support</span></span><br/>

<span data-ttu-id="486be-256">351</span><span class="sxs-lookup"><span data-stu-id="486be-256">351</span></span>

[<span data-ttu-id="486be-257">Windows PowerShell Integrated Scripting Environment (ISE)</span><span class="sxs-lookup"><span data-stu-id="486be-257">Windows PowerShell Integrated Scripting Environment (ISE)</span></span>](/windows)<br/>

<span data-ttu-id="486be-258">352</span><span class="sxs-lookup"><span data-stu-id="486be-258">352</span></span>

<span data-ttu-id="486be-259">Windows-TIFF-IFilter</span><span class="sxs-lookup"><span data-stu-id="486be-259">Windows TIFF IFilter</span></span><br/>

<span data-ttu-id="486be-260">404</span><span class="sxs-lookup"><span data-stu-id="486be-260">404</span></span>

[<span data-ttu-id="486be-261">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="486be-261">Window Server Update Services</span></span>](/windows)

<span data-ttu-id="486be-262">409</span><span class="sxs-lookup"><span data-stu-id="486be-262">409</span></span>

[<span data-ttu-id="486be-263">IP-Adressverwaltungsserver (IPAM-Server)</span><span class="sxs-lookup"><span data-stu-id="486be-263">IP Address Management (IPAM) Server</span></span>](/windows)

<span data-ttu-id="486be-264">417</span><span class="sxs-lookup"><span data-stu-id="486be-264">417</span></span>

[<span data-ttu-id="486be-265">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-265">Windows PowerShell</span></span>](/windows)

<span data-ttu-id="486be-266">418</span><span class="sxs-lookup"><span data-stu-id="486be-266">418</span></span>

[<span data-ttu-id="486be-267">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="486be-267">.NET Framework 4.5</span></span>](/windows)

<span data-ttu-id="486be-268">432</span><span class="sxs-lookup"><span data-stu-id="486be-268">432</span></span>

[<span data-ttu-id="486be-269">Windows Search-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-269">Windows Search Service</span></span>](/windows)

<span data-ttu-id="486be-270">438</span><span class="sxs-lookup"><span data-stu-id="486be-270">438</span></span>

[<span data-ttu-id="486be-271">Client für NFS</span><span class="sxs-lookup"><span data-stu-id="486be-271">Client for NFS</span></span>](/windows)

<span data-ttu-id="486be-272">441</span><span class="sxs-lookup"><span data-stu-id="486be-272">441</span></span>

[<span data-ttu-id="486be-273">BitLocker-Netzwerkentsperrung</span><span class="sxs-lookup"><span data-stu-id="486be-273">BitLocker Network Unlock</span></span>](/windows)

<span data-ttu-id="486be-274">442</span><span class="sxs-lookup"><span data-stu-id="486be-274">442</span></span>

[<span data-ttu-id="486be-275">IIS-Erweiterung für OData Services for Management</span><span class="sxs-lookup"><span data-stu-id="486be-275">Management OData IIS Extension</span></span>](/windows)

<span data-ttu-id="486be-276">450</span><span class="sxs-lookup"><span data-stu-id="486be-276">450</span></span>

[<span data-ttu-id="486be-277">.NET Framework 4.5 Advanced Services</span><span class="sxs-lookup"><span data-stu-id="486be-277">.NET Framework 4.5 Advanced Services</span></span>](/windows)

<span data-ttu-id="486be-278">466</span><span class="sxs-lookup"><span data-stu-id="486be-278">466</span></span>

[<span data-ttu-id="486be-279">.NET Framework 4.5-Features</span><span class="sxs-lookup"><span data-stu-id="486be-279">.NET Framework 4.5 Features</span></span>](/windows)

<span data-ttu-id="486be-280">468</span><span class="sxs-lookup"><span data-stu-id="486be-280">468</span></span>

[<span data-ttu-id="486be-281">Remotezugriff</span><span class="sxs-lookup"><span data-stu-id="486be-281">Remote Access</span></span>](/windows)<br/>

<span data-ttu-id="486be-282">477</span><span class="sxs-lookup"><span data-stu-id="486be-282">477</span></span>

[<span data-ttu-id="486be-283">Benutzeroberflächen und Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="486be-283">User Interfaces and Infrastructure</span></span>](/windows)

<span data-ttu-id="486be-284">478</span><span class="sxs-lookup"><span data-stu-id="486be-284">478</span></span>

[<span data-ttu-id="486be-285">Grafische Verwaltungstools und Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="486be-285">Graphical Management Tools and Infrastructure</span></span>](/windows)

<span data-ttu-id="486be-286">481</span><span class="sxs-lookup"><span data-stu-id="486be-286">481</span></span>

[<span data-ttu-id="486be-287">Datei- und Speicherdienste</span><span class="sxs-lookup"><span data-stu-id="486be-287">File and Storage Services</span></span>](/windows)

<span data-ttu-id="486be-288">485</span><span class="sxs-lookup"><span data-stu-id="486be-288">485</span></span>

[<span data-ttu-id="486be-289">Windows Server Essentials Experience</span><span class="sxs-lookup"><span data-stu-id="486be-289">Windows Server Essentials Experience</span></span>](/windows)

<span data-ttu-id="486be-290">488</span><span class="sxs-lookup"><span data-stu-id="486be-290">488</span></span>

[<span data-ttu-id="486be-291">DirectPlay</span><span class="sxs-lookup"><span data-stu-id="486be-291">Direct Play</span></span>](/windows)

<span data-ttu-id="486be-292">Dateidienste: Rollen Dienste (6)</span><span class="sxs-lookup"><span data-stu-id="486be-292">File Services - Role Services (6)</span></span>

<span data-ttu-id="486be-293">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-293">Value</span></span>

<span data-ttu-id="486be-294">Name</span><span class="sxs-lookup"><span data-stu-id="486be-294">Name</span></span>

<span data-ttu-id="486be-295">100</span><span class="sxs-lookup"><span data-stu-id="486be-295">100</span></span>

[<span data-ttu-id="486be-296">verteiltes Dateisystem</span><span class="sxs-lookup"><span data-stu-id="486be-296">Distributed File System</span></span>](/windows)

<span data-ttu-id="486be-297">101</span><span class="sxs-lookup"><span data-stu-id="486be-297">101</span></span>

<span data-ttu-id="486be-298">DFS-Namespace</span><span class="sxs-lookup"><span data-stu-id="486be-298">DFS Namespace</span></span>

<span data-ttu-id="486be-299">102</span><span class="sxs-lookup"><span data-stu-id="486be-299">102</span></span>

<span data-ttu-id="486be-300">DFS-Replikation</span><span class="sxs-lookup"><span data-stu-id="486be-300">DFS Replication</span></span>

<span data-ttu-id="486be-301">103</span><span class="sxs-lookup"><span data-stu-id="486be-301">103</span></span>

[<span data-ttu-id="486be-302">Dateireplikationsdienst</span><span class="sxs-lookup"><span data-stu-id="486be-302">File Replication Service</span></span>](/windows)

<span data-ttu-id="486be-303">104</span><span class="sxs-lookup"><span data-stu-id="486be-303">104</span></span>

[<span data-ttu-id="486be-304">Ressourcen-Manager für Dateiserver (File Server Resource Manager, FSRM)</span><span class="sxs-lookup"><span data-stu-id="486be-304">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="486be-305">105</span><span class="sxs-lookup"><span data-stu-id="486be-305">105</span></span>

[<span data-ttu-id="486be-306">Dienste für Netzwerkdatei System</span><span class="sxs-lookup"><span data-stu-id="486be-306">Services For Network File System</span></span>](/windows)

<span data-ttu-id="486be-307">106</span><span class="sxs-lookup"><span data-stu-id="486be-307">106</span></span>

[<span data-ttu-id="486be-308">Einzelinstanz-Speicherung</span><span class="sxs-lookup"><span data-stu-id="486be-308">Single Instance Storage</span></span>](/windows)

<span data-ttu-id="486be-309">107</span><span class="sxs-lookup"><span data-stu-id="486be-309">107</span></span>

[<span data-ttu-id="486be-310">Windows Search-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-310">Windows Search Service</span></span>](/windows)

<span data-ttu-id="486be-311">108</span><span class="sxs-lookup"><span data-stu-id="486be-311">108</span></span>

[<span data-ttu-id="486be-312">Indexdienst</span><span class="sxs-lookup"><span data-stu-id="486be-312">Indexing Service</span></span>](/windows)

<span data-ttu-id="486be-313">255</span><span class="sxs-lookup"><span data-stu-id="486be-313">255</span></span>

<span data-ttu-id="486be-314">Dateiserver</span><span class="sxs-lookup"><span data-stu-id="486be-314">File Server</span></span>

<span data-ttu-id="486be-315">350</span><span class="sxs-lookup"><span data-stu-id="486be-315">350</span></span>

<span data-ttu-id="486be-316">BranchCache für Netzwerkdateien</span><span class="sxs-lookup"><span data-stu-id="486be-316">BranchCache for Network Files</span></span>

<span data-ttu-id="486be-317">431</span><span class="sxs-lookup"><span data-stu-id="486be-317">431</span></span>

[<span data-ttu-id="486be-318">Server für NFS</span><span class="sxs-lookup"><span data-stu-id="486be-318">Server for NFS</span></span>](/windows)<br/>

<span data-ttu-id="486be-319">434</span><span class="sxs-lookup"><span data-stu-id="486be-319">434</span></span>

[<span data-ttu-id="486be-320">Dateiserver-VSS-Agent-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-320">File Server VSS Agent Service</span></span>](/windows)<br/>

<span data-ttu-id="486be-321">435</span><span class="sxs-lookup"><span data-stu-id="486be-321">435</span></span>

[<span data-ttu-id="486be-322">iSCSI-Zielserver</span><span class="sxs-lookup"><span data-stu-id="486be-322">iSCSI Target Server</span></span>](/windows)<br/>

<span data-ttu-id="486be-323">436</span><span class="sxs-lookup"><span data-stu-id="486be-323">436</span></span>

[<span data-ttu-id="486be-324">Datendeduplizierung</span><span class="sxs-lookup"><span data-stu-id="486be-324">Data Deduplication</span></span>](/windows)<br/>

<span data-ttu-id="486be-325">437</span><span class="sxs-lookup"><span data-stu-id="486be-325">437</span></span>

[<span data-ttu-id="486be-326">iSCSI-Zielspeicher Anbieter (VDS-und VSS-Hardware Anbieter)</span><span class="sxs-lookup"><span data-stu-id="486be-326">iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>](/windows)

<span data-ttu-id="486be-327">486</span><span class="sxs-lookup"><span data-stu-id="486be-327">486</span></span>

[<span data-ttu-id="486be-328">Arbeitsordner</span><span class="sxs-lookup"><span data-stu-id="486be-328">Work Folders</span></span>](/windows)

<span data-ttu-id="486be-329">Rollen Dienste für AD DS (10)</span><span class="sxs-lookup"><span data-stu-id="486be-329">AD DS - Role Services (10)</span></span>

<span data-ttu-id="486be-330">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-330">Value</span></span>

<span data-ttu-id="486be-331">Name</span><span class="sxs-lookup"><span data-stu-id="486be-331">Name</span></span>

<span data-ttu-id="486be-332">110</span><span class="sxs-lookup"><span data-stu-id="486be-332">110</span></span>

[<span data-ttu-id="486be-333">Active Directory-Domänencontroller</span><span class="sxs-lookup"><span data-stu-id="486be-333">Active Directory Domain Controller</span></span>](/windows)

<span data-ttu-id="486be-334">111</span><span class="sxs-lookup"><span data-stu-id="486be-334">111</span></span>

[<span data-ttu-id="486be-335">Identitätsverwaltung für UNIX</span><span class="sxs-lookup"><span data-stu-id="486be-335">Identity Management For Unix</span></span>](/windows)

<span data-ttu-id="486be-336">112</span><span class="sxs-lookup"><span data-stu-id="486be-336">112</span></span>

[<span data-ttu-id="486be-337">Server für Netzwerk Informationsdienste</span><span class="sxs-lookup"><span data-stu-id="486be-337">Server For Network Information Services</span></span>](/windows)

<span data-ttu-id="486be-338">113</span><span class="sxs-lookup"><span data-stu-id="486be-338">113</span></span>

[<span data-ttu-id="486be-339">Kennwortsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="486be-339">Password Synchronization</span></span>](/windows)

<span data-ttu-id="486be-340">294</span><span class="sxs-lookup"><span data-stu-id="486be-340">294</span></span>

[<span data-ttu-id="486be-341">Remoteserver-Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="486be-341">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="486be-342">Streaming Media-Rollen Dienste (3)</span><span class="sxs-lookup"><span data-stu-id="486be-342">Streaming Media - Role Services (3)</span></span>

<span data-ttu-id="486be-343">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-343">Value</span></span>

<span data-ttu-id="486be-344">Name</span><span class="sxs-lookup"><span data-stu-id="486be-344">Name</span></span>

<span data-ttu-id="486be-345">120</span><span class="sxs-lookup"><span data-stu-id="486be-345">120</span></span>

[<span data-ttu-id="486be-346">Windows Media-Server</span><span class="sxs-lookup"><span data-stu-id="486be-346">Windows Media Server</span></span>](/windows)

<span data-ttu-id="486be-347">121</span><span class="sxs-lookup"><span data-stu-id="486be-347">121</span></span>

[<span data-ttu-id="486be-348">Webbasierte Verwaltung</span><span class="sxs-lookup"><span data-stu-id="486be-348">Web-based Administration</span></span>](/windows)

<span data-ttu-id="486be-349">122</span><span class="sxs-lookup"><span data-stu-id="486be-349">122</span></span>

[<span data-ttu-id="486be-350">Protokollierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="486be-350">Logging Agent</span></span>](/windows)

<span data-ttu-id="486be-351">ADFS-Rollen Dienste (8)</span><span class="sxs-lookup"><span data-stu-id="486be-351">ADFS - Role Services (8)</span></span>

<span data-ttu-id="486be-352">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-352">Value</span></span>

<span data-ttu-id="486be-353">Name</span><span class="sxs-lookup"><span data-stu-id="486be-353">Name</span></span>

<span data-ttu-id="486be-354">125</span><span class="sxs-lookup"><span data-stu-id="486be-354">125</span></span>

[<span data-ttu-id="486be-355">Active Directory-Verbunddienste (AD FS)</span><span class="sxs-lookup"><span data-stu-id="486be-355">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="486be-356">126</span><span class="sxs-lookup"><span data-stu-id="486be-356">126</span></span>

[<span data-ttu-id="486be-357">Verbunddienst-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="486be-357">Federation Service Policy</span></span>](/windows)

<span data-ttu-id="486be-358">127</span><span class="sxs-lookup"><span data-stu-id="486be-358">127</span></span>

[<span data-ttu-id="486be-359">AD FS-Web-Agents</span><span class="sxs-lookup"><span data-stu-id="486be-359">AD FS Web Agents</span></span>](/windows)

<span data-ttu-id="486be-360">128</span><span class="sxs-lookup"><span data-stu-id="486be-360">128</span></span>

[<span data-ttu-id="486be-361">Ansprüche unterstützender Agent</span><span class="sxs-lookup"><span data-stu-id="486be-361">Claims-aware Agent</span></span>](/windows)

<span data-ttu-id="486be-362">129</span><span class="sxs-lookup"><span data-stu-id="486be-362">129</span></span>

[<span data-ttu-id="486be-363">Windows-Token-basierter Agent</span><span class="sxs-lookup"><span data-stu-id="486be-363">Windows Token-based Agent</span></span>](/windows)

<span data-ttu-id="486be-364">Remotedesktopdienste Rollen Dienste (18)</span><span class="sxs-lookup"><span data-stu-id="486be-364">Remote Desktop Services - Role Services (18)</span></span>

<span data-ttu-id="486be-365">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-365">Value</span></span>

<span data-ttu-id="486be-366">Name</span><span class="sxs-lookup"><span data-stu-id="486be-366">Name</span></span>

<span data-ttu-id="486be-367">130</span><span class="sxs-lookup"><span data-stu-id="486be-367">130</span></span>

<span data-ttu-id="486be-368">Remotedesktop-Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="486be-368">Remote Desktop Session Host</span></span><br/> [<span data-ttu-id="486be-369">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-369">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-370">131</span><span class="sxs-lookup"><span data-stu-id="486be-370">131</span></span>

[<span data-ttu-id="486be-371">Remotedesktoplizenzierung</span><span class="sxs-lookup"><span data-stu-id="486be-371">Remote Desktop Licensing</span></span>](/windows)<br/> [<span data-ttu-id="486be-372">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-372">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-373">132</span><span class="sxs-lookup"><span data-stu-id="486be-373">132</span></span>

<span data-ttu-id="486be-374">Remotedesktopgateway</span><span class="sxs-lookup"><span data-stu-id="486be-374">Remote Desktop Gateway</span></span><br/> [<span data-ttu-id="486be-375">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-375">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-376">133</span><span class="sxs-lookup"><span data-stu-id="486be-376">133</span></span>

<span data-ttu-id="486be-377">Remotedesktop-Verbindungsbroker</span><span class="sxs-lookup"><span data-stu-id="486be-377">Remote Desktop Connection Broker</span></span><br/> [<span data-ttu-id="486be-378">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-378">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-379">134</span><span class="sxs-lookup"><span data-stu-id="486be-379">134</span></span>

<span data-ttu-id="486be-380">Remotedesktop-Webzugriff</span><span class="sxs-lookup"><span data-stu-id="486be-380">Remote Desktop Web Access</span></span><br/> [<span data-ttu-id="486be-381">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-381">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-382">322</span><span class="sxs-lookup"><span data-stu-id="486be-382">322</span></span>

<span data-ttu-id="486be-383">Remotedesktop-Virtualisierungshost</span><span class="sxs-lookup"><span data-stu-id="486be-383">Remote Desktop Virtualization Host</span></span><br/>

<span data-ttu-id="486be-384">Remotedesktop-Virtualisierungshost Rollen Dienste (322)</span><span class="sxs-lookup"><span data-stu-id="486be-384">Remote Desktop Virtualization Host - Role Services (322)</span></span>

<span data-ttu-id="486be-385">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-385">Value</span></span>

<span data-ttu-id="486be-386">Name</span><span class="sxs-lookup"><span data-stu-id="486be-386">Name</span></span>

<span data-ttu-id="486be-387">325</span><span class="sxs-lookup"><span data-stu-id="486be-387">325</span></span>

[<span data-ttu-id="486be-388">Kerndienste</span><span class="sxs-lookup"><span data-stu-id="486be-388">Core Services</span></span>](/windows)<br/>

<span data-ttu-id="486be-389">327</span><span class="sxs-lookup"><span data-stu-id="486be-389">327</span></span>

[<span data-ttu-id="486be-390">Remotedesktop von virtuellen Grafiken</span><span class="sxs-lookup"><span data-stu-id="486be-390">Remote Desktop Virtual Graphics</span></span>](/windows)<br/>

<span data-ttu-id="486be-391">Druck-und Dokumentdienste Rollen Dienste (7)</span><span class="sxs-lookup"><span data-stu-id="486be-391">Print and Document Services - Role Services (7)</span></span>

<span data-ttu-id="486be-392">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-392">Value</span></span>

<span data-ttu-id="486be-393">Name</span><span class="sxs-lookup"><span data-stu-id="486be-393">Name</span></span>

<span data-ttu-id="486be-394">135</span><span class="sxs-lookup"><span data-stu-id="486be-394">135</span></span>

<span data-ttu-id="486be-395">Druckerserver</span><span class="sxs-lookup"><span data-stu-id="486be-395">Print Server</span></span>

<span data-ttu-id="486be-396">136</span><span class="sxs-lookup"><span data-stu-id="486be-396">136</span></span>

<span data-ttu-id="486be-397">Internetdrucken</span><span class="sxs-lookup"><span data-stu-id="486be-397">Internet Printing</span></span>

<span data-ttu-id="486be-398">137</span><span class="sxs-lookup"><span data-stu-id="486be-398">137</span></span>

<span data-ttu-id="486be-399">LPD-Druckdienst</span><span class="sxs-lookup"><span data-stu-id="486be-399">LPD Print Service</span></span>

<span data-ttu-id="486be-400">328</span><span class="sxs-lookup"><span data-stu-id="486be-400">328</span></span>

[<span data-ttu-id="486be-401">Server für verteilte Scanvorgänge</span><span class="sxs-lookup"><span data-stu-id="486be-401">Distributed Scan Server</span></span>](/windows)<br/>

<span data-ttu-id="486be-402">Webserver (IIS)-Rollen Dienste (2)</span><span class="sxs-lookup"><span data-stu-id="486be-402">Web Server (IIS) - Role Services (2)</span></span>

<span data-ttu-id="486be-403">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-403">Value</span></span>

<span data-ttu-id="486be-404">Name</span><span class="sxs-lookup"><span data-stu-id="486be-404">Name</span></span>

<span data-ttu-id="486be-405">140</span><span class="sxs-lookup"><span data-stu-id="486be-405">140</span></span>

<span data-ttu-id="486be-406">Webserver</span><span class="sxs-lookup"><span data-stu-id="486be-406">Web Server</span></span>

<span data-ttu-id="486be-407">141</span><span class="sxs-lookup"><span data-stu-id="486be-407">141</span></span>

<span data-ttu-id="486be-408">Allgemeine HTTP-Funktionen</span><span class="sxs-lookup"><span data-stu-id="486be-408">Common HTTP Features</span></span>

<span data-ttu-id="486be-409">142</span><span class="sxs-lookup"><span data-stu-id="486be-409">142</span></span>

<span data-ttu-id="486be-410">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="486be-410">Static Content</span></span>

<span data-ttu-id="486be-411">143</span><span class="sxs-lookup"><span data-stu-id="486be-411">143</span></span>

<span data-ttu-id="486be-412">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="486be-412">Default Document</span></span>

<span data-ttu-id="486be-413">144</span><span class="sxs-lookup"><span data-stu-id="486be-413">144</span></span>

<span data-ttu-id="486be-414">Verzeichnis durchsuchen</span><span class="sxs-lookup"><span data-stu-id="486be-414">Directory Browse</span></span>

<span data-ttu-id="486be-415">145</span><span class="sxs-lookup"><span data-stu-id="486be-415">145</span></span>

<span data-ttu-id="486be-416">HTTP-Fehler</span><span class="sxs-lookup"><span data-stu-id="486be-416">HTTP Errors</span></span>

<span data-ttu-id="486be-417">146</span><span class="sxs-lookup"><span data-stu-id="486be-417">146</span></span>

<span data-ttu-id="486be-418">HTTP-Umleitung</span><span class="sxs-lookup"><span data-stu-id="486be-418">HTTP Redirection</span></span>

<span data-ttu-id="486be-419">147</span><span class="sxs-lookup"><span data-stu-id="486be-419">147</span></span>

<span data-ttu-id="486be-420">Anwendungsentwicklung</span><span class="sxs-lookup"><span data-stu-id="486be-420">Application Development</span></span>

<span data-ttu-id="486be-421">148</span><span class="sxs-lookup"><span data-stu-id="486be-421">148</span></span>

<span data-ttu-id="486be-422">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="486be-422">ASP.NET</span></span>

<span data-ttu-id="486be-423">149</span><span class="sxs-lookup"><span data-stu-id="486be-423">149</span></span>

<span data-ttu-id="486be-424">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="486be-424">.NET Extensibility</span></span>

<span data-ttu-id="486be-425">150</span><span class="sxs-lookup"><span data-stu-id="486be-425">150</span></span>

<span data-ttu-id="486be-426">ASP</span><span class="sxs-lookup"><span data-stu-id="486be-426">ASP</span></span>

<span data-ttu-id="486be-427">151</span><span class="sxs-lookup"><span data-stu-id="486be-427">151</span></span>

<span data-ttu-id="486be-428">CGI</span><span class="sxs-lookup"><span data-stu-id="486be-428">CGI</span></span>

<span data-ttu-id="486be-429">152</span><span class="sxs-lookup"><span data-stu-id="486be-429">152</span></span>

<span data-ttu-id="486be-430">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="486be-430">ISAPI Extensions</span></span>

<span data-ttu-id="486be-431">153</span><span class="sxs-lookup"><span data-stu-id="486be-431">153</span></span>

<span data-ttu-id="486be-432">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="486be-432">ISAPI Filters</span></span>

<span data-ttu-id="486be-433">154</span><span class="sxs-lookup"><span data-stu-id="486be-433">154</span></span>

<span data-ttu-id="486be-434">Serverseitige Includes (SSI)</span><span class="sxs-lookup"><span data-stu-id="486be-434">Server Side Includes</span></span>

<span data-ttu-id="486be-435">155</span><span class="sxs-lookup"><span data-stu-id="486be-435">155</span></span>

<span data-ttu-id="486be-436">Integrität und Diagnose</span><span class="sxs-lookup"><span data-stu-id="486be-436">Health And Diagnostics</span></span>

<span data-ttu-id="486be-437">156</span><span class="sxs-lookup"><span data-stu-id="486be-437">156</span></span>

<span data-ttu-id="486be-438">HTTP-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="486be-438">HTTP Logging</span></span>

<span data-ttu-id="486be-439">157</span><span class="sxs-lookup"><span data-stu-id="486be-439">157</span></span>

<span data-ttu-id="486be-440">Protokollierungstools</span><span class="sxs-lookup"><span data-stu-id="486be-440">Logging Tools</span></span>

<span data-ttu-id="486be-441">158</span><span class="sxs-lookup"><span data-stu-id="486be-441">158</span></span>

<span data-ttu-id="486be-442">Anforderungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="486be-442">Request Monitor</span></span>

<span data-ttu-id="486be-443">159</span><span class="sxs-lookup"><span data-stu-id="486be-443">159</span></span>

<span data-ttu-id="486be-444">Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="486be-444">Tracing</span></span>

<span data-ttu-id="486be-445">160</span><span class="sxs-lookup"><span data-stu-id="486be-445">160</span></span>

<span data-ttu-id="486be-446">Benutzerdefinierte Protokollierung</span><span class="sxs-lookup"><span data-stu-id="486be-446">Custom Logging</span></span>

<span data-ttu-id="486be-447">161</span><span class="sxs-lookup"><span data-stu-id="486be-447">161</span></span>

<span data-ttu-id="486be-448">ODBC-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="486be-448">ODBC Logging</span></span>

<span data-ttu-id="486be-449">162</span><span class="sxs-lookup"><span data-stu-id="486be-449">162</span></span>

<span data-ttu-id="486be-450">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="486be-450">Security</span></span>

<span data-ttu-id="486be-451">163</span><span class="sxs-lookup"><span data-stu-id="486be-451">163</span></span>

<span data-ttu-id="486be-452">Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="486be-452">Basic Authentication</span></span>

<span data-ttu-id="486be-453">164</span><span class="sxs-lookup"><span data-stu-id="486be-453">164</span></span>

<span data-ttu-id="486be-454">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="486be-454">Windows Authentication</span></span>

<span data-ttu-id="486be-455">165</span><span class="sxs-lookup"><span data-stu-id="486be-455">165</span></span>

<span data-ttu-id="486be-456">Digestauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="486be-456">Digest Authentication</span></span>

<span data-ttu-id="486be-457">166</span><span class="sxs-lookup"><span data-stu-id="486be-457">166</span></span>

<span data-ttu-id="486be-458">Authentifizierung durch Clientzertifikatszuordnung</span><span class="sxs-lookup"><span data-stu-id="486be-458">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="486be-459">167</span><span class="sxs-lookup"><span data-stu-id="486be-459">167</span></span>

<span data-ttu-id="486be-460">Authentifizierung durch IIS-Clientzertifikatszuordnung</span><span class="sxs-lookup"><span data-stu-id="486be-460">IIS Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="486be-461">168</span><span class="sxs-lookup"><span data-stu-id="486be-461">168</span></span>

<span data-ttu-id="486be-462">URL-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="486be-462">URL Authorization</span></span>

<span data-ttu-id="486be-463">169</span><span class="sxs-lookup"><span data-stu-id="486be-463">169</span></span>

<span data-ttu-id="486be-464">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="486be-464">Request Filtering</span></span>

<span data-ttu-id="486be-465">170</span><span class="sxs-lookup"><span data-stu-id="486be-465">170</span></span>

<span data-ttu-id="486be-466">IP-und Domänen Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="486be-466">IP And Domain Restrictions</span></span>

<span data-ttu-id="486be-467">171</span><span class="sxs-lookup"><span data-stu-id="486be-467">171</span></span>

<span data-ttu-id="486be-468">Leistung</span><span class="sxs-lookup"><span data-stu-id="486be-468">Performance</span></span>

<span data-ttu-id="486be-469">172</span><span class="sxs-lookup"><span data-stu-id="486be-469">172</span></span>

<span data-ttu-id="486be-470">Komprimierung statischer Inhalte</span><span class="sxs-lookup"><span data-stu-id="486be-470">Static Content Compression</span></span>

<span data-ttu-id="486be-471">173</span><span class="sxs-lookup"><span data-stu-id="486be-471">173</span></span>

<span data-ttu-id="486be-472">Komprimierung dynamischer Inhalte</span><span class="sxs-lookup"><span data-stu-id="486be-472">Dynamic Content Compression</span></span>

<span data-ttu-id="486be-473">174</span><span class="sxs-lookup"><span data-stu-id="486be-473">174</span></span>

<span data-ttu-id="486be-474">Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="486be-474">Management Tools</span></span>

<span data-ttu-id="486be-475">175</span><span class="sxs-lookup"><span data-stu-id="486be-475">175</span></span>

<span data-ttu-id="486be-476">IIS-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="486be-476">IIS Management Console</span></span>

<span data-ttu-id="486be-477">176</span><span class="sxs-lookup"><span data-stu-id="486be-477">176</span></span>

<span data-ttu-id="486be-478">IIS-Verwaltungs Skripts und-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-478">IIS Management Scripts And Tools</span></span>

<span data-ttu-id="486be-479">177</span><span class="sxs-lookup"><span data-stu-id="486be-479">177</span></span>

<span data-ttu-id="486be-480">Verwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="486be-480">Management Service</span></span>

<span data-ttu-id="486be-481">178</span><span class="sxs-lookup"><span data-stu-id="486be-481">178</span></span>

<span data-ttu-id="486be-482">IIS 6-Verwaltungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="486be-482">IIS 6 Management Compatibility</span></span>

<span data-ttu-id="486be-483">179</span><span class="sxs-lookup"><span data-stu-id="486be-483">179</span></span>

<span data-ttu-id="486be-484">IIS 6-Metabasiskompatibilität</span><span class="sxs-lookup"><span data-stu-id="486be-484">IIS 6 Metabase Compatibility</span></span>

<span data-ttu-id="486be-485">180</span><span class="sxs-lookup"><span data-stu-id="486be-485">180</span></span>

<span data-ttu-id="486be-486">IIS 6-WMI-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="486be-486">IIS 6 WMI Compatibility</span></span>

<span data-ttu-id="486be-487">181</span><span class="sxs-lookup"><span data-stu-id="486be-487">181</span></span>

<span data-ttu-id="486be-488">IIS 6-Skripttools</span><span class="sxs-lookup"><span data-stu-id="486be-488">IIS 6 Scripting Tools</span></span>

<span data-ttu-id="486be-489">182</span><span class="sxs-lookup"><span data-stu-id="486be-489">182</span></span>

<span data-ttu-id="486be-490">IIS 6-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="486be-490">IIS 6 Management Console</span></span>

<span data-ttu-id="486be-491">183</span><span class="sxs-lookup"><span data-stu-id="486be-491">183</span></span>

<span data-ttu-id="486be-492">FTP-Publishingdienst</span><span class="sxs-lookup"><span data-stu-id="486be-492">FTP Publishing Service</span></span><br/>

<span data-ttu-id="486be-493">184</span><span class="sxs-lookup"><span data-stu-id="486be-493">184</span></span>

<span data-ttu-id="486be-494">FTP-Server</span><span class="sxs-lookup"><span data-stu-id="486be-494">FTP Server</span></span>

<span data-ttu-id="486be-495">185</span><span class="sxs-lookup"><span data-stu-id="486be-495">185</span></span>

<span data-ttu-id="486be-496">FTP-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="486be-496">FTP Management Console</span></span><br/>

<span data-ttu-id="486be-497">314</span><span class="sxs-lookup"><span data-stu-id="486be-497">314</span></span>

<span data-ttu-id="486be-498">WebDAV-Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="486be-498">WebDAV Publishing</span></span>

<span data-ttu-id="486be-499">316</span><span class="sxs-lookup"><span data-stu-id="486be-499">316</span></span>

<span data-ttu-id="486be-500">FTP-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-500">FTP Service</span></span><br/>

<span data-ttu-id="486be-501">317</span><span class="sxs-lookup"><span data-stu-id="486be-501">317</span></span>

<span data-ttu-id="486be-502">FTP-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="486be-502">FTP Extensibility</span></span><br/>

<span data-ttu-id="486be-503">336</span><span class="sxs-lookup"><span data-stu-id="486be-503">336</span></span>

<span data-ttu-id="486be-504">Hostfähiger IIS-Webkern</span><span class="sxs-lookup"><span data-stu-id="486be-504">IIS Hostable Web Core</span></span><br/>

<span data-ttu-id="486be-505">413</span><span class="sxs-lookup"><span data-stu-id="486be-505">413</span></span>

[<span data-ttu-id="486be-506">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="486be-506">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="486be-507">414</span><span class="sxs-lookup"><span data-stu-id="486be-507">414</span></span>

[<span data-ttu-id="486be-508">.NET-Erweiterbarkeit 4.5</span><span class="sxs-lookup"><span data-stu-id="486be-508">.NET Extensibility 4.5</span></span>](/windows)

<span data-ttu-id="486be-509">445</span><span class="sxs-lookup"><span data-stu-id="486be-509">445</span></span>

[<span data-ttu-id="486be-510">appialisierung</span><span class="sxs-lookup"><span data-stu-id="486be-510">appialization</span></span>](/windows)

<span data-ttu-id="486be-511">446</span><span class="sxs-lookup"><span data-stu-id="486be-511">446</span></span>

[<span data-ttu-id="486be-512">Zentralisierte Unterstützung von SSL-Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="486be-512">Centralized SSL Certificate Support</span></span>](/windows)

<span data-ttu-id="486be-513">447</span><span class="sxs-lookup"><span data-stu-id="486be-513">447</span></span>

[<span data-ttu-id="486be-514">WebSocket-Protokoll</span><span class="sxs-lookup"><span data-stu-id="486be-514">WebSocket Protocol</span></span>](/windows)

<span data-ttu-id="486be-515">Message Queuing-Features (49)</span><span class="sxs-lookup"><span data-stu-id="486be-515">Message Queuing - Features (49)</span></span>

<span data-ttu-id="486be-516">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-516">Value</span></span>

<span data-ttu-id="486be-517">Name</span><span class="sxs-lookup"><span data-stu-id="486be-517">Name</span></span>

<span data-ttu-id="486be-518">190</span><span class="sxs-lookup"><span data-stu-id="486be-518">190</span></span>

<span data-ttu-id="486be-519">Message Queuing Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-519">Message Queuing Services</span></span>

<span data-ttu-id="486be-520">191</span><span class="sxs-lookup"><span data-stu-id="486be-520">191</span></span>

<span data-ttu-id="486be-521">Message Queuing Server</span><span class="sxs-lookup"><span data-stu-id="486be-521">Message Queuing Server</span></span>

<span data-ttu-id="486be-522">192</span><span class="sxs-lookup"><span data-stu-id="486be-522">192</span></span>

<span data-ttu-id="486be-523">Verzeichnisdienstintegration</span><span class="sxs-lookup"><span data-stu-id="486be-523">Directory Service Integration</span></span>

<span data-ttu-id="486be-524">193</span><span class="sxs-lookup"><span data-stu-id="486be-524">193</span></span>

<span data-ttu-id="486be-525">Message Queuing Trigger</span><span class="sxs-lookup"><span data-stu-id="486be-525">Message Queuing Triggers</span></span>

<span data-ttu-id="486be-526">194</span><span class="sxs-lookup"><span data-stu-id="486be-526">194</span></span>

<span data-ttu-id="486be-527">HTTP-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-527">HTTP Support</span></span>

<span data-ttu-id="486be-528">195</span><span class="sxs-lookup"><span data-stu-id="486be-528">195</span></span>

<span data-ttu-id="486be-529">Routingdienst</span><span class="sxs-lookup"><span data-stu-id="486be-529">Routing Service</span></span>

<span data-ttu-id="486be-530">196</span><span class="sxs-lookup"><span data-stu-id="486be-530">196</span></span>

[<span data-ttu-id="486be-531">Windows 2000-Client Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-531">Windows 2000 Client Support</span></span>](/windows)<br/>

<span data-ttu-id="486be-532">197</span><span class="sxs-lookup"><span data-stu-id="486be-532">197</span></span>

<span data-ttu-id="486be-533">Message Queuing-DCOM-Proxy</span><span class="sxs-lookup"><span data-stu-id="486be-533">Message Queuing DCOM Proxy</span></span>

<span data-ttu-id="486be-534">228</span><span class="sxs-lookup"><span data-stu-id="486be-534">228</span></span>

<span data-ttu-id="486be-535">Multicasting-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-535">Multicasting Support</span></span>

<span data-ttu-id="486be-536">Active Directory Zertifikat Dienste-Rollen Dienste (16)</span><span class="sxs-lookup"><span data-stu-id="486be-536">Active Directory Certificate Services - Role Services (16)</span></span>

<span data-ttu-id="486be-537">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-537">Value</span></span>

<span data-ttu-id="486be-538">Name</span><span class="sxs-lookup"><span data-stu-id="486be-538">Name</span></span>

<span data-ttu-id="486be-539">200</span><span class="sxs-lookup"><span data-stu-id="486be-539">200</span></span>

<span data-ttu-id="486be-540">Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="486be-540">Certification Authority</span></span>

<span data-ttu-id="486be-541">201</span><span class="sxs-lookup"><span data-stu-id="486be-541">201</span></span>

<span data-ttu-id="486be-542">Zertifizierungsstellen-Webregistrierung</span><span class="sxs-lookup"><span data-stu-id="486be-542">Certification Authority Web Enrollment</span></span>

<span data-ttu-id="486be-543">202</span><span class="sxs-lookup"><span data-stu-id="486be-543">202</span></span>

<span data-ttu-id="486be-544">Online-Responder</span><span class="sxs-lookup"><span data-stu-id="486be-544">Online Responder</span></span>

<span data-ttu-id="486be-545">204</span><span class="sxs-lookup"><span data-stu-id="486be-545">204</span></span>

<span data-ttu-id="486be-546">Registrierungsdienst für Netzwerkgeräte</span><span class="sxs-lookup"><span data-stu-id="486be-546">Network Device Enrollment Service</span></span>

<span data-ttu-id="486be-547">318</span><span class="sxs-lookup"><span data-stu-id="486be-547">318</span></span>

[<span data-ttu-id="486be-548">Zertifikatregistrierungs-Webdienst</span><span class="sxs-lookup"><span data-stu-id="486be-548">Certificate Enrollment Web Service</span></span>](/windows)<br/>

<span data-ttu-id="486be-549">319</span><span class="sxs-lookup"><span data-stu-id="486be-549">319</span></span>

[<span data-ttu-id="486be-550">Zertifikatregistrierungsrichtlinien-Webdienst</span><span class="sxs-lookup"><span data-stu-id="486be-550">Certificate Enrollment Policy Web Service</span></span>](/windows)<br/>

<span data-ttu-id="486be-551">Netzwerk Richtlinien-und Zugriffs Dienste: Rollen Dienste (14)</span><span class="sxs-lookup"><span data-stu-id="486be-551">Network Policy and Access Services - Role Services (14)</span></span>

<span data-ttu-id="486be-552">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-552">Value</span></span>

<span data-ttu-id="486be-553">Name</span><span class="sxs-lookup"><span data-stu-id="486be-553">Name</span></span>

<span data-ttu-id="486be-554">205</span><span class="sxs-lookup"><span data-stu-id="486be-554">205</span></span>

[<span data-ttu-id="486be-555">Netzwerkrichtlinienserver</span><span class="sxs-lookup"><span data-stu-id="486be-555">Network Policy Server</span></span>](/windows)

<span data-ttu-id="486be-556">206</span><span class="sxs-lookup"><span data-stu-id="486be-556">206</span></span>

[<span data-ttu-id="486be-557">VPN</span><span class="sxs-lookup"><span data-stu-id="486be-557">VPN</span></span>](#vpn)

<span data-ttu-id="486be-558">207</span><span class="sxs-lookup"><span data-stu-id="486be-558">207</span></span>

[<span data-ttu-id="486be-559">Remote Zugriffs Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-559">Remote Access Services</span></span>](/windows)

<span data-ttu-id="486be-560">208</span><span class="sxs-lookup"><span data-stu-id="486be-560">208</span></span>

[<span data-ttu-id="486be-561">Routing</span><span class="sxs-lookup"><span data-stu-id="486be-561">Routing</span></span>](#routing)

<span data-ttu-id="486be-562">210</span><span class="sxs-lookup"><span data-stu-id="486be-562">210</span></span>

[<span data-ttu-id="486be-563">Integritätsregistrierungsstelle</span><span class="sxs-lookup"><span data-stu-id="486be-563">Health Registration Authority</span></span>](/windows)

<span data-ttu-id="486be-564">250</span><span class="sxs-lookup"><span data-stu-id="486be-564">250</span></span>

[<span data-ttu-id="486be-565">Host Credential Authorization-Protokoll</span><span class="sxs-lookup"><span data-stu-id="486be-565">Host Credential Authorization Protocol</span></span>](/windows)

<span data-ttu-id="486be-566">UDDI-Dienste-Rollen Dienste (11)</span><span class="sxs-lookup"><span data-stu-id="486be-566">UDDI Services - Role Services (11)</span></span>

<span data-ttu-id="486be-567">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-567">Value</span></span>

<span data-ttu-id="486be-568">Name</span><span class="sxs-lookup"><span data-stu-id="486be-568">Name</span></span>

<span data-ttu-id="486be-569">215</span><span class="sxs-lookup"><span data-stu-id="486be-569">215</span></span>

[<span data-ttu-id="486be-570">Webanwendung der UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-570">UDDI Services Web Application</span></span>](/windows)<br/>

<span data-ttu-id="486be-571">216</span><span class="sxs-lookup"><span data-stu-id="486be-571">216</span></span>

[<span data-ttu-id="486be-572">Datenbank der UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-572">UDDI Services Database</span></span>](/windows)<br/>

<span data-ttu-id="486be-573">Windows-Prozess Aktivierungs Dienst: Rollen Dienste (41)</span><span class="sxs-lookup"><span data-stu-id="486be-573">Windows Process Activation Service - Role Services (41)</span></span>

<span data-ttu-id="486be-574">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-574">Value</span></span>

<span data-ttu-id="486be-575">Name</span><span class="sxs-lookup"><span data-stu-id="486be-575">Name</span></span>

<span data-ttu-id="486be-576">217</span><span class="sxs-lookup"><span data-stu-id="486be-576">217</span></span>

<span data-ttu-id="486be-577">Konfigurations-API</span><span class="sxs-lookup"><span data-stu-id="486be-577">Configuration API</span></span>

<span data-ttu-id="486be-578">218</span><span class="sxs-lookup"><span data-stu-id="486be-578">218</span></span>

<span data-ttu-id="486be-579">.NET-Umgebung</span><span class="sxs-lookup"><span data-stu-id="486be-579">.NET Environment</span></span>

<span data-ttu-id="486be-580">219</span><span class="sxs-lookup"><span data-stu-id="486be-580">219</span></span>

<span data-ttu-id="486be-581">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="486be-581">Process Model</span></span>

<span data-ttu-id="486be-582">.NET Framework 3.5.1-Features (36)</span><span class="sxs-lookup"><span data-stu-id="486be-582">.NET Framework 3.5.1 - Features (36)</span></span>

<span data-ttu-id="486be-583">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-583">Value</span></span>

<span data-ttu-id="486be-584">Name</span><span class="sxs-lookup"><span data-stu-id="486be-584">Name</span></span>

<span data-ttu-id="486be-585">220</span><span class="sxs-lookup"><span data-stu-id="486be-585">220</span></span>

<span data-ttu-id="486be-586">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="486be-586">.NET Framework 3.5.1</span></span><br/> [<span data-ttu-id="486be-587">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-587">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-588">221</span><span class="sxs-lookup"><span data-stu-id="486be-588">221</span></span>

<span data-ttu-id="486be-589">WCF-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-589">WCF Activation</span></span>

<span data-ttu-id="486be-590">222</span><span class="sxs-lookup"><span data-stu-id="486be-590">222</span></span>

<span data-ttu-id="486be-591">HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-591">HTTP Activation</span></span>

<span data-ttu-id="486be-592">223</span><span class="sxs-lookup"><span data-stu-id="486be-592">223</span></span>

<span data-ttu-id="486be-593">Nicht-HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-593">Non-HTTP Activation</span></span>

<span data-ttu-id="486be-594">227</span><span class="sxs-lookup"><span data-stu-id="486be-594">227</span></span>

<span data-ttu-id="486be-595">XPS-Viewer</span><span class="sxs-lookup"><span data-stu-id="486be-595">XPS Viewer</span></span><br/>

<span data-ttu-id="486be-596">SNMP-Dienste-Features (59)</span><span class="sxs-lookup"><span data-stu-id="486be-596">SNMP Services - Features (59)</span></span>

<span data-ttu-id="486be-597">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-597">Value</span></span>

<span data-ttu-id="486be-598">Name</span><span class="sxs-lookup"><span data-stu-id="486be-598">Name</span></span>

<span data-ttu-id="486be-599">224</span><span class="sxs-lookup"><span data-stu-id="486be-599">224</span></span>

[<span data-ttu-id="486be-600">SNMP-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-600">SNMP Service</span></span>](/windows)

<span data-ttu-id="486be-601">225</span><span class="sxs-lookup"><span data-stu-id="486be-601">225</span></span>

[<span data-ttu-id="486be-602">SNMP-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="486be-602">SNMP WMI Provider</span></span>](/windows)

<span data-ttu-id="486be-603">Anwendungsdienste Rollen Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-603">Application Services - Role Services</span></span>

<span data-ttu-id="486be-604">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-604">Value</span></span>

<span data-ttu-id="486be-605">Name</span><span class="sxs-lookup"><span data-stu-id="486be-605">Name</span></span>

<span data-ttu-id="486be-606">230</span><span class="sxs-lookup"><span data-stu-id="486be-606">230</span></span>

[<span data-ttu-id="486be-607">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="486be-607">.NET Framework 3.5.1</span></span>](/windows)<br/> [<span data-ttu-id="486be-608">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-608">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-609">231</span><span class="sxs-lookup"><span data-stu-id="486be-609">231</span></span>

[<span data-ttu-id="486be-610">Webserver-Unterstützung (IIS)</span><span class="sxs-lookup"><span data-stu-id="486be-610">Web Server (IIS) Support</span></span>](/windows)

<span data-ttu-id="486be-611">232</span><span class="sxs-lookup"><span data-stu-id="486be-611">232</span></span>

[<span data-ttu-id="486be-612">Com+-Netzwerk Zugriff</span><span class="sxs-lookup"><span data-stu-id="486be-612">COM+ Network Access</span></span>](/windows)

<span data-ttu-id="486be-613">233</span><span class="sxs-lookup"><span data-stu-id="486be-613">233</span></span>

[<span data-ttu-id="486be-614">TCP-Portfreigabe</span><span class="sxs-lookup"><span data-stu-id="486be-614">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="486be-615">234</span><span class="sxs-lookup"><span data-stu-id="486be-615">234</span></span>

[<span data-ttu-id="486be-616">Unterstützung für Windows-Prozess Aktivierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-616">Windows Process Activation Service Support</span></span>](/windows)

<span data-ttu-id="486be-617">235</span><span class="sxs-lookup"><span data-stu-id="486be-617">235</span></span>

[<span data-ttu-id="486be-618">HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-618">HTTP Activation</span></span>](/windows)

<span data-ttu-id="486be-619">236</span><span class="sxs-lookup"><span data-stu-id="486be-619">236</span></span>

[<span data-ttu-id="486be-620">Message Queuing Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-620">Message Queuing Activation</span></span>](/windows)

<span data-ttu-id="486be-621">237</span><span class="sxs-lookup"><span data-stu-id="486be-621">237</span></span>

[<span data-ttu-id="486be-622">TCP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-622">TCP Activation</span></span>](/windows)

<span data-ttu-id="486be-623">238</span><span class="sxs-lookup"><span data-stu-id="486be-623">238</span></span>

[<span data-ttu-id="486be-624">Named Pipes-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-624">Named Pipes Activation</span></span>](/windows)

<span data-ttu-id="486be-625">239</span><span class="sxs-lookup"><span data-stu-id="486be-625">239</span></span>

<span data-ttu-id="486be-626">[Distributed Transactions](/windows) (Verteilte Transaktionen)</span><span class="sxs-lookup"><span data-stu-id="486be-626">[Distributed Transactions](/windows)</span></span>

<span data-ttu-id="486be-627">240</span><span class="sxs-lookup"><span data-stu-id="486be-627">240</span></span>

[<span data-ttu-id="486be-628">Eingehende Remote Transaktionen</span><span class="sxs-lookup"><span data-stu-id="486be-628">Incoming Remote Transactions</span></span>](/windows)

<span data-ttu-id="486be-629">241</span><span class="sxs-lookup"><span data-stu-id="486be-629">241</span></span>

[<span data-ttu-id="486be-630">Ausgehende Remote Transaktionen</span><span class="sxs-lookup"><span data-stu-id="486be-630">Outgoing Remote Transactions</span></span>](/windows)

<span data-ttu-id="486be-631">242</span><span class="sxs-lookup"><span data-stu-id="486be-631">242</span></span>

[<span data-ttu-id="486be-632">WS-automatische Transaktionen</span><span class="sxs-lookup"><span data-stu-id="486be-632">WS-Automatic Transactions</span></span>](/windows)

<span data-ttu-id="486be-633">353</span><span class="sxs-lookup"><span data-stu-id="486be-633">353</span></span>

[<span data-ttu-id="486be-634">Anwendungs Server Erweiterungen für .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="486be-634">Application Server Extensions for .NET 4.0</span></span>](/windows)<br/>

<span data-ttu-id="486be-635">Windows-Bereitstellungs Dienste-Rolle (19)</span><span class="sxs-lookup"><span data-stu-id="486be-635">Windows Deployment Services - Role (19)</span></span>

<span data-ttu-id="486be-636">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-636">Value</span></span>

<span data-ttu-id="486be-637">Name</span><span class="sxs-lookup"><span data-stu-id="486be-637">Name</span></span>

<span data-ttu-id="486be-638">251</span><span class="sxs-lookup"><span data-stu-id="486be-638">251</span></span>

<span data-ttu-id="486be-639">Bereitstellungsserver</span><span class="sxs-lookup"><span data-stu-id="486be-639">Deployment Server</span></span>

<span data-ttu-id="486be-640">252</span><span class="sxs-lookup"><span data-stu-id="486be-640">252</span></span>

<span data-ttu-id="486be-641">Transportserver</span><span class="sxs-lookup"><span data-stu-id="486be-641">Transport Server</span></span>

<span data-ttu-id="486be-642">Rollen Dienste für Active Directory Rights Management Services (17)</span><span class="sxs-lookup"><span data-stu-id="486be-642">Active Directory Rights Management Services - Role Services (17)</span></span>

<span data-ttu-id="486be-643">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-643">Value</span></span>

<span data-ttu-id="486be-644">Name</span><span class="sxs-lookup"><span data-stu-id="486be-644">Name</span></span>

<span data-ttu-id="486be-645">253</span><span class="sxs-lookup"><span data-stu-id="486be-645">253</span></span>

<span data-ttu-id="486be-646">Active Directory-Rechteverwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="486be-646">Active Directory Rights Management Server</span></span>

<span data-ttu-id="486be-647">254</span><span class="sxs-lookup"><span data-stu-id="486be-647">254</span></span>

<span data-ttu-id="486be-648">Unterstützung für Identitätsverbund</span><span class="sxs-lookup"><span data-stu-id="486be-648">Identity Federation Support</span></span>

<span data-ttu-id="486be-649">Remoteserver-Verwaltungstools (67)</span><span class="sxs-lookup"><span data-stu-id="486be-649">Remote Server Administration Tools (67)</span></span>

<span data-ttu-id="486be-650">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-650">Value</span></span>

<span data-ttu-id="486be-651">Name</span><span class="sxs-lookup"><span data-stu-id="486be-651">Name</span></span>

<span data-ttu-id="486be-652">256</span><span class="sxs-lookup"><span data-stu-id="486be-652">256</span></span>

[<span data-ttu-id="486be-653">Rollenverwaltungstools</span><span class="sxs-lookup"><span data-stu-id="486be-653">Role Administration Tools</span></span>](/windows)

<span data-ttu-id="486be-654">257</span><span class="sxs-lookup"><span data-stu-id="486be-654">257</span></span>

[<span data-ttu-id="486be-655">AD DS-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-655">AD DS Tools</span></span>](/windows)<br/> [<span data-ttu-id="486be-656">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-656">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-657">258</span><span class="sxs-lookup"><span data-stu-id="486be-657">258</span></span>

[<span data-ttu-id="486be-658">AD LDS Snap-Ins und Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="486be-658">AD LDS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="486be-659">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-659">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-660">259</span><span class="sxs-lookup"><span data-stu-id="486be-660">259</span></span>

<span data-ttu-id="486be-661">Tools für Active Directory-Zertifikatdienste</span><span class="sxs-lookup"><span data-stu-id="486be-661">Active Directory Certificate Services Tools</span></span>

<span data-ttu-id="486be-662">260</span><span class="sxs-lookup"><span data-stu-id="486be-662">260</span></span>

[<span data-ttu-id="486be-663">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="486be-663">Network Policy and Access Services</span></span>](/windows)

<span data-ttu-id="486be-664">261</span><span class="sxs-lookup"><span data-stu-id="486be-664">261</span></span>

<span data-ttu-id="486be-665">Druck-und Dokumentdienste Tools</span><span class="sxs-lookup"><span data-stu-id="486be-665">Print and Document Services Tools</span></span><br/> [<span data-ttu-id="486be-666">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-666">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-667">262</span><span class="sxs-lookup"><span data-stu-id="486be-667">262</span></span>

[<span data-ttu-id="486be-668">Active Directory-Rechteverwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="486be-668">Active Directory Rights Management Services</span></span>](/windows)

<span data-ttu-id="486be-669">263</span><span class="sxs-lookup"><span data-stu-id="486be-669">263</span></span>

[<span data-ttu-id="486be-670">Tools für Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="486be-670">Remote Desktop Services Tools</span></span>](/windows)<br/> [<span data-ttu-id="486be-671">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-671">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-672">264</span><span class="sxs-lookup"><span data-stu-id="486be-672">264</span></span>

<span data-ttu-id="486be-673">Tools der Windows-Bereitstellungs Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-673">Windows Deployment Services Tools</span></span>

<span data-ttu-id="486be-674">265</span><span class="sxs-lookup"><span data-stu-id="486be-674">265</span></span>

[<span data-ttu-id="486be-675">Featureverwaltungstools</span><span class="sxs-lookup"><span data-stu-id="486be-675">Feature Administration Tools</span></span>](/windows)

<span data-ttu-id="486be-676">266</span><span class="sxs-lookup"><span data-stu-id="486be-676">266</span></span>

<span data-ttu-id="486be-677">Tools zur BitLocker-Laufwerkverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="486be-677">BitLocker Drive Encryption Tools</span></span>

<span data-ttu-id="486be-678">267</span><span class="sxs-lookup"><span data-stu-id="486be-678">267</span></span>

<span data-ttu-id="486be-679">Tools für BITS-Servererweiterungen</span><span class="sxs-lookup"><span data-stu-id="486be-679">BITS Server Extensions Tools</span></span>

<span data-ttu-id="486be-680">268</span><span class="sxs-lookup"><span data-stu-id="486be-680">268</span></span>

[<span data-ttu-id="486be-681">Failoverclusteringtools</span><span class="sxs-lookup"><span data-stu-id="486be-681">Failover Clustering Tools</span></span>](/windows)

<span data-ttu-id="486be-682">269</span><span class="sxs-lookup"><span data-stu-id="486be-682">269</span></span>

<span data-ttu-id="486be-683">Tools für Netzwerklastenausgleich</span><span class="sxs-lookup"><span data-stu-id="486be-683">Network Load Balancing Tools</span></span>

<span data-ttu-id="486be-684">270</span><span class="sxs-lookup"><span data-stu-id="486be-684">270</span></span>

<span data-ttu-id="486be-685">SMTP-Server Tools</span><span class="sxs-lookup"><span data-stu-id="486be-685">SMTP Server Tools</span></span>

<span data-ttu-id="486be-686">273</span><span class="sxs-lookup"><span data-stu-id="486be-686">273</span></span>

[<span data-ttu-id="486be-687">DNS-Servertools</span><span class="sxs-lookup"><span data-stu-id="486be-687">DNS Server Tools</span></span>](/windows)

<span data-ttu-id="486be-688">277</span><span class="sxs-lookup"><span data-stu-id="486be-688">277</span></span>

<span data-ttu-id="486be-689">Tools für Dateidienste</span><span class="sxs-lookup"><span data-stu-id="486be-689">File Services Tools</span></span>

<span data-ttu-id="486be-690">278</span><span class="sxs-lookup"><span data-stu-id="486be-690">278</span></span>

<span data-ttu-id="486be-691">Verteiltes Dateisystem Tools</span><span class="sxs-lookup"><span data-stu-id="486be-691">Distributed File System Tools</span></span>

<span data-ttu-id="486be-692">279</span><span class="sxs-lookup"><span data-stu-id="486be-692">279</span></span>

<span data-ttu-id="486be-693">Tools für den Ressourcen-Manager für Dateiserver</span><span class="sxs-lookup"><span data-stu-id="486be-693">File Server Resource Manager Tools</span></span>

<span data-ttu-id="486be-694">280</span><span class="sxs-lookup"><span data-stu-id="486be-694">280</span></span>

[<span data-ttu-id="486be-695">Dienste für Network File System-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-695">Services For Network File System Tools</span></span>](/windows)

<span data-ttu-id="486be-696">281</span><span class="sxs-lookup"><span data-stu-id="486be-696">281</span></span>

<span data-ttu-id="486be-697">Webserver (IIS)-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-697">Web Server (IIS) Tools</span></span>

<span data-ttu-id="486be-698">284</span><span class="sxs-lookup"><span data-stu-id="486be-698">284</span></span>

[<span data-ttu-id="486be-699">Remotedesktop-Sitzungshost Tools</span><span class="sxs-lookup"><span data-stu-id="486be-699">Remote Desktop Session Host Tools</span></span>](/windows)<br/> [<span data-ttu-id="486be-700">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-700">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-701">285</span><span class="sxs-lookup"><span data-stu-id="486be-701">285</span></span>

<span data-ttu-id="486be-702">Remotedesktop Gateway-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-702">Remote Desktop Gateway Tools</span></span><br/> [<span data-ttu-id="486be-703">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-703">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-704">286</span><span class="sxs-lookup"><span data-stu-id="486be-704">286</span></span>

<span data-ttu-id="486be-705">Remotedesktop Lizenzierungs Tools</span><span class="sxs-lookup"><span data-stu-id="486be-705">Remote Desktop Licensing Tools</span></span><br/> [<span data-ttu-id="486be-706">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-706">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-707">288</span><span class="sxs-lookup"><span data-stu-id="486be-707">288</span></span>

<span data-ttu-id="486be-708">Faxserver Tools</span><span class="sxs-lookup"><span data-stu-id="486be-708">Fax Server Tools</span></span>

<span data-ttu-id="486be-709">290</span><span class="sxs-lookup"><span data-stu-id="486be-709">290</span></span>

<span data-ttu-id="486be-710">WINS-Server Tools</span><span class="sxs-lookup"><span data-stu-id="486be-710">WINS Server Tools</span></span>

<span data-ttu-id="486be-711">291</span><span class="sxs-lookup"><span data-stu-id="486be-711">291</span></span>

[<span data-ttu-id="486be-712">Tools für UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-712">UDDI Services Tools</span></span>](/windows)<br/>

<span data-ttu-id="486be-713">292</span><span class="sxs-lookup"><span data-stu-id="486be-713">292</span></span>

<span data-ttu-id="486be-714">Zertifizierungsstellen Tools</span><span class="sxs-lookup"><span data-stu-id="486be-714">Certification Authority Tools</span></span>

<span data-ttu-id="486be-715">293</span><span class="sxs-lookup"><span data-stu-id="486be-715">293</span></span>

<span data-ttu-id="486be-716">Online-Respondertools</span><span class="sxs-lookup"><span data-stu-id="486be-716">Online Responder Tools</span></span>

<span data-ttu-id="486be-717">297</span><span class="sxs-lookup"><span data-stu-id="486be-717">297</span></span>

[<span data-ttu-id="486be-718">Server für NIS Tools</span><span class="sxs-lookup"><span data-stu-id="486be-718">Server for NIS Tools</span></span>](/windows)

<span data-ttu-id="486be-719">299</span><span class="sxs-lookup"><span data-stu-id="486be-719">299</span></span>

[<span data-ttu-id="486be-720">AD DS-Snap-Ins und -Befehlszeilentools</span><span class="sxs-lookup"><span data-stu-id="486be-720">AD DS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="486be-721">Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-721">name change</span></span>](/windows)<br/>

<span data-ttu-id="486be-722">300</span><span class="sxs-lookup"><span data-stu-id="486be-722">300</span></span>

[<span data-ttu-id="486be-723">Active Directory-Verwaltungscenter</span><span class="sxs-lookup"><span data-stu-id="486be-723">Active Directory Administrative Center</span></span>](/windows)

<span data-ttu-id="486be-724">301</span><span class="sxs-lookup"><span data-stu-id="486be-724">301</span></span>

<span data-ttu-id="486be-725">Hyper-V-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-725">Hyper-V Tools</span></span>

<span data-ttu-id="486be-726">323</span><span class="sxs-lookup"><span data-stu-id="486be-726">323</span></span>

[<span data-ttu-id="486be-727">BitLocker-Wiederherstellungs Kenn Wort Anzeige</span><span class="sxs-lookup"><span data-stu-id="486be-727">BitLocker Recovery Password Viewer</span></span>](/windows)<br/>

<span data-ttu-id="486be-728">326</span><span class="sxs-lookup"><span data-stu-id="486be-728">326</span></span>

[<span data-ttu-id="486be-729">Verwaltungsdienstprogramme für die BitLocker-Laufwerkverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="486be-729">BitLocker Drive Encryption Administration Utilities</span></span>](/windows)<br/>

<span data-ttu-id="486be-730">329</span><span class="sxs-lookup"><span data-stu-id="486be-730">329</span></span>

[<span data-ttu-id="486be-731">AD DS- und AD LDS-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-731">AD DS and AD LDS Tools</span></span>](/windows)<br/>

<span data-ttu-id="486be-732">330</span><span class="sxs-lookup"><span data-stu-id="486be-732">330</span></span>

<span data-ttu-id="486be-733">Active Directory-Verwaltungscenter</span><span class="sxs-lookup"><span data-stu-id="486be-733">Active Directory Administrative Center</span></span><br/>

<span data-ttu-id="486be-734">331</span><span class="sxs-lookup"><span data-stu-id="486be-734">331</span></span>

[<span data-ttu-id="486be-735">Active Directory-Modul für Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-735">Active Directory module for Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="486be-736">337</span><span class="sxs-lookup"><span data-stu-id="486be-736">337</span></span>

[<span data-ttu-id="486be-737">Remotedesktopverbindung Broker-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-737">Remote Desktop Connection Broker Tools</span></span>](/windows)<br/>

<span data-ttu-id="486be-738">410</span><span class="sxs-lookup"><span data-stu-id="486be-738">410</span></span>

[<span data-ttu-id="486be-739">IP-Adressverwaltung (IPAM)-Client</span><span class="sxs-lookup"><span data-stu-id="486be-739">IP Address Management (IPAM) Client</span></span>](/windows)

<span data-ttu-id="486be-740">450</span><span class="sxs-lookup"><span data-stu-id="486be-740">450</span></span>

[<span data-ttu-id="486be-741">Hyper-V-Modul für Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-741">Hyper-V Module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="486be-742">462</span><span class="sxs-lookup"><span data-stu-id="486be-742">462</span></span>

[<span data-ttu-id="486be-743">Active Directory Rights Management Services Tools</span><span class="sxs-lookup"><span data-stu-id="486be-743">Active Directory Rights Management Services Tools</span></span>](/windows)

<span data-ttu-id="486be-744">465</span><span class="sxs-lookup"><span data-stu-id="486be-744">465</span></span>

[<span data-ttu-id="486be-745">Freigabe-und Speicher Verwaltungs Tool</span><span class="sxs-lookup"><span data-stu-id="486be-745">Share and Storage Management Tool</span></span>](/windows)

<span data-ttu-id="486be-746">471</span><span class="sxs-lookup"><span data-stu-id="486be-746">471</span></span>

[<span data-ttu-id="486be-747">Tools für die Remotezugriffsverwaltung</span><span class="sxs-lookup"><span data-stu-id="486be-747">Remote Access Management Tools</span></span>](/windows)

<span data-ttu-id="486be-748">472</span><span class="sxs-lookup"><span data-stu-id="486be-748">472</span></span>

[<span data-ttu-id="486be-749">RAS-Modul für Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-749">Remote Access module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="486be-750">473</span><span class="sxs-lookup"><span data-stu-id="486be-750">473</span></span>

[<span data-ttu-id="486be-751">Remote Zugriffs-GUI und-Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="486be-751">Remote Access GUI and Command-Line Tools</span></span>](/windows)

<span data-ttu-id="486be-752">474</span><span class="sxs-lookup"><span data-stu-id="486be-752">474</span></span>

[<span data-ttu-id="486be-753">Windows Server Update Services-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-753">Windows Server Update Services Tools</span></span>](/windows)

<span data-ttu-id="486be-754">476</span><span class="sxs-lookup"><span data-stu-id="486be-754">476</span></span>

[<span data-ttu-id="486be-755">Diagnose Tools für Remotedesktop Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="486be-755">Remote Desktop Licensing Diagnoser Tools</span></span>](/windows)

<span data-ttu-id="486be-756">479</span><span class="sxs-lookup"><span data-stu-id="486be-756">479</span></span>

[<span data-ttu-id="486be-757">SNMP-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-757">SNMP Tools</span></span>](/windows)

<span data-ttu-id="486be-758">480</span><span class="sxs-lookup"><span data-stu-id="486be-758">480</span></span>

[<span data-ttu-id="486be-759">Volumenaktivierungstools</span><span class="sxs-lookup"><span data-stu-id="486be-759">Volume Activation Tools</span></span>](/windows)

<span data-ttu-id="486be-760">Windows Server-Sicherung-Features (39)</span><span class="sxs-lookup"><span data-stu-id="486be-760">Windows Server Backup - Features (39)</span></span>

<span data-ttu-id="486be-761">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-761">Value</span></span>

<span data-ttu-id="486be-762">Name</span><span class="sxs-lookup"><span data-stu-id="486be-762">Name</span></span>

<span data-ttu-id="486be-763">296</span><span class="sxs-lookup"><span data-stu-id="486be-763">296</span></span>

[<span data-ttu-id="486be-764">Windows Server-Sicherung</span><span class="sxs-lookup"><span data-stu-id="486be-764">Windows Server Backup</span></span>](/windows)

<span data-ttu-id="486be-765">297</span><span class="sxs-lookup"><span data-stu-id="486be-765">297</span></span>

[<span data-ttu-id="486be-766">Befehlszeilen Tools</span><span class="sxs-lookup"><span data-stu-id="486be-766">Command Line Tools</span></span>](/windows)

<span data-ttu-id="486be-767">Freihand-und Handschriftdienste-Features (310)</span><span class="sxs-lookup"><span data-stu-id="486be-767">Ink and Handwriting Services - Features (310)</span></span>

<span data-ttu-id="486be-768">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-768">Value</span></span>

<span data-ttu-id="486be-769">Name</span><span class="sxs-lookup"><span data-stu-id="486be-769">Name</span></span>

<span data-ttu-id="486be-770">311</span><span class="sxs-lookup"><span data-stu-id="486be-770">311</span></span>

[<span data-ttu-id="486be-771">Freihand Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-771">Ink Support</span></span>](/windows)<br/>

<span data-ttu-id="486be-772">312</span><span class="sxs-lookup"><span data-stu-id="486be-772">312</span></span>

[<span data-ttu-id="486be-773">Handschrifterkennung</span><span class="sxs-lookup"><span data-stu-id="486be-773">Handwriting Recognition</span></span>](/windows)<br/>

<span data-ttu-id="486be-774">Background Intelligent Transfer Service (Bits)-Features (335)</span><span class="sxs-lookup"><span data-stu-id="486be-774">Background Intelligent Transfer Service (BITS) - Features (335)</span></span>

<span data-ttu-id="486be-775">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-775">Value</span></span>

<span data-ttu-id="486be-776">Name</span><span class="sxs-lookup"><span data-stu-id="486be-776">Name</span></span>

<span data-ttu-id="486be-777">54</span><span class="sxs-lookup"><span data-stu-id="486be-777">54</span></span>

<span data-ttu-id="486be-778">IIS-Servererweiterung</span><span class="sxs-lookup"><span data-stu-id="486be-778">IIS Server Extension</span></span>

<span data-ttu-id="486be-779">332</span><span class="sxs-lookup"><span data-stu-id="486be-779">332</span></span>

[<span data-ttu-id="486be-780">Compact Server</span><span class="sxs-lookup"><span data-stu-id="486be-780">Compact Server</span></span>](/windows)<br/>

<span data-ttu-id="486be-781">WOW64-Unterstützung: Features (340)</span><span class="sxs-lookup"><span data-stu-id="486be-781">Wow64 Support - Features (340)</span></span>

<span data-ttu-id="486be-782">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-782">Value</span></span>

<span data-ttu-id="486be-783">Name</span><span class="sxs-lookup"><span data-stu-id="486be-783">Name</span></span>

<span data-ttu-id="486be-784">341</span><span class="sxs-lookup"><span data-stu-id="486be-784">341</span></span>

[<span data-ttu-id="486be-785">WOW64</span><span class="sxs-lookup"><span data-stu-id="486be-785">WoW64</span></span>](#wow64)<br/>

<span data-ttu-id="486be-786">342</span><span class="sxs-lookup"><span data-stu-id="486be-786">342</span></span>

[<span data-ttu-id="486be-787">WOW64 für .NET Framework 2,0 und Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-787">WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="486be-788">343</span><span class="sxs-lookup"><span data-stu-id="486be-788">343</span></span>

[<span data-ttu-id="486be-789">WOW64 für .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="486be-789">WoW64 for .NET Framework 2.0</span></span>](/windows)<br/>

<span data-ttu-id="486be-790">344</span><span class="sxs-lookup"><span data-stu-id="486be-790">344</span></span>

[<span data-ttu-id="486be-791">WOW64 für PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-791">WoW64 for PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="486be-792">345</span><span class="sxs-lookup"><span data-stu-id="486be-792">345</span></span>

[<span data-ttu-id="486be-793">WOW64 für .NET Framework 3,0 und 3,5</span><span class="sxs-lookup"><span data-stu-id="486be-793">WoW64 for .NET Framework 3.0 and 3.5</span></span>](/windows)<br/>

<span data-ttu-id="486be-794">346</span><span class="sxs-lookup"><span data-stu-id="486be-794">346</span></span>

[<span data-ttu-id="486be-795">WOW64 für Druckdienste</span><span class="sxs-lookup"><span data-stu-id="486be-795">WoW64 for Print Services</span></span>](/windows)<br/>

<span data-ttu-id="486be-796">347</span><span class="sxs-lookup"><span data-stu-id="486be-796">347</span></span>

[<span data-ttu-id="486be-797">WOW64 für Failoverclustering</span><span class="sxs-lookup"><span data-stu-id="486be-797">WoW64 for Failover Clustering</span></span>](/windows)<br/>

<span data-ttu-id="486be-798">348</span><span class="sxs-lookup"><span data-stu-id="486be-798">348</span></span>

[<span data-ttu-id="486be-799">WOW64 für Eingabemethoden-Editor</span><span class="sxs-lookup"><span data-stu-id="486be-799">WoW64 for Input Method Editor</span></span>](/windows)<br/>

<span data-ttu-id="486be-800">349</span><span class="sxs-lookup"><span data-stu-id="486be-800">349</span></span>

[<span data-ttu-id="486be-801">WOW64 für Subsystem für UNIX-basierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="486be-801">WoW64 for Subsystem for UNIX-based Applications</span></span>](/windows)<br/>

<span data-ttu-id="486be-802">Benutzeroberflächen und Infrastruktur Rollen Dienste (447)</span><span class="sxs-lookup"><span data-stu-id="486be-802">User Interfaces and Infrastructure - Role Services (447)</span></span>

<span data-ttu-id="486be-803">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-803">Value</span></span>

<span data-ttu-id="486be-804">Name</span><span class="sxs-lookup"><span data-stu-id="486be-804">Name</span></span>

<span data-ttu-id="486be-805">35</span><span class="sxs-lookup"><span data-stu-id="486be-805">35</span></span>

[<span data-ttu-id="486be-806">Desktop Darstellung</span><span class="sxs-lookup"><span data-stu-id="486be-806">Desktop Experience</span></span>](/windows)

<span data-ttu-id="486be-807">99</span><span class="sxs-lookup"><span data-stu-id="486be-807">99</span></span>

[<span data-ttu-id="486be-808">Grafische Shell für Server</span><span class="sxs-lookup"><span data-stu-id="486be-808">Server Graphical Shell</span></span>](/windows)

<span data-ttu-id="486be-809">Windows Server Update Services-Features (404)</span><span class="sxs-lookup"><span data-stu-id="486be-809">Window Server Update Services - Features (404)</span></span>

<span data-ttu-id="486be-810">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-810">Value</span></span>

<span data-ttu-id="486be-811">Name</span><span class="sxs-lookup"><span data-stu-id="486be-811">Name</span></span>

<span data-ttu-id="486be-812">405</span><span class="sxs-lookup"><span data-stu-id="486be-812">405</span></span>

[<span data-ttu-id="486be-813">API-und PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="486be-813">API and PowerShell cmdlets</span></span>](/windows)

<span data-ttu-id="486be-814">406</span><span class="sxs-lookup"><span data-stu-id="486be-814">406</span></span>

[<span data-ttu-id="486be-815">SQL Server Konnektivität</span><span class="sxs-lookup"><span data-stu-id="486be-815">SQL Server Connectivity</span></span>](/windows)

<span data-ttu-id="486be-816">407</span><span class="sxs-lookup"><span data-stu-id="486be-816">407</span></span>

[<span data-ttu-id="486be-817">WSUS-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-817">WSUS Services</span></span>](/windows)

<span data-ttu-id="486be-818">408</span><span class="sxs-lookup"><span data-stu-id="486be-818">408</span></span>

[<span data-ttu-id="486be-819">Verwaltungskonsole für die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="486be-819">User Interface Management Console</span></span>](/windows)

<span data-ttu-id="486be-820">449</span><span class="sxs-lookup"><span data-stu-id="486be-820">449</span></span>

[<span data-ttu-id="486be-821">WID-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="486be-821">WID Connectivity</span></span>](/windows)

<span data-ttu-id="486be-822">Windows PowerShell-Features (417)</span><span class="sxs-lookup"><span data-stu-id="486be-822">Windows PowerShell - Features (417)</span></span>

<span data-ttu-id="486be-823">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-823">Value</span></span>

<span data-ttu-id="486be-824">Name</span><span class="sxs-lookup"><span data-stu-id="486be-824">Name</span></span>

<span data-ttu-id="486be-825">411</span><span class="sxs-lookup"><span data-stu-id="486be-825">411</span></span>

[<span data-ttu-id="486be-826">Windows PowerShell 2,0-Engine</span><span class="sxs-lookup"><span data-stu-id="486be-826">Windows PowerShell 2.0 Engine</span></span>](/windows)

<span data-ttu-id="486be-827">412</span><span class="sxs-lookup"><span data-stu-id="486be-827">412</span></span>

[<span data-ttu-id="486be-828">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="486be-828">Windows PowerShell 3.0</span></span>](/windows)

<span data-ttu-id="486be-829">448</span><span class="sxs-lookup"><span data-stu-id="486be-829">448</span></span>

[<span data-ttu-id="486be-830">Windows PowerShell Web Access</span><span class="sxs-lookup"><span data-stu-id="486be-830">Windows PowerShell Web Access</span></span>](/windows)

<span data-ttu-id="486be-831">1000</span><span class="sxs-lookup"><span data-stu-id="486be-831">1000</span></span>

[<span data-ttu-id="486be-832">Windows PowerShell-Dienst zum Konfigurieren des gewünschten Zustands</span><span class="sxs-lookup"><span data-stu-id="486be-832">Windows PowerShell Desired State Configuration Service</span></span>](/windows)

<span data-ttu-id="486be-833">.NET Framework 4,5-Features (418)</span><span class="sxs-lookup"><span data-stu-id="486be-833">.NET Framework 4.5 - Features (418)</span></span>

<span data-ttu-id="486be-834">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-834">Value</span></span>

<span data-ttu-id="486be-835">Name</span><span class="sxs-lookup"><span data-stu-id="486be-835">Name</span></span>

<span data-ttu-id="486be-836">419</span><span class="sxs-lookup"><span data-stu-id="486be-836">419</span></span>

[<span data-ttu-id="486be-837">.NET Framework 4,5 erweitert</span><span class="sxs-lookup"><span data-stu-id="486be-837">.NET Framework 4.5 Extended</span></span>](/windows)

<span data-ttu-id="486be-838">420</span><span class="sxs-lookup"><span data-stu-id="486be-838">420</span></span>

[<span data-ttu-id="486be-839">WCF-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-839">WCF Services</span></span>](/windows)

<span data-ttu-id="486be-840">421</span><span class="sxs-lookup"><span data-stu-id="486be-840">421</span></span>

[<span data-ttu-id="486be-841">HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-841">HTTP Activation</span></span>](/windows)

<span data-ttu-id="486be-842">422</span><span class="sxs-lookup"><span data-stu-id="486be-842">422</span></span>

[<span data-ttu-id="486be-843">Message Queuing Aktivierung (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="486be-843">Message Queuing (MSMQ) Activation</span></span>](/windows)

<span data-ttu-id="486be-844">423</span><span class="sxs-lookup"><span data-stu-id="486be-844">423</span></span>

[<span data-ttu-id="486be-845">Named Pipe-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-845">Named Pipe Activation</span></span>](/windows)

<span data-ttu-id="486be-846">424</span><span class="sxs-lookup"><span data-stu-id="486be-846">424</span></span>

[<span data-ttu-id="486be-847">TCP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-847">TCP Activation</span></span>](/windows)

<span data-ttu-id="486be-848">425</span><span class="sxs-lookup"><span data-stu-id="486be-848">425</span></span>

[<span data-ttu-id="486be-849">TCP-Portfreigabe</span><span class="sxs-lookup"><span data-stu-id="486be-849">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="486be-850">429</span><span class="sxs-lookup"><span data-stu-id="486be-850">429</span></span>

[<span data-ttu-id="486be-851">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="486be-851">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="486be-852">Remote Zugriff-Rolle (468)</span><span class="sxs-lookup"><span data-stu-id="486be-852">Remote Access - Role (468)</span></span>

<span data-ttu-id="486be-853">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-853">Value</span></span>

<span data-ttu-id="486be-854">Name</span><span class="sxs-lookup"><span data-stu-id="486be-854">Name</span></span>

<span data-ttu-id="486be-855">469</span><span class="sxs-lookup"><span data-stu-id="486be-855">469</span></span>

[<span data-ttu-id="486be-856">DirectAccess und VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="486be-856">DirectAccess and VPN (RAS)</span></span>](/windows)

<span data-ttu-id="486be-857">470</span><span class="sxs-lookup"><span data-stu-id="486be-857">470</span></span>

[<span data-ttu-id="486be-858">Routing</span><span class="sxs-lookup"><span data-stu-id="486be-858">Routing</span></span>](#routing)

<span data-ttu-id="486be-859">Datei-und Speicherdienste-Rolle (481)</span><span class="sxs-lookup"><span data-stu-id="486be-859">File and Storage Services - Role (481)</span></span>

<span data-ttu-id="486be-860">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-860">Value</span></span>

<span data-ttu-id="486be-861">Name</span><span class="sxs-lookup"><span data-stu-id="486be-861">Name</span></span>

<span data-ttu-id="486be-862">482</span><span class="sxs-lookup"><span data-stu-id="486be-862">482</span></span>

[<span data-ttu-id="486be-863">Speicherdienste</span><span class="sxs-lookup"><span data-stu-id="486be-863">Storage Services</span></span>](/windows)

<span data-ttu-id="486be-864">484</span><span class="sxs-lookup"><span data-stu-id="486be-864">484</span></span>

[<span data-ttu-id="486be-865">Verwaltungs Tools für Failovercluster</span><span class="sxs-lookup"><span data-stu-id="486be-865">Failover Cluster Management Tools</span></span>](/windows)



 

</dd> <dt>

<span data-ttu-id="486be-866">**Name**</span><span class="sxs-lookup"><span data-stu-id="486be-866">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="486be-867">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="486be-867">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="486be-868">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="486be-868">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="486be-869">Anzeige Name der Server Funktion, z. b. "Dateiserver", "Druckserver" oder "Desktop Darstellung".</span><span class="sxs-lookup"><span data-stu-id="486be-869">Display name of the server feature, such as "File Server", "Print Server", or "Desktop Experience".</span></span>

</dd> <dt>

<span data-ttu-id="486be-870">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="486be-870">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="486be-871">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="486be-871">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="486be-872">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="486be-872">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="486be-873">ID-Nummer der übergeordneten Server Funktion.</span><span class="sxs-lookup"><span data-stu-id="486be-873">ID number of the parent server feature.</span></span> <span data-ttu-id="486be-874">Diese Eigenschaft ist 0, wenn die Funktion, die von der aktuellen Instanz der-Klasse dargestellt wird, über keine übergeordnete Funktion verfügt.</span><span class="sxs-lookup"><span data-stu-id="486be-874">This property is 0 if the feature represented by the current instance of the class does not have a parent feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="486be-875">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="486be-875">Remarks</span></span>

<span data-ttu-id="486be-876">Weitere Informationen zu Server Funktionen finden Sie in der [technischen Übersicht zu Windows Server 2008 Server-Manager](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="486be-876">Read the [Windows Server 2008 Server Manager Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) to learn about server features.</span></span>

<span data-ttu-id="486be-877">Unternehmen, die keine Verwaltungssoftware verwenden, die Serverfunktionen meldet (z. b. System Center Operations Manager mit installierten Management Packs), können diese Informationen abrufen, indem Sie die **Win32 \_ Serverfeature** -Klasse Abfragen.</span><span class="sxs-lookup"><span data-stu-id="486be-877">Enterprises that do not use management software that reports server features, such as System Center Operations Manager with management packs installed, can get that information by querying the **Win32\_ServerFeature** class.</span></span>

<span data-ttu-id="486be-878">Sie können die Remoting-Features von WMI oder WinRM verwenden, um Server Funktions Informationen von Remote Servern zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="486be-878">You can use the remoting features of WMI or WinRM to get server feature information from remote servers.</span></span> <span data-ttu-id="486be-879">Weitere Informationen zu Remote-WMI-DCOM-Verbindungen finden [Sie unter Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="486be-879">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="486be-880">Weitere Informationen über WinRM finden Sie unter Windows-Remoteverwaltung.</span><span class="sxs-lookup"><span data-stu-id="486be-880">For more information about WinRM, see Windows Remote Management.</span></span>

<span data-ttu-id="486be-881">Windows Server 2012: **Win32 \_ Server Feature** ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="486be-881">Windows Server 2012: **Win32\_ServerFeature** has been deprecated.</span></span> <span data-ttu-id="486be-882">Für den programmgesteuerten Zugriff auf Windows Server-Funktions Informationen können Sie die [Server-Manager-Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10))verwenden.</span><span class="sxs-lookup"><span data-stu-id="486be-882">To access windows server feature information programmatically, you can use the [Server Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span></span>

### <a name="windows-server-2012-r2"></a><span data-ttu-id="486be-883">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="486be-883">Windows Server 2012 R2</span></span>

<dl> <dt>

<span data-ttu-id="486be-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Anwendungs Server</span><span class="sxs-lookup"><span data-stu-id="486be-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Application Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-885">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-885">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming-Media Services</span><span class="sxs-lookup"><span data-stu-id="486be-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-887">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-887">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory-Verbunddienste (AD FS)</span><span class="sxs-lookup"><span data-stu-id="486be-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-889">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-889">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP-Server</span><span class="sxs-lookup"><span data-stu-id="486be-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-891">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-891">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS-Server</span><span class="sxs-lookup"><span data-stu-id="486be-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-893">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-893">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="486be-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remote Desktop Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-895">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-895">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="486be-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-897">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-897">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failoverclustering</span><span class="sxs-lookup"><span data-stu-id="486be-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="486be-899">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-899">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Netzwerk Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="486be-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network Load Balancing</span></span>
</dt> <dd>

<span data-ttu-id="486be-901">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-901">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1-Features</span><span class="sxs-lookup"><span data-stu-id="486be-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Features</span></span>
</dt> <dd>

<span data-ttu-id="486be-903">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-903">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows-System Ressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="486be-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="486be-905">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-905">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server-Sicherung Features</span><span class="sxs-lookup"><span data-stu-id="486be-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup Features</span></span>
</dt> <dd>

<span data-ttu-id="486be-907">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-907">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Assistance</span></span>
</dt> <dd>

<span data-ttu-id="486be-909">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-909">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet-Client</span><span class="sxs-lookup"><span data-stu-id="486be-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client</span></span>
</dt> <dd>

<span data-ttu-id="486be-911">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-911">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet-Server</span><span class="sxs-lookup"><span data-stu-id="486be-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-913">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-913">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem für UNIX-basierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="486be-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem For Unix-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="486be-915">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-915">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Interne Windows-Datenbank</span><span class="sxs-lookup"><span data-stu-id="486be-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span></span>
</dt> <dd>

<span data-ttu-id="486be-917">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-917">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Speicher-Manager für Sans</span><span class="sxs-lookup"><span data-stu-id="486be-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager For SANs</span></span>
</dt> <dd>

<span data-ttu-id="486be-919">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-919">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet-Speicher Namen Server</span><span class="sxs-lookup"><span data-stu-id="486be-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-921">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-921">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipfad-e/a</span><span class="sxs-lookup"><span data-stu-id="486be-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span></span>
</dt> <dd>

<span data-ttu-id="486be-923">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-923">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-925">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-925">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Dienste für Netzwerkdatei System</span><span class="sxs-lookup"><span data-stu-id="486be-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="486be-927">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-927">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution-Protokoll</span><span class="sxs-lookup"><span data-stu-id="486be-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol</span></span>
</dt> <dd>

<span data-ttu-id="486be-929">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-929">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remoteserver-Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="486be-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remote Server Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-931">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-931">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Qualität der Windows-audiovideos</span><span class="sxs-lookup"><span data-stu-id="486be-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience</span></span>
</dt> <dd>

<span data-ttu-id="486be-933">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-933">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Gruppenrichtlinie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="486be-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Group Policy Management</span></span>
</dt> <dd>

<span data-ttu-id="486be-935">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-935">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indizierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-937">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-937">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Datei Server Ressourcen-Manager (File Server, f)</span><span class="sxs-lookup"><span data-stu-id="486be-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File Server Resource Manager (FSRM)</span></span>
</dt> <dd>

<span data-ttu-id="486be-939">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-939">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server-Migrationstools</span><span class="sxs-lookup"><span data-stu-id="486be-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server Migration Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-941">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-941">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span><span class="sxs-lookup"><span data-stu-id="486be-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span></span>
</dt> <dd>

<span data-ttu-id="486be-943">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-943">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="486be-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="486be-945">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-945">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (Bits)</span><span class="sxs-lookup"><span data-stu-id="486be-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="486be-947">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-947">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WOW64-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="486be-949">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-949">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="486be-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Window Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-951">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-951">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP-Adress Verwaltungs Server (IPAM)</span><span class="sxs-lookup"><span data-stu-id="486be-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP Address Management (IPAM) Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-953">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-953">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-955">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-955">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="486be-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5</span></span>
</dt> <dd>

<span data-ttu-id="486be-957">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-957">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows-Suchdienst</span><span class="sxs-lookup"><span data-stu-id="486be-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-959">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-959">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client für NFS</span><span class="sxs-lookup"><span data-stu-id="486be-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client for NFS</span></span>
</dt> <dd>

<span data-ttu-id="486be-961">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-961">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker-Netzwerk Entsperrung</span><span class="sxs-lookup"><span data-stu-id="486be-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker Network Unlock</span></span>
</dt> <dd>

<span data-ttu-id="486be-963">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-963">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>IIS-Erweiterung für Management odata</span><span class="sxs-lookup"><span data-stu-id="486be-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Management OData IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="486be-965">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-965">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4,5 Erweiterte Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-967">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-967">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4,5-Features</span><span class="sxs-lookup"><span data-stu-id="486be-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Features</span></span>
</dt> <dd>

<span data-ttu-id="486be-969">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-969">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Benutzeroberflächen und Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="486be-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="486be-971">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-971">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Tools und Infrastruktur für die grafische Verwaltung</span><span class="sxs-lookup"><span data-stu-id="486be-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Graphical Management Tools and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="486be-973">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-973">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Datei-und Speicherdienste</span><span class="sxs-lookup"><span data-stu-id="486be-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>File and Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-975">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-975">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials-Darstellung</span><span class="sxs-lookup"><span data-stu-id="486be-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience</span></span>
</dt> <dd>

<span data-ttu-id="486be-977">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-977">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direktes abspielen</span><span class="sxs-lookup"><span data-stu-id="486be-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play</span></span>
</dt> <dd>

<span data-ttu-id="486be-979">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-979">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>verteiltes Dateisystem</span><span class="sxs-lookup"><span data-stu-id="486be-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Distributed File System</span></span>
</dt> <dd>

<span data-ttu-id="486be-981">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-981">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Datei Server Ressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="486be-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="486be-983">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-983">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Dienste für Netzwerkdatei System</span><span class="sxs-lookup"><span data-stu-id="486be-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="486be-985">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-985">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Einzelinstanzspeicher</span><span class="sxs-lookup"><span data-stu-id="486be-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Single Instance Storage</span></span>
</dt> <dd>

<span data-ttu-id="486be-987">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-987">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows-Suchdienst</span><span class="sxs-lookup"><span data-stu-id="486be-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-989">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-989">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indizierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-991">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-991">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI-Zielspeicher Anbieter (VDS-und VSS-Hardware Anbieter)</span><span class="sxs-lookup"><span data-stu-id="486be-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>
</dt> <dd>

<span data-ttu-id="486be-993">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-993">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Arbeitsordner</span><span class="sxs-lookup"><span data-stu-id="486be-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="486be-995">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-995">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory-Domäne Controller</span><span class="sxs-lookup"><span data-stu-id="486be-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory Domain Controller</span></span>
</dt> <dd>

<span data-ttu-id="486be-997">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-997">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identitätsverwaltung für UNIX</span><span class="sxs-lookup"><span data-stu-id="486be-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identity Management For Unix</span></span>
</dt> <dd>

<span data-ttu-id="486be-999">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-999">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server für Netzwerk Informationsdienste</span><span class="sxs-lookup"><span data-stu-id="486be-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server For Network Information Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1001">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1001">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Kenn Wort Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="486be-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Password Synchronization</span></span>
</dt> <dd>

<span data-ttu-id="486be-1003">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1003">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1005">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1005">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media-Server</span><span class="sxs-lookup"><span data-stu-id="486be-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-1007">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="486be-1007">No longer supported.</span></span>

</dd> <dt>

<span data-ttu-id="486be-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Webbasierte Verwaltung</span><span class="sxs-lookup"><span data-stu-id="486be-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Web-based Administration</span></span>
</dt> <dd>

<span data-ttu-id="486be-1009">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1009">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Protokollierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="486be-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Logging Agent</span></span>
</dt> <dd>

<span data-ttu-id="486be-1011">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1011">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Verbunddienst</span><span class="sxs-lookup"><span data-stu-id="486be-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Federation Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1013">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1013">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Verbunddienst-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="486be-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Federation Service Policy</span></span>
</dt> <dd>

<span data-ttu-id="486be-1015">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1015">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS von Web-Agents</span><span class="sxs-lookup"><span data-stu-id="486be-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents</span></span>
</dt> <dd>

<span data-ttu-id="486be-1017">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1017">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows-Token-basierter Agent</span><span class="sxs-lookup"><span data-stu-id="486be-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Token-based Agent</span></span>
</dt> <dd>

<span data-ttu-id="486be-1019">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1019">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remotedesktop Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="486be-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remote Desktop Licensing</span></span>
</dt> <dd>

<span data-ttu-id="486be-1021">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1021">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="486be-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Network Policy Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-1023">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1023">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span><span class="sxs-lookup"><span data-stu-id="486be-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span></span>
</dt> <dd>

<span data-ttu-id="486be-1025">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1025">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Zugriffs Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1027">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1027">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span><span class="sxs-lookup"><span data-stu-id="486be-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="486be-1029">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1029">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Integritäts Registrierungsstelle</span><span class="sxs-lookup"><span data-stu-id="486be-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Health Registration Authority</span></span>
</dt> <dd>

<span data-ttu-id="486be-1031">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1031">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization-Protokoll</span><span class="sxs-lookup"><span data-stu-id="486be-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol</span></span>
</dt> <dd>

<span data-ttu-id="486be-1033">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1033">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="486be-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="486be-1035">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1035">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS-Viewer</span><span class="sxs-lookup"><span data-stu-id="486be-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="486be-1037">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1037">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1039">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1039">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="486be-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider</span></span>
</dt> <dd>

<span data-ttu-id="486be-1041">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1041">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="486be-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="486be-1043">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1043">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Webserver (IIS)-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Web Server (IIS) Support</span></span>
</dt> <dd>

<span data-ttu-id="486be-1045">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1045">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Com+-Netzwerk Zugriff</span><span class="sxs-lookup"><span data-stu-id="486be-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="486be-1047">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1047">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP-Port Freigabe</span><span class="sxs-lookup"><span data-stu-id="486be-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="486be-1049">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1049">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Unterstützung für Windows-Prozess Aktivierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Process Activation Service Support</span></span>
</dt> <dd>

<span data-ttu-id="486be-1051">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1051">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="486be-1053">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1053">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Activation</span></span>
</dt> <dd>

<span data-ttu-id="486be-1055">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1055">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="486be-1057">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1057">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes Activation</span></span>
</dt> <dd>

<span data-ttu-id="486be-1059">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1059">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Verteilte Transaktionen</span><span class="sxs-lookup"><span data-stu-id="486be-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Distributed Transactions</span></span>
</dt> <dd>

<span data-ttu-id="486be-1061">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1061">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Eingehende Remote Transaktionen</span><span class="sxs-lookup"><span data-stu-id="486be-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Incoming Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="486be-1063">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1063">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Ausgehende Remote Transaktionen</span><span class="sxs-lookup"><span data-stu-id="486be-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Outgoing Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="486be-1065">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1065">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-automatische Transaktionen</span><span class="sxs-lookup"><span data-stu-id="486be-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-Automatic Transactions</span></span>
</dt> <dd>

<span data-ttu-id="486be-1067">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1067">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Anwendungs Server Erweiterungen für .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="486be-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="486be-1069">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1069">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Rollen Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Role Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1071">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1071">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1073">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1073">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins und Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1075">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1075">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Netzwerk Richtlinien-und Zugriffs Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Network Policy and Access Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1077">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1077">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="486be-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1079">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1079">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remotedesktopdienste Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remote Desktop Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1081">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1081">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Verwaltungs Tools für Funktionen</span><span class="sxs-lookup"><span data-stu-id="486be-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Feature Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1083">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1083">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failoverclustering-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failover Clustering Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1085">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1085">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS-Server Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS Server Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1087">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1087">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Dienste für Network File System-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1089">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1089">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Webserver (IIS)-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web Server (IIS) Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1091">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1091">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server für NIS Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1093">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1093">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins und Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1095">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1095">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS und AD LDS Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1097">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1097">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remotedesktopverbindung Broker-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1099">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1099">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP-Adressverwaltung (IPAM)-Client</span><span class="sxs-lookup"><span data-stu-id="486be-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP Address Management (IPAM) Client</span></span>
</dt> <dd>

<span data-ttu-id="486be-1101">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1101">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V-Modul für Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V Module for Windows PowerShell</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="486be-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span><span class="sxs-lookup"><span data-stu-id="486be-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span></span>
</dt> <dd>

<span data-ttu-id="486be-1104">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1104">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Freigabe-und Speicher Verwaltungs Tool</span><span class="sxs-lookup"><span data-stu-id="486be-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Storage Management Tool</span></span>
</dt> <dd>

<span data-ttu-id="486be-1106">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1106">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Tools für die Remote Zugriffs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="486be-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remote Access Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1108">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1108">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Zugriffs Modul für Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Access module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1110">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1110">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Zugriffs-GUI und-Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Access GUI and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1112">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1112">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1114">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1114">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Diagnose Tools für Remotedesktop Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="486be-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remote Desktop Licensing Diagnoser Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1116">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1116">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1118">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1118">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volumen Aktivierungs Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volume Activation Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1120">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1120">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server-Sicherung</span><span class="sxs-lookup"><span data-stu-id="486be-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span></span>
</dt> <dd>

<span data-ttu-id="486be-1122">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1122">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Befehlszeilen Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Command Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1124">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1124">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Freihand Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Ink Support</span></span>
</dt> <dd>

<span data-ttu-id="486be-1126">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1126">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handschrifterkennung</span><span class="sxs-lookup"><span data-stu-id="486be-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handwriting Recognition</span></span>
</dt> <dd>

<span data-ttu-id="486be-1128">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1128">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span><span class="sxs-lookup"><span data-stu-id="486be-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-1130">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1130">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WOW64</span><span class="sxs-lookup"><span data-stu-id="486be-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="486be-1132">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1132">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WOW64 für .NET Framework 2,0 und PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 for .NET Framework 2.0 and PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1134">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1134">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WOW64 für .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="486be-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="486be-1136">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1136">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WOW64 für PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1138">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1138">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WOW64 für .NET Framework 3,0 und 3,5</span><span class="sxs-lookup"><span data-stu-id="486be-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="486be-1140">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1140">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WOW64 für Druckdienste</span><span class="sxs-lookup"><span data-stu-id="486be-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1142">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1142">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WOW64 für Failoverclustering</span><span class="sxs-lookup"><span data-stu-id="486be-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="486be-1144">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1144">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WOW64 für Eingabemethoden-Editor</span><span class="sxs-lookup"><span data-stu-id="486be-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="486be-1146">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1146">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WOW64 für Subsystem für UNIX-basierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="486be-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="486be-1148">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1148">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Darstellung</span><span class="sxs-lookup"><span data-stu-id="486be-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Experience</span></span>
</dt> <dd>

<span data-ttu-id="486be-1150">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1150">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Grafische Shell für Server</span><span class="sxs-lookup"><span data-stu-id="486be-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Server Graphical Shell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1152">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1152">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API-und PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="486be-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API and PowerShell cmdlets</span></span>
</dt> <dd>

<span data-ttu-id="486be-1154">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1154">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Konnektivität</span><span class="sxs-lookup"><span data-stu-id="486be-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="486be-1156">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1156">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1158">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1158">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Verwaltungskonsole für die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="486be-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>User Interface Management Console</span></span>
</dt> <dd>

<span data-ttu-id="486be-1160">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1160">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="486be-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="486be-1162">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1162">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2,0-Engine</span><span class="sxs-lookup"><span data-stu-id="486be-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 Engine</span></span>
</dt> <dd>

<span data-ttu-id="486be-1164">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1164">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="486be-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0</span></span>
</dt> <dd>

<span data-ttu-id="486be-1166">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1166">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell-Webzugriff</span><span class="sxs-lookup"><span data-stu-id="486be-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span></span>
</dt> <dd>

<span data-ttu-id="486be-1168">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1168">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell-Dienst zum Konfigurieren des gewünschten Zustands</span><span class="sxs-lookup"><span data-stu-id="486be-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1170">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1170">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4,5 erweitert</span><span class="sxs-lookup"><span data-stu-id="486be-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended</span></span>
</dt> <dd>

<span data-ttu-id="486be-1172">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1172">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1174">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1174">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="486be-1176">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1176">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing Aktivierung (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="486be-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing (MSMQ) Activation</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="486be-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe Activation</span></span>
</dt> <dd>

<span data-ttu-id="486be-1179">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1179">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="486be-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="486be-1181">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1181">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP-Port Freigabe</span><span class="sxs-lookup"><span data-stu-id="486be-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="486be-1183">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1183">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="486be-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5</span></span>
</dt> <dd>

<span data-ttu-id="486be-1185">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1185">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET-Erweiterbarkeit 4,5</span><span class="sxs-lookup"><span data-stu-id="486be-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET Extensibility 4.5</span></span>
</dt> <dd>

<span data-ttu-id="486be-1187">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1187">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess und VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="486be-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess and VPN (RAS)</span></span>
</dt> <dd>

<span data-ttu-id="486be-1189">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1189">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span><span class="sxs-lookup"><span data-stu-id="486be-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="486be-1191">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1191">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Speicherdienste</span><span class="sxs-lookup"><span data-stu-id="486be-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1193">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1193">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Verwaltungs Tools für Failovercluster</span><span class="sxs-lookup"><span data-stu-id="486be-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failover Cluster Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1195">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1195">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1197">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1197">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Anwendungs Initialisierung</span><span class="sxs-lookup"><span data-stu-id="486be-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Application Initialization</span></span>
</dt> <dd>

<span data-ttu-id="486be-1199">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1199">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Zentralisierte SSL-Zertifikat Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Centralized SSL Certificate Support</span></span>
</dt> <dd>

<span data-ttu-id="486be-1201">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1201">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Ansprüche-fähiger Agent</span><span class="sxs-lookup"><span data-stu-id="486be-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Claims-aware Agent</span></span>
</dt> <dd>

<span data-ttu-id="486be-1203">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1203">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remotedesktop-Sitzungshost Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remote Desktop Session Host Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1205">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1205">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket-Protokoll</span><span class="sxs-lookup"><span data-stu-id="486be-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket Protocol</span></span>
</dt> <dd>

<span data-ttu-id="486be-1207">nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1207">no longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Com+-Netzwerk Zugriff</span><span class="sxs-lookup"><span data-stu-id="486be-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="486be-1209">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1209">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Namensänderung für Datei-und iSCSI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>File and iSCSI Services name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1211">Geändert in "Dateidienste"</span><span class="sxs-lookup"><span data-stu-id="486be-1211">Changed to File Services</span></span>

</dd> </dl>

### <a name="windows-server-2012"></a><span data-ttu-id="486be-1212">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="486be-1212">Windows Server 2012</span></span>

<dl> <dt>

<span data-ttu-id="486be-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Benutzeroberflächen und Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="486be-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="486be-1214">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1214">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server für NFS</span><span class="sxs-lookup"><span data-stu-id="486be-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span></span>
</dt> <dd>

<span data-ttu-id="486be-1216">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1216">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Datei Server-VSS-Agent-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>File Server VSS Agent Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1218">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1218">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI-Ziel Server</span><span class="sxs-lookup"><span data-stu-id="486be-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI Target Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-1220">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1220">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Datendeduplizierung</span><span class="sxs-lookup"><span data-stu-id="486be-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Data Deduplication</span></span>
</dt> <dd>

<span data-ttu-id="486be-1222">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1222">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Arbeitsordner</span><span class="sxs-lookup"><span data-stu-id="486be-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="486be-1224">Entfernt</span><span class="sxs-lookup"><span data-stu-id="486be-1224">Removed</span></span>

</dd> <dt>

<span data-ttu-id="486be-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Kerndienste</span><span class="sxs-lookup"><span data-stu-id="486be-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Core Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1226">Nur für diese Version hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="486be-1226">Added for this version only.</span></span>

</dd> <dt>

<span data-ttu-id="486be-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remotedesktop von virtuellen Grafiken</span><span class="sxs-lookup"><span data-stu-id="486be-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remote Desktop Virtual Graphics</span></span>
</dt> <dd>

<span data-ttu-id="486be-1228">Nur für diese Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1228">Added for this version only</span></span>

</dd> <dt>

<span data-ttu-id="486be-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Zugriff</span><span class="sxs-lookup"><span data-stu-id="486be-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Access</span></span>
</dt> <dd>

<span data-ttu-id="486be-1230">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1230">Added</span></span>

</dd> </dl>

### <a name="windows-server-2008-r2"></a><span data-ttu-id="486be-1231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="486be-1231">Windows Server 2008 R2</span></span>

<dl> <dt>

<span data-ttu-id="486be-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1233">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1233">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows-System Ressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="486be-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="486be-1235">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1235">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Wechsel Speicher-Manager</span><span class="sxs-lookup"><span data-stu-id="486be-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Removable Storage Manager</span></span>
</dt> <dd>

<span data-ttu-id="486be-1237">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1237">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1239">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1239">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Freihand- und Handschriftdienste</span><span class="sxs-lookup"><span data-stu-id="486be-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Ink and Handwriting Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1241">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1241">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM-IIS-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="486be-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="486be-1243">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1243">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="486be-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="486be-1245">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1245">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (Bits)</span><span class="sxs-lookup"><span data-stu-id="486be-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="486be-1247">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1247">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS-Viewer</span><span class="sxs-lookup"><span data-stu-id="486be-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="486be-1249">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1249">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows-Biometrieframework</span><span class="sxs-lookup"><span data-stu-id="486be-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span></span>
</dt> <dd>

<span data-ttu-id="486be-1251">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1251">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WOW64-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="486be-1253">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1253">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span><span class="sxs-lookup"><span data-stu-id="486be-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span></span>
</dt> <dd>

<span data-ttu-id="486be-1255">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1255">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Datei Replikations Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>File Replication Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1257">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1257">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache für Netzwerkdateien</span><span class="sxs-lookup"><span data-stu-id="486be-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache for Network Files</span></span>
</dt> <dd>

<span data-ttu-id="486be-1259">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1259">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Arbeitsordner</span><span class="sxs-lookup"><span data-stu-id="486be-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="486be-1261">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1261">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Server für verteilte Scanvorgänge</span><span class="sxs-lookup"><span data-stu-id="486be-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Distributed Scan Server</span></span>
</dt> <dd>

<span data-ttu-id="486be-1263">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1263">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP-Publishing Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP Publishing Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1265">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1265">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="486be-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP Management Console</span></span>
</dt> <dd>

<span data-ttu-id="486be-1267">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1267">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP-Dienst</span><span class="sxs-lookup"><span data-stu-id="486be-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1269">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1269">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="486be-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP Extensibility</span></span>
</dt> <dd>

<span data-ttu-id="486be-1271">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1271">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS-Hostfähiger Webkern</span><span class="sxs-lookup"><span data-stu-id="486be-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS Hostable Web Core</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="486be-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000-Client Unterstützung</span><span class="sxs-lookup"><span data-stu-id="486be-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support</span></span>
</dt> <dd>

<span data-ttu-id="486be-1274">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1274">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Zertifikatregistrierungs-Webdienst</span><span class="sxs-lookup"><span data-stu-id="486be-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Certificate Enrollment Web Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1276">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1276">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Zertifikatregistrierungsrichtlinien-Webdienst</span><span class="sxs-lookup"><span data-stu-id="486be-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Certificate Enrollment Policy Web Service</span></span>
</dt> <dd>

<span data-ttu-id="486be-1278">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1278">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Webanwendung der UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services Web Application</span></span>
</dt> <dd>

<span data-ttu-id="486be-1280">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1280">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Datenbank der UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services Database</span></span>
</dt> <dd>

<span data-ttu-id="486be-1282">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1282">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Anwendungs Server Erweiterungen für .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="486be-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="486be-1284">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1284">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Tools für UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="486be-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1286">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1286">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker-Laufwerkverschlüsselung Verwaltungs Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="486be-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker Drive Encryption Administration Utilities</span></span>
</dt> <dd>

<span data-ttu-id="486be-1288">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1288">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS und AD LDS Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1290">Nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1290">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="486be-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS und AD LDS Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1292">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1292">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory-Verwaltungscenter</span><span class="sxs-lookup"><span data-stu-id="486be-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory Administrative Center</span></span>
</dt> <dd>

<span data-ttu-id="486be-1294">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1294">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory-Modul für Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1296">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1296">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remotedesktopverbindung Broker-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="486be-1298">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1298">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WOW64</span><span class="sxs-lookup"><span data-stu-id="486be-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="486be-1300">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1300">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WOW64 für .NET Framework 2,0 und Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1302">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1302">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WOW64 für .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="486be-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="486be-1304">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1304">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WOW64 für PowerShell</span><span class="sxs-lookup"><span data-stu-id="486be-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="486be-1306">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1306">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WOW64 für .NET Framework 3,0 und 3,5</span><span class="sxs-lookup"><span data-stu-id="486be-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="486be-1308">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1308">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WOW64 für Druckdienste</span><span class="sxs-lookup"><span data-stu-id="486be-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="486be-1310">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1310">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WOW64 für Failoverclustering</span><span class="sxs-lookup"><span data-stu-id="486be-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="486be-1312">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1312">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WOW64 für Eingabemethoden-Editor</span><span class="sxs-lookup"><span data-stu-id="486be-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="486be-1314">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1314">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WOW64 für Subsystem für UNIX-basierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="486be-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="486be-1316">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1316">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker-Wiederherstellungs Kenn Wort Anzeige</span><span class="sxs-lookup"><span data-stu-id="486be-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker Recovery Password Viewer</span></span>
</dt> <dd>

<span data-ttu-id="486be-1318">hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="486be-1318">Added</span></span>

</dd> <dt>

<span data-ttu-id="486be-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Druck-und Dokumentdienste Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Print and Document Services name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1320">benannte Druckdienste für diese Version</span><span class="sxs-lookup"><span data-stu-id="486be-1320">named Print Services for this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remotedesktopdienste Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remote Desktop Services name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1322">benannte terminaldienstedienste in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1322">named Terminal Services in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>Namensänderung für .NET Framework 3.5.1 Features</span><span class="sxs-lookup"><span data-stu-id="486be-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Features name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1324">Benannte .NET Framework 3,0-Features in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1324">Named .NET Framework 3.0 Features in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remotedesktop-Sitzungshost Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remote Desktop Session Host name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1326">Benannte Terminal Server in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1326">Named Terminal Server in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Namensänderung für Remotedesktop Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="486be-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remote Desktop Licensing name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1328">Benannte Terminaldienstelizenzierung in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1328">Named TS Licensing in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Änderung des Remotedesktop Gateway-namens</span><span class="sxs-lookup"><span data-stu-id="486be-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remote Desktop Gateway name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1330">Benanntes Terminaldienstegateway in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1330">Named TS Gateway in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remotedesktopverbindung Broker-Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remote Desktop Connection Broker name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1332">Benannte TS-Sitzungs Broker in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1332">Named TS Session Broker in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remotedesktop Webzugriff Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remote Desktop Web Access name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1334">Benannte TS-Webzugriff in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1334">Named TS Web Access in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 Namensänderung</span><span class="sxs-lookup"><span data-stu-id="486be-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1336">(220) benannte net FX 3,0-Funktionen in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1336">(220) Named Net FX 3.0 Features in this release</span></span>

<span data-ttu-id="486be-1337">(230) namens Anwendungs Server Core in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1337">(230) Named Application Server Core in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Namensänderung für AD DS Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1339">Benannte Active Directory Domain Services Tools in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1339">Named Active Directory Domain Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Namensänderung für AD LDS Snap-Ins und Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1341">Benannte Active Directory Lightweight Directory Services Tools in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1341">Named Active Directory Lightweight Directory Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Namensänderung für Druck-und Dokumentdienste Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Print and Document Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1343">Benannte Druckdienst Tools in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1343">Named Print Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Namensänderung für Remotedesktopdienste Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remote Desktop Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1345">Benannte Terminaldienstetools in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1345">Named Terminal Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Namensänderung für Remotedesktop-Sitzungshost Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remote Desktop Session Host Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1347">Benannte Terminal Server Tools in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1347">Named Terminal Server Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Namensänderung für Remotedesktop Gateway-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remote Desktop Gateway Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1349">Benannte Terminaldienstegateway-Tools in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1349">Named TS Gateway Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Namensänderung für Remotedesktop Lizenzierungs Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remote Desktop Licensing Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1351">Benannte Terminaldienstelizenzierungs-Tools in dieser Version</span><span class="sxs-lookup"><span data-stu-id="486be-1351">Named TS Licensing Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="486be-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Namensänderung für AD DS Snap-Ins und Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="486be-1353">Active Directory-Domänencontroller-Tools</span><span class="sxs-lookup"><span data-stu-id="486be-1353">Active Directory Domain Controller Tools</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="486be-1354">Beispiele</span><span class="sxs-lookup"><span data-stu-id="486be-1354">Examples</span></span>

<span data-ttu-id="486be-1355">Das folgende Skript zeigt die Namen aller Serverfunktionen auf dem Computer mit dem Namen Fabrikam an.</span><span class="sxs-lookup"><span data-stu-id="486be-1355">The following script displays the names of all the server features on the computer named "FABRIKAM".</span></span> <span data-ttu-id="486be-1356">Beachten Sie, dass auf dem Bereitstellungs Zielcomputer Windows Server 2008 oder ein späteres Server Betriebssystem ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="486be-1356">Note that the target computer must be running Windows Server 2008 or a later server operating system.</span></span>


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a><span data-ttu-id="486be-1357">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="486be-1357">Requirements</span></span>



| <span data-ttu-id="486be-1358">Anforderung</span><span class="sxs-lookup"><span data-stu-id="486be-1358">Requirement</span></span> | <span data-ttu-id="486be-1359">Wert</span><span class="sxs-lookup"><span data-stu-id="486be-1359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="486be-1360">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="486be-1360">Minimum supported client</span></span><br/> | <span data-ttu-id="486be-1361">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="486be-1361">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="486be-1362">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="486be-1362">Minimum supported server</span></span><br/> | <span data-ttu-id="486be-1363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="486be-1363">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="486be-1364">Namespace</span><span class="sxs-lookup"><span data-stu-id="486be-1364">Namespace</span></span><br/>                | <span data-ttu-id="486be-1365">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="486be-1365">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="486be-1366">MOF</span><span class="sxs-lookup"><span data-stu-id="486be-1366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="486be-1367"><dt>Servercompprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="486be-1367"><dt>ServerCompProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="486be-1368">DLL</span><span class="sxs-lookup"><span data-stu-id="486be-1368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="486be-1369"><dt>ServerCompProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="486be-1369"><dt>ServerCompProv.dll</dt></span></span> </dl> |



 

