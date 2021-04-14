---
description: Die EnableWINS-&\# 32; Die statische WMI-Klassenmethode aktiviert Windows Internet Naming Service (WINS)-Einstellungen für TCP/IP, aber unabhängig vom Netzwerkadapter.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: EnableWINS-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523387"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="c6c2c-103">EnableWINS-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6c2c-103">EnableWINS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="c6c2c-104">Mit der statischen Methode " **EnableWINS** " der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) können Windows Internet Naming Service (WINS)-Einstellungen speziell für TCP/IP, aber unabhängig vom Netzwerkadapter aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-104">The **EnableWINS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables Windows Internet Naming Service (WINS) settings specific to TCP/IP, but independent of the network adapter.</span></span>

<span data-ttu-id="c6c2c-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c6c2c-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c2c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6c2c-107">Syntax</span></span>


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a><span data-ttu-id="c6c2c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6c2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c2c-109">*DNSEnabledForWINSResolution* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6c2c-109">*DNSEnabledForWINSResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6c2c-110">**True** gibt an, dass die Domain Name System (DNS) für die Namensauflösung über die WINS-Auflösung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-110">If **true**, the Domain Name System (DNS) is enabled for name resolution over WINS resolution.</span></span>

</dd> <dt>

<span data-ttu-id="c6c2c-111">*WINSEnableLMHostsLookup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6c2c-111">*WINSEnableLMHostsLookup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6c2c-112">**True** gibt an, dass lokale Suchdateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-112">If **true**, local lookup files are used.</span></span> <span data-ttu-id="c6c2c-113">Suchdateien enthalten Zuordnungen von IP-Adressen zu Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-113">Lookup files will contain mappings of IP addresses to host names.</span></span>

</dd> <dt>

<span data-ttu-id="c6c2c-114">*WINSHostLookupFile* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c6c2c-114">*WINSHostLookupFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6c2c-115">Suchdateien, die Zuordnungen von IP-Adressen zu Hostnamen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-115">Lookup files that contain mappings of IP addresses to host names.</span></span> <span data-ttu-id="c6c2c-116">Wenn Sie verfügbar sind, befinden sich die Dateien unter% systemroot% \\ system32 \\ Drivers \\ .</span><span class="sxs-lookup"><span data-stu-id="c6c2c-116">If available, the files will be found in %SystemRoot%\\system32\\drivers\\ .</span></span>

</dd> <dt>

<span data-ttu-id="c6c2c-117">*WINSScopeID* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c6c2c-117">*WINSScopeID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6c2c-118">Der Wert des Bereichs Bezeichners, der am Ende des NetBIOS-Namens des Computers angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-118">Scope identifier value that will be appended to the end of the computer's NetBIOS name.</span></span> <span data-ttu-id="c6c2c-119">Systeme, die denselben Bereichs Bezeichner verwenden, können mit diesem Computer kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-119">Systems that use the same scope identifier can communicate with this computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c2c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6c2c-120">Return value</span></span>

<span data-ttu-id="c6c2c-121">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist. 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist. eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-121">Returns a value of 0 (zero) for a successful completion when no reboot is required; 1 (one) for a successful completion when a reboot is required; a different number if there is an error.</span></span> <span data-ttu-id="c6c2c-122">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-122">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c6c2c-123">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c6c2c-124">**Erfolgreicher Abschluss, kein Neustart erforderlich** (0)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-124">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-125">**Erfolgreicher Abschluss, Neustart erforderlich** (1)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-125">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-126">**Methode wird auf dieser Plattform nicht unterstützt** (64).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-126">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-127">**Unbekannter Fehler** (65).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-127">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-128">**Ungültige Subnetzmaske** (66).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-128">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-129">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde** (67).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-129">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-130">**Ungültiger Eingabeparameter** (68)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-130">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-131">**Es wurden mehr als 5 Gateways angegeben** (69).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-131">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-132">**Ungültige IP-Adresse** (70)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-132">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-133">**Ungültige Gateway-IP-Adresse** (71)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-133">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-134">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen** (72).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-134">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-135">**Ungültiger Domänen Name** (73).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-135">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-136">**Ungültiger Hostname** (74).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-136">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-137">**Kein primärer/sekundärer WINS-Server definiert** (75)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-137">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-138">**Ungültige Datei** (76)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-138">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-139">**Ungültiger Systempfad** (77).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-139">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-140">Fehler beim **Kopieren der Datei** (78).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-140">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-141">**Ungültiger Sicherheitsparameter** (79).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-141">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-142">Der **TCP/IP-Dienst kann nicht konfiguriert** werden (80).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-142">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-143">**DHCP-Dienst kann nicht konfiguriert** werden (81).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-143">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-144">**DHCP-Lease kann nicht erneuert** werden (82).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-144">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-145">**DHCP-Lease kann nicht frei** gegeben werden (83).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-145">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-146">Die **IP ist auf dem Adapter nicht aktiviert** (84).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-146">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-147">**IPX ist auf dem Adapter nicht aktiviert** (85).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-147">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-148">**Fehler bei Frame/Netzwerk Nummer** (86)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-148">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-149">**Ungültiger Frame-Typ** (87).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-149">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-150">**Ungültige Netzwerk Nummer** (88).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-150">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-151">**Doppelte Netzwerk Nummer** (89)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-151">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-152">**Parameter außerhalb des** gültigen Bereichs (90)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-152">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-153">**Zugriff verweigert** (91)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-153">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-154">**Nicht** genügend Arbeitsspeicher (92)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-154">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-155">**Bereits vorhanden** (93)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-155">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-156">Der **Pfad, die Datei oder das Objekt wurde nicht gefunden** (94).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-156">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-157">Der **Dienst kann nicht benachrichtigt** werden (95).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-157">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-158">Der **DNS-Dienst kann nicht benachrichtigt** werden (96).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-158">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-159">**Schnittstelle nicht konfigurierbar** (97)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-159">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-160">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden** (98).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-160">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-161">**DHCP ist auf dem Adapter nicht aktiviert** (100).</span><span class="sxs-lookup"><span data-stu-id="c6c2c-161">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="c6c2c-162">**Sonstige** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-162">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="c6c2c-163">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6c2c-163">Examples</span></span>

<span data-ttu-id="c6c2c-164">Das Codebeispiel [Aktivieren von WINS für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript in der TechNet Gallery verwendet **EnableWINS** , um WINS auf allen Netzwerkadaptern zu aktivieren, die auf einem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="c6c2c-164">The [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript code sample, on TechNet Gallery, uses **EnableWINS** to Enables WINS on all the network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c2c-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6c2c-165">Requirements</span></span>



| <span data-ttu-id="c6c2c-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6c2c-166">Requirement</span></span> | <span data-ttu-id="c6c2c-167">Wert</span><span class="sxs-lookup"><span data-stu-id="c6c2c-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c2c-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c2c-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6c2c-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6c2c-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6c2c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c2c-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6c2c-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6c2c-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6c2c-172">Namespace</span></span><br/>                | <span data-ttu-id="c6c2c-173">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c6c2c-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6c2c-174">MOF</span><span class="sxs-lookup"><span data-stu-id="c6c2c-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6c2c-175"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c6c2c-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6c2c-176">DLL</span><span class="sxs-lookup"><span data-stu-id="c6c2c-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6c2c-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6c2c-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c2c-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6c2c-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c2c-179">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="c6c2c-179">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c6c2c-180">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="c6c2c-180">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="c6c2c-181">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c6c2c-181">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="c6c2c-182">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="c6c2c-182">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="c6c2c-183">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="c6c2c-183">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

