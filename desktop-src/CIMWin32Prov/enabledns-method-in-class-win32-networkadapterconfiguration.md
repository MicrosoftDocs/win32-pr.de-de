---
description: Die statische Methode der EnableDNS-WMI-Klasse aktiviert den Domain Name System (DNS) für den Dienst.
ms.assetid: 083dccb1-eb38-4ae5-a252-0001759c0f50
ms.tgt_platform: multiple
title: EnableDNS-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDNS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc217211455d8804de47b2b3ffc761d4328fa49a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126518"
---
# <a name="enabledns-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8639d-103">EnableDNS-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="8639d-103">EnableDNS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8639d-104">Die statische Methode der **EnableDNS** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) aktiviert den Domain Name System (DNS) für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="8639d-104">The **EnableDNS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables the Domain Name System (DNS) for service.</span></span>

<span data-ttu-id="8639d-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8639d-105">This topic uses the Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8639d-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8639d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8639d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8639d-107">Syntax</span></span>


```mof
uint32 EnableDNS(
  [in, optional] string DNSHostName,
  [in, optional] string DNSDomain,
  [in, optional] string DNSServerSearchOrder[],
  [in, optional] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="8639d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8639d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8639d-109">*DNSHostName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8639d-109">*DNSHostName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8639d-110">Der Name des DNS-Hosts, der von dieser Methode aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="8639d-110">Name of the DNS host that this method enables.</span></span>

<span data-ttu-id="8639d-111">Beispiel: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="8639d-111">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="8639d-112">*DNSDomain* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8639d-112">*DNSDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8639d-113">Stellt einen Organisationsnamen gefolgt von einem Zeitraum und einer Erweiterung dar, die den Typ der Organisation angibt.</span><span class="sxs-lookup"><span data-stu-id="8639d-113">Represents an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="8639d-114">Beispiel: "Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="8639d-114">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="8639d-115">*DNSServerSearchOrder* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8639d-115">*DNSServerSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8639d-116">Liste der Server-IP-Adressen für die Abfrage von DNS-Servern.</span><span class="sxs-lookup"><span data-stu-id="8639d-116">List of server IP addresses to query for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-117">*DNSDomainSuffixSearchOrder* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8639d-117">*DNSDomainSuffixSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8639d-118">DNS-Domänen Suffix, das während der Namensauflösung an einen Hostnamen angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="8639d-118">DNS domain suffix that is appended to a host name during name resolution.</span></span> <span data-ttu-id="8639d-119">Beim Auflösen eines voll qualifizierten Domänen Namens (Fully Qualified Domain Name, FQDN) aus einem reinen Host Namen fügt das System den lokalen Domänen Namen an.</span><span class="sxs-lookup"><span data-stu-id="8639d-119">When resolving a fully qualified domain name (FQDN) from a host-only name, the system appends the local domain name.</span></span> <span data-ttu-id="8639d-120">Wenn die Namensauflösung nicht erfolgreich ist, verwendet das System die Liste der Domänen Suffixe, um zusätzliche FQDNs in der aufgeführten Reihenfolge zu erstellen, und fragt dann die DNS-Server für jede einzelne ab.</span><span class="sxs-lookup"><span data-stu-id="8639d-120">If the name resolution is not successful, the system uses the domain suffix list to create additional FQDNs in the order listed, and then queries DNS servers for each one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8639d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8639d-121">Return value</span></span>

<span data-ttu-id="8639d-122">Gibt einen Wert von 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und jede andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="8639d-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="8639d-123">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8639d-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8639d-124">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8639d-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8639d-125">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8639d-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-126">0</span><span class="sxs-lookup"><span data-stu-id="8639d-126">0</span></span>

<span data-ttu-id="8639d-127">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8639d-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-128">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8639d-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-129">1</span><span class="sxs-lookup"><span data-stu-id="8639d-129">1</span></span>

<span data-ttu-id="8639d-130">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8639d-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-131">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="8639d-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-132">64</span><span class="sxs-lookup"><span data-stu-id="8639d-132">64</span></span>

<span data-ttu-id="8639d-133">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8639d-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-134">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="8639d-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-135">65</span><span class="sxs-lookup"><span data-stu-id="8639d-135">65</span></span>

<span data-ttu-id="8639d-136">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8639d-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-137">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="8639d-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-138">66</span><span class="sxs-lookup"><span data-stu-id="8639d-138">66</span></span>

<span data-ttu-id="8639d-139">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="8639d-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-140">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="8639d-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-141">67</span><span class="sxs-lookup"><span data-stu-id="8639d-141">67</span></span>

<span data-ttu-id="8639d-142">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8639d-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-143">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="8639d-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-144">68</span><span class="sxs-lookup"><span data-stu-id="8639d-144">68</span></span>

<span data-ttu-id="8639d-145">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="8639d-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-146">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="8639d-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-147">69</span><span class="sxs-lookup"><span data-stu-id="8639d-147">69</span></span>

<span data-ttu-id="8639d-148">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="8639d-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-149">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="8639d-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-150">70</span><span class="sxs-lookup"><span data-stu-id="8639d-150">70</span></span>

<span data-ttu-id="8639d-151">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8639d-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-152">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="8639d-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-153">71</span><span class="sxs-lookup"><span data-stu-id="8639d-153">71</span></span>

<span data-ttu-id="8639d-154">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8639d-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-155">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="8639d-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-156">72</span><span class="sxs-lookup"><span data-stu-id="8639d-156">72</span></span>

<span data-ttu-id="8639d-157">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="8639d-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-158">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="8639d-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-159">73</span><span class="sxs-lookup"><span data-stu-id="8639d-159">73</span></span>

<span data-ttu-id="8639d-160">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="8639d-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-161">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="8639d-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-162">74</span><span class="sxs-lookup"><span data-stu-id="8639d-162">74</span></span>

<span data-ttu-id="8639d-163">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="8639d-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-164">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="8639d-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-165">75</span><span class="sxs-lookup"><span data-stu-id="8639d-165">75</span></span>

<span data-ttu-id="8639d-166">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="8639d-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-167">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="8639d-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-168">76</span><span class="sxs-lookup"><span data-stu-id="8639d-168">76</span></span>

<span data-ttu-id="8639d-169">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="8639d-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-170">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="8639d-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-171">77</span><span class="sxs-lookup"><span data-stu-id="8639d-171">77</span></span>

<span data-ttu-id="8639d-172">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="8639d-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-173">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="8639d-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-174">78</span><span class="sxs-lookup"><span data-stu-id="8639d-174">78</span></span>

<span data-ttu-id="8639d-175">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="8639d-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-176">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="8639d-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-177">79</span><span class="sxs-lookup"><span data-stu-id="8639d-177">79</span></span>

<span data-ttu-id="8639d-178">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="8639d-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-179">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-180">80</span><span class="sxs-lookup"><span data-stu-id="8639d-180">80</span></span>

<span data-ttu-id="8639d-181">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8639d-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-182">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-183">81</span><span class="sxs-lookup"><span data-stu-id="8639d-183">81</span></span>

<span data-ttu-id="8639d-184">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8639d-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-185">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-186">82</span><span class="sxs-lookup"><span data-stu-id="8639d-186">82</span></span>

<span data-ttu-id="8639d-187">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="8639d-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-188">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="8639d-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-189">83</span><span class="sxs-lookup"><span data-stu-id="8639d-189">83</span></span>

<span data-ttu-id="8639d-190">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8639d-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-191">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8639d-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-192">84</span><span class="sxs-lookup"><span data-stu-id="8639d-192">84</span></span>

<span data-ttu-id="8639d-193">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8639d-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-194">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8639d-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-195">85</span><span class="sxs-lookup"><span data-stu-id="8639d-195">85</span></span>

<span data-ttu-id="8639d-196">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8639d-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-197">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="8639d-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-198">86</span><span class="sxs-lookup"><span data-stu-id="8639d-198">86</span></span>

<span data-ttu-id="8639d-199">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="8639d-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-200">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="8639d-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-201">87</span><span class="sxs-lookup"><span data-stu-id="8639d-201">87</span></span>

<span data-ttu-id="8639d-202">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="8639d-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-203">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="8639d-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-204">88</span><span class="sxs-lookup"><span data-stu-id="8639d-204">88</span></span>

<span data-ttu-id="8639d-205">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="8639d-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-206">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="8639d-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-207">89</span><span class="sxs-lookup"><span data-stu-id="8639d-207">89</span></span>

<span data-ttu-id="8639d-208">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="8639d-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-209">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="8639d-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-210">90</span><span class="sxs-lookup"><span data-stu-id="8639d-210">90</span></span>

<span data-ttu-id="8639d-211">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="8639d-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-212">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="8639d-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-213">91</span><span class="sxs-lookup"><span data-stu-id="8639d-213">91</span></span>

<span data-ttu-id="8639d-214">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="8639d-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-215">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="8639d-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-216">92</span><span class="sxs-lookup"><span data-stu-id="8639d-216">92</span></span>

<span data-ttu-id="8639d-217">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8639d-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-218">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-219">93</span><span class="sxs-lookup"><span data-stu-id="8639d-219">93</span></span>

<span data-ttu-id="8639d-220">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8639d-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-221">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-222">94</span><span class="sxs-lookup"><span data-stu-id="8639d-222">94</span></span>

<span data-ttu-id="8639d-223">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="8639d-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-224">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-225">95</span><span class="sxs-lookup"><span data-stu-id="8639d-225">95</span></span>

<span data-ttu-id="8639d-226">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8639d-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-227">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-228">96</span><span class="sxs-lookup"><span data-stu-id="8639d-228">96</span></span>

<span data-ttu-id="8639d-229">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8639d-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-230">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="8639d-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-231">97</span><span class="sxs-lookup"><span data-stu-id="8639d-231">97</span></span>

<span data-ttu-id="8639d-232">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="8639d-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-233">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="8639d-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-234">98</span><span class="sxs-lookup"><span data-stu-id="8639d-234">98</span></span>

<span data-ttu-id="8639d-235">Nicht alle DHCP-Leases können freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="8639d-235">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-236">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8639d-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-237">100</span><span class="sxs-lookup"><span data-stu-id="8639d-237">100</span></span>

<span data-ttu-id="8639d-238">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8639d-238">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8639d-239">**Andere**</span><span class="sxs-lookup"><span data-stu-id="8639d-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8639d-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8639d-240">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8639d-241">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8639d-241">Examples</span></span>

<span data-ttu-id="8639d-242">Das folgende Codebeispiel, das aus dem Beispiel [DNS auf allen Netzwerkadaptern](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) im VBScript-Code in der TechNet Gallery aktiviert ist, aktiviert DNS für alle Netzwerkadapter auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="8639d-242">The following code sample, taken from the [Enable DNS on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) VBScript code sample on TechNet Gallery, enables DNS for all network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
strHostName = "fabrikam1" 
arrDNSSuffixes = Array("hr.fabrikam.com", "research.fabrikam.com") 
objNetworkSettings.EnableDNS strHostName, , , arrDNSSuffixes 
```



## <a name="requirements"></a><span data-ttu-id="8639d-243">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8639d-243">Requirements</span></span>



| <span data-ttu-id="8639d-244">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8639d-244">Requirement</span></span> | <span data-ttu-id="8639d-245">Wert</span><span class="sxs-lookup"><span data-stu-id="8639d-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8639d-246">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8639d-246">Minimum supported client</span></span><br/> | <span data-ttu-id="8639d-247">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8639d-247">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8639d-248">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8639d-248">Minimum supported server</span></span><br/> | <span data-ttu-id="8639d-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8639d-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8639d-250">Namespace</span><span class="sxs-lookup"><span data-stu-id="8639d-250">Namespace</span></span><br/>                | <span data-ttu-id="8639d-251">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8639d-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8639d-252">MOF</span><span class="sxs-lookup"><span data-stu-id="8639d-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8639d-253"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8639d-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8639d-254">DLL</span><span class="sxs-lookup"><span data-stu-id="8639d-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8639d-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8639d-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8639d-256">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8639d-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8639d-257">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="8639d-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8639d-258">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="8639d-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8639d-259">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="8639d-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8639d-260">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="8639d-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8639d-261">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="8639d-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

