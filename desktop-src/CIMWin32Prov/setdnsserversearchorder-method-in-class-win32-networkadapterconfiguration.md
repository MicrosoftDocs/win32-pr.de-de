---
description: SetDNSServerSearchOrder &\# 32; Die WMI-Klassenmethode verwendet ein Array von Zeichen folgen Elementen, um die Server Such Reihenfolge festzulegen.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: SetDNSServerSearchOrder-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041472"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="44aa6-103">SetDNSServerSearchOrder-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="44aa6-103">SetDNSServerSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="44aa6-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetDNSServerSearchOrder** verwendet ein Array von Zeichen folgen Elementen, um die Server Such Reihenfolge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44aa6-104">The **SetDNSServerSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses an array of string elements to set the server search order.</span></span>

<span data-ttu-id="44aa6-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="44aa6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="44aa6-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="44aa6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="44aa6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="44aa6-107">Syntax</span></span>


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="44aa6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="44aa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44aa6-109">*DNSServerSearchOrder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44aa6-109">*DNSServerSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44aa6-110">Liste der Server-IP-Adressen für die Abfrage von DNS-Servern.</span><span class="sxs-lookup"><span data-stu-id="44aa6-110">List of server IP addresses to query for DNS servers.</span></span>

<span data-ttu-id="44aa6-111">Beispiel: 130.215.24.1 oder 157.54.164.1</span><span class="sxs-lookup"><span data-stu-id="44aa6-111">Example: 130.215.24.1 or 157.54.164.1</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44aa6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44aa6-112">Return value</span></span>

<span data-ttu-id="44aa6-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="44aa6-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="44aa6-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="44aa6-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="44aa6-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="44aa6-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="44aa6-116">**Erfolgreicher Abschluss, kein Neustart erforderlich** (0)</span><span class="sxs-lookup"><span data-stu-id="44aa6-116">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-117">**Erfolgreicher Abschluss, Neustart erforderlich** (1)</span><span class="sxs-lookup"><span data-stu-id="44aa6-117">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-118">**Methode wird auf dieser Plattform nicht unterstützt** (64).</span><span class="sxs-lookup"><span data-stu-id="44aa6-118">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-119">**Unbekannter Fehler** (65).</span><span class="sxs-lookup"><span data-stu-id="44aa6-119">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-120">**Ungültige Subnetzmaske** (66).</span><span class="sxs-lookup"><span data-stu-id="44aa6-120">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-121">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde** (67).</span><span class="sxs-lookup"><span data-stu-id="44aa6-121">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-122">**Ungültiger Eingabeparameter** (68)</span><span class="sxs-lookup"><span data-stu-id="44aa6-122">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-123">**Es wurden mehr als 5 Gateways angegeben** (69).</span><span class="sxs-lookup"><span data-stu-id="44aa6-123">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-124">**Ungültige IP-Adresse** (70)</span><span class="sxs-lookup"><span data-stu-id="44aa6-124">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-125">**Ungültige Gateway-IP-Adresse** (71)</span><span class="sxs-lookup"><span data-stu-id="44aa6-125">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-126">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen** (72).</span><span class="sxs-lookup"><span data-stu-id="44aa6-126">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-127">**Ungültiger Domänen Name** (73).</span><span class="sxs-lookup"><span data-stu-id="44aa6-127">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-128">**Ungültiger Hostname** (74).</span><span class="sxs-lookup"><span data-stu-id="44aa6-128">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-129">**Kein primärer/sekundärer WINS-Server definiert** (75)</span><span class="sxs-lookup"><span data-stu-id="44aa6-129">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-130">**Ungültige Datei** (76)</span><span class="sxs-lookup"><span data-stu-id="44aa6-130">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-131">**Ungültiger Systempfad** (77).</span><span class="sxs-lookup"><span data-stu-id="44aa6-131">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-132">Fehler beim **Kopieren der Datei** (78).</span><span class="sxs-lookup"><span data-stu-id="44aa6-132">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-133">**Ungültiger Sicherheitsparameter** (79).</span><span class="sxs-lookup"><span data-stu-id="44aa6-133">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-134">Der **TCP/IP-Dienst kann nicht konfiguriert** werden (80).</span><span class="sxs-lookup"><span data-stu-id="44aa6-134">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-135">**DHCP-Dienst kann nicht konfiguriert** werden (81).</span><span class="sxs-lookup"><span data-stu-id="44aa6-135">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-136">**DHCP-Lease kann nicht erneuert** werden (82).</span><span class="sxs-lookup"><span data-stu-id="44aa6-136">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-137">**DHCP-Lease kann nicht frei** gegeben werden (83).</span><span class="sxs-lookup"><span data-stu-id="44aa6-137">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-138">Die **IP ist auf dem Adapter nicht aktiviert** (84).</span><span class="sxs-lookup"><span data-stu-id="44aa6-138">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-139">**IPX ist auf dem Adapter nicht aktiviert** (85).</span><span class="sxs-lookup"><span data-stu-id="44aa6-139">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-140">**Fehler bei Frame/Netzwerk Nummer** (86)</span><span class="sxs-lookup"><span data-stu-id="44aa6-140">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-141">**Ungültiger Frame-Typ** (87).</span><span class="sxs-lookup"><span data-stu-id="44aa6-141">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-142">**Ungültige Netzwerk Nummer** (88).</span><span class="sxs-lookup"><span data-stu-id="44aa6-142">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-143">**Doppelte Netzwerk Nummer** (89)</span><span class="sxs-lookup"><span data-stu-id="44aa6-143">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-144">**Parameter außerhalb des** gültigen Bereichs (90)</span><span class="sxs-lookup"><span data-stu-id="44aa6-144">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-145">**Zugriff verweigert** (91)</span><span class="sxs-lookup"><span data-stu-id="44aa6-145">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-146">**Nicht** genügend Arbeitsspeicher (92)</span><span class="sxs-lookup"><span data-stu-id="44aa6-146">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-147">**Bereits vorhanden** (93)</span><span class="sxs-lookup"><span data-stu-id="44aa6-147">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-148">Der **Pfad, die Datei oder das Objekt wurde nicht gefunden** (94).</span><span class="sxs-lookup"><span data-stu-id="44aa6-148">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-149">Der **Dienst kann nicht benachrichtigt** werden (95).</span><span class="sxs-lookup"><span data-stu-id="44aa6-149">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-150">Der **DNS-Dienst kann nicht benachrichtigt** werden (96).</span><span class="sxs-lookup"><span data-stu-id="44aa6-150">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-151">**Schnittstelle nicht konfigurierbar** (97)</span><span class="sxs-lookup"><span data-stu-id="44aa6-151">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-152">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden** (98).</span><span class="sxs-lookup"><span data-stu-id="44aa6-152">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-153">**DHCP ist auf dem Adapter nicht aktiviert** (100).</span><span class="sxs-lookup"><span data-stu-id="44aa6-153">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="44aa6-154">**Sonstige** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="44aa6-154">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="44aa6-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44aa6-155">Remarks</span></span>

<span data-ttu-id="44aa6-156">Dabei handelt es sich um einen instanzabhängigen Methoden Aufrufwert, der pro Adapter angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="44aa6-156">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="44aa6-157">Nachdem statische DNS-Server angegeben wurden, um mit der Verwendung des Dynamic Host Configuration-Protokolls (DHCP) anstelle statischer DNS-Server zu beginnen, können Sie die Methode ohne Angabe von "in"-Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="44aa6-157">After static DNS servers are specified to start using Dynamic Host Configuration Protocol (DHCP) instead of static DNS servers, you can call the method without supplying "in" parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="44aa6-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44aa6-158">Examples</span></span>

<span data-ttu-id="44aa6-159">Die [Such Reihenfolge der DNS-Server Suche für mehrere Computer in einer Organisationseinheit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) "VBScript" in der TechNet Gallery Ruft die DNS-Server Such Reihenfolge für mehrere Computer ab, die einer Organisationseinheit angehören, oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="44aa6-159">The [Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript sample on TechNet Gallery retrieves or sets DNS Server search order for multiple computers that belongs to one organizational unit.</span></span>

<span data-ttu-id="44aa6-160">Das Beispiel [Ändern der DNS-Server-Such Reihenfolge für ein Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript konfiguriert einen TCP/IP-gebundenen Netzwerkadapter für die Verwendung von zwei DNS-Servern.</span><span class="sxs-lookup"><span data-stu-id="44aa6-160">The [Modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript sample configures a TCP/IP-bound network adapter to use two DNS servers.</span></span>

## <a name="requirements"></a><span data-ttu-id="44aa6-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44aa6-161">Requirements</span></span>



| <span data-ttu-id="44aa6-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44aa6-162">Requirement</span></span> | <span data-ttu-id="44aa6-163">Wert</span><span class="sxs-lookup"><span data-stu-id="44aa6-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44aa6-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44aa6-164">Minimum supported client</span></span><br/> | <span data-ttu-id="44aa6-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44aa6-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44aa6-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44aa6-166">Minimum supported server</span></span><br/> | <span data-ttu-id="44aa6-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44aa6-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44aa6-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="44aa6-168">Namespace</span></span><br/>                | <span data-ttu-id="44aa6-169">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="44aa6-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44aa6-170">MOF</span><span class="sxs-lookup"><span data-stu-id="44aa6-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44aa6-171"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="44aa6-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44aa6-172">DLL</span><span class="sxs-lookup"><span data-stu-id="44aa6-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44aa6-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44aa6-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44aa6-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44aa6-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44aa6-175">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="44aa6-175">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="44aa6-176">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="44aa6-176">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="44aa6-177">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="44aa6-177">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="44aa6-178">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="44aa6-178">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="44aa6-179">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="44aa6-179">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

