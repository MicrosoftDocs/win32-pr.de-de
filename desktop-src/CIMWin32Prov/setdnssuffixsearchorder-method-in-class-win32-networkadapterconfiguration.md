---
description: Die statische Methode SetDNSSuffixSearchOrder WMI-Klasse verwendet ein Array von Zeichen folgen Elementen, um die Suffixsuchreihenfolge festzulegen.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: SetDNSSuffixSearchOrder-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10088b1d0722f968e5d3742984baa91ec3e423aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861383"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="37737-103">SetDNSSuffixSearchOrder-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="37737-103">SetDNSSuffixSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="37737-104">Die statische Methode **SetDNSSuffixSearchOrder** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) verwendet ein Array von Zeichen folgen Elementen, um die Suffixsuchreihenfolge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="37737-104">The **SetDNSSuffixSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method uses an array of string elements to set the suffix search order.</span></span>

<span data-ttu-id="37737-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="37737-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="37737-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="37737-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="37737-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37737-107">Syntax</span></span>


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="37737-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37737-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37737-109">*DNSDomainSuffixSearchOrder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37737-109">*DNSDomainSuffixSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37737-110">Liste der Server Suffixe, die für DNS-Server abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37737-110">List of server suffixes to query for DNS servers.</span></span> <span data-ttu-id="37737-111">Der Registrierungs Speicherort des DNS-Suffixes ist **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **tcpip \| Nameserver**</span><span class="sxs-lookup"><span data-stu-id="37737-111">The registry location of the DNS suffix is **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Tcpip\|NameServer**</span></span>

<span data-ttu-id="37737-112">Beispiel: "suffix1.Company.com", "suffix2.Company.com"</span><span class="sxs-lookup"><span data-stu-id="37737-112">Example: "suffix1.company.com", "suffix2.company.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37737-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37737-113">Return value</span></span>

<span data-ttu-id="37737-114">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="37737-114">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="37737-115">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="37737-115">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="37737-116">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="37737-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="37737-117">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="37737-117">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="37737-118">0</span><span class="sxs-lookup"><span data-stu-id="37737-118">0</span></span>

<span data-ttu-id="37737-119">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37737-119">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="37737-120">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="37737-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="37737-121">1</span><span class="sxs-lookup"><span data-stu-id="37737-121">1</span></span>

<span data-ttu-id="37737-122">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37737-122">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="37737-123">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="37737-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="37737-124">64</span><span class="sxs-lookup"><span data-stu-id="37737-124">64</span></span>

<span data-ttu-id="37737-125">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37737-125">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="37737-126">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="37737-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="37737-127">65</span><span class="sxs-lookup"><span data-stu-id="37737-127">65</span></span>

<span data-ttu-id="37737-128">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="37737-128">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="37737-129">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="37737-129">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="37737-130">66</span><span class="sxs-lookup"><span data-stu-id="37737-130">66</span></span>

<span data-ttu-id="37737-131">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="37737-131">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="37737-132">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="37737-132">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="37737-133">67</span><span class="sxs-lookup"><span data-stu-id="37737-133">67</span></span>

<span data-ttu-id="37737-134">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="37737-134">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="37737-135">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="37737-135">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="37737-136">68</span><span class="sxs-lookup"><span data-stu-id="37737-136">68</span></span>

<span data-ttu-id="37737-137">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="37737-137">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="37737-138">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="37737-138">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="37737-139">69</span><span class="sxs-lookup"><span data-stu-id="37737-139">69</span></span>

<span data-ttu-id="37737-140">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="37737-140">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="37737-141">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="37737-141">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="37737-142">70</span><span class="sxs-lookup"><span data-stu-id="37737-142">70</span></span>

<span data-ttu-id="37737-143">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="37737-143">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="37737-144">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="37737-144">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="37737-145">71</span><span class="sxs-lookup"><span data-stu-id="37737-145">71</span></span>

<span data-ttu-id="37737-146">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="37737-146">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="37737-147">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="37737-147">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="37737-148">72</span><span class="sxs-lookup"><span data-stu-id="37737-148">72</span></span>

<span data-ttu-id="37737-149">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="37737-149">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="37737-150">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="37737-150">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="37737-151">73</span><span class="sxs-lookup"><span data-stu-id="37737-151">73</span></span>

<span data-ttu-id="37737-152">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="37737-152">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="37737-153">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="37737-153">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="37737-154">74</span><span class="sxs-lookup"><span data-stu-id="37737-154">74</span></span>

<span data-ttu-id="37737-155">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="37737-155">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="37737-156">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="37737-156">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="37737-157">75</span><span class="sxs-lookup"><span data-stu-id="37737-157">75</span></span>

<span data-ttu-id="37737-158">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="37737-158">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="37737-159">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="37737-159">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="37737-160">76</span><span class="sxs-lookup"><span data-stu-id="37737-160">76</span></span>

<span data-ttu-id="37737-161">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="37737-161">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="37737-162">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="37737-162">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="37737-163">77</span><span class="sxs-lookup"><span data-stu-id="37737-163">77</span></span>

<span data-ttu-id="37737-164">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="37737-164">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="37737-165">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="37737-165">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="37737-166">78</span><span class="sxs-lookup"><span data-stu-id="37737-166">78</span></span>

<span data-ttu-id="37737-167">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="37737-167">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="37737-168">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="37737-168">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="37737-169">79</span><span class="sxs-lookup"><span data-stu-id="37737-169">79</span></span>

<span data-ttu-id="37737-170">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="37737-170">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="37737-171">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="37737-171">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="37737-172">80</span><span class="sxs-lookup"><span data-stu-id="37737-172">80</span></span>

<span data-ttu-id="37737-173">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="37737-173">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="37737-174">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="37737-174">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="37737-175">81</span><span class="sxs-lookup"><span data-stu-id="37737-175">81</span></span>

<span data-ttu-id="37737-176">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="37737-176">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="37737-177">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="37737-177">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="37737-178">82</span><span class="sxs-lookup"><span data-stu-id="37737-178">82</span></span>

<span data-ttu-id="37737-179">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="37737-179">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="37737-180">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="37737-180">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="37737-181">83</span><span class="sxs-lookup"><span data-stu-id="37737-181">83</span></span>

<span data-ttu-id="37737-182">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37737-182">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="37737-183">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="37737-183">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="37737-184">84</span><span class="sxs-lookup"><span data-stu-id="37737-184">84</span></span>

<span data-ttu-id="37737-185">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37737-185">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="37737-186">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="37737-186">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="37737-187">85</span><span class="sxs-lookup"><span data-stu-id="37737-187">85</span></span>

<span data-ttu-id="37737-188">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37737-188">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="37737-189">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="37737-189">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="37737-190">86</span><span class="sxs-lookup"><span data-stu-id="37737-190">86</span></span>

<span data-ttu-id="37737-191">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="37737-191">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="37737-192">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="37737-192">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="37737-193">87</span><span class="sxs-lookup"><span data-stu-id="37737-193">87</span></span>

<span data-ttu-id="37737-194">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="37737-194">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="37737-195">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="37737-195">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="37737-196">88</span><span class="sxs-lookup"><span data-stu-id="37737-196">88</span></span>

<span data-ttu-id="37737-197">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="37737-197">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="37737-198">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="37737-198">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="37737-199">89</span><span class="sxs-lookup"><span data-stu-id="37737-199">89</span></span>

<span data-ttu-id="37737-200">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="37737-200">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="37737-201">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="37737-201">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="37737-202">90</span><span class="sxs-lookup"><span data-stu-id="37737-202">90</span></span>

<span data-ttu-id="37737-203">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="37737-203">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="37737-204">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="37737-204">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="37737-205">91</span><span class="sxs-lookup"><span data-stu-id="37737-205">91</span></span>

<span data-ttu-id="37737-206">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="37737-206">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="37737-207">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="37737-207">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="37737-208">92</span><span class="sxs-lookup"><span data-stu-id="37737-208">92</span></span>

<span data-ttu-id="37737-209">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37737-209">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="37737-210">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="37737-210">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="37737-211">93</span><span class="sxs-lookup"><span data-stu-id="37737-211">93</span></span>

<span data-ttu-id="37737-212">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37737-212">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="37737-213">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="37737-213">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="37737-214">94</span><span class="sxs-lookup"><span data-stu-id="37737-214">94</span></span>

<span data-ttu-id="37737-215">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="37737-215">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="37737-216">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="37737-216">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="37737-217">95</span><span class="sxs-lookup"><span data-stu-id="37737-217">95</span></span>

<span data-ttu-id="37737-218">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="37737-218">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="37737-219">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="37737-219">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="37737-220">96</span><span class="sxs-lookup"><span data-stu-id="37737-220">96</span></span>

<span data-ttu-id="37737-221">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="37737-221">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="37737-222">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="37737-222">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="37737-223">97</span><span class="sxs-lookup"><span data-stu-id="37737-223">97</span></span>

<span data-ttu-id="37737-224">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="37737-224">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="37737-225">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="37737-225">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="37737-226">98</span><span class="sxs-lookup"><span data-stu-id="37737-226">98</span></span>

<span data-ttu-id="37737-227">Nicht alle DHCP-Leases werden freigegeben oder erneuert.</span><span class="sxs-lookup"><span data-stu-id="37737-227">Not all DHCP leases are released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="37737-228">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="37737-228">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="37737-229">100</span><span class="sxs-lookup"><span data-stu-id="37737-229">100</span></span>

<span data-ttu-id="37737-230">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37737-230">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="37737-231">**Andere**</span><span class="sxs-lookup"><span data-stu-id="37737-231">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="37737-232">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="37737-232">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37737-233">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37737-233">Remarks</span></span>

<span data-ttu-id="37737-234">Dabei handelt es sich um einen instanzunabhängigen-Rückruf, der für alle Adapter gilt, aber nur für Windows.</span><span class="sxs-lookup"><span data-stu-id="37737-234">This is an instance-independent call that applies to all adapters but only for Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="37737-235">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37737-235">Examples</span></span>

<span data-ttu-id="37737-236">Das Codebeispiel [Ändern der DNS-suffixsuche für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript konfiguriert einen Computer so, dass beim Durchführen von DNS-Suchen zwei DNS-Suffixe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37737-236">The [Modify the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript code sample configures a computer to use two DNS suffixes when performing DNS searches.</span></span>

<span data-ttu-id="37737-237">Im Beispiel [Enable DHCP settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript werden alle Einstellungen konfiguriert, die in der Regel zum Aktivieren von DHCP auf einem Computer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="37737-237">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample configures all the settings typically required to enable DHCP on a computer.</span></span>

<span data-ttu-id="37737-238">Der folgende PowerShell-Code legt die Such Reihenfolge für das DNS-Suffix fest</span><span class="sxs-lookup"><span data-stu-id="37737-238">The following PowerShell code sets the DNS suffix search order.</span></span>


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



## <a name="requirements"></a><span data-ttu-id="37737-239">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37737-239">Requirements</span></span>



| <span data-ttu-id="37737-240">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37737-240">Requirement</span></span> | <span data-ttu-id="37737-241">Wert</span><span class="sxs-lookup"><span data-stu-id="37737-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37737-242">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37737-242">Minimum supported client</span></span><br/> | <span data-ttu-id="37737-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37737-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37737-244">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37737-244">Minimum supported server</span></span><br/> | <span data-ttu-id="37737-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37737-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37737-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="37737-246">Namespace</span></span><br/>                | <span data-ttu-id="37737-247">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="37737-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37737-248">MOF</span><span class="sxs-lookup"><span data-stu-id="37737-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37737-249"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37737-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37737-250">DLL</span><span class="sxs-lookup"><span data-stu-id="37737-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37737-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37737-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37737-252">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37737-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37737-253">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="37737-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="37737-254">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="37737-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="37737-255">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="37737-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="37737-256">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="37737-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="37737-257">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="37737-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

