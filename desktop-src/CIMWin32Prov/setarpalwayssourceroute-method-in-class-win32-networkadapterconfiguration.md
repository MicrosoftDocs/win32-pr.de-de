---
description: Die statische Methode setarpalwayssourceroute WMI-Klasse wird verwendet, um die Übertragung von ARP-Abfragen durch TCP/IP festzulegen.
ms.assetid: bbff4e2e-aea6-400e-8bd8-f62aaa9fa601
ms.tgt_platform: multiple
title: Die Methode "tartarpalwayssourceroute" der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpAlwaysSourceRoute
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7151fbbd13d3ac6fdf4ac3b129cdcb438abe73a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126284"
---
# <a name="setarpalwayssourceroute-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="83b25-103">Die Methode "tartarpalwayssourceroute" der Win32- \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="83b25-103">SetArpAlwaysSourceRoute method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="83b25-104">Die statische Methode **setarpalwayssourceroute** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Übertragung von ARP-Abfragen durch TCP/IP festzulegen.</span><span class="sxs-lookup"><span data-stu-id="83b25-104">The **SetArpAlwaysSourceRoute** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the transmission of ARP queries by TCP/IP.</span></span>

<span data-ttu-id="83b25-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="83b25-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="83b25-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="83b25-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="83b25-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="83b25-107">Syntax</span></span>


```mof
uint32 SetArpAlwaysSourceRoute(
  [in] boolean ArpAlwaysSourceRoute
);
```



## <a name="parameters"></a><span data-ttu-id="83b25-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="83b25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b25-109">*ArpAlwaysSourceRoute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83b25-109">*ArpAlwaysSourceRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b25-110">**True** gibt an, dass TCP/IP zum Übertragen von ARP-Abfragen mit aktiviertem Quell Routing auf Tokenringnetzwerken gezwungen ist.</span><span class="sxs-lookup"><span data-stu-id="83b25-110">If **true**, TCP/IP is forced to transmit ARP queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="83b25-111">Standardmäßig überträgt der Stapel ARP-Abfragen ohne Quell Routing und führt dann einen Wiederholungsversuch mit aktiviertem Quell Routing aus, wenn keine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="83b25-111">By default, the stack transmits ARP queries without source routing first, then retries with source routing enabled if no reply is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83b25-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83b25-112">Return value</span></span>

<span data-ttu-id="83b25-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="83b25-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="83b25-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="83b25-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="83b25-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="83b25-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="83b25-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="83b25-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-117">0</span><span class="sxs-lookup"><span data-stu-id="83b25-117">0</span></span>

<span data-ttu-id="83b25-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83b25-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="83b25-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-120">1</span><span class="sxs-lookup"><span data-stu-id="83b25-120">1</span></span>

<span data-ttu-id="83b25-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83b25-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="83b25-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-123">64</span><span class="sxs-lookup"><span data-stu-id="83b25-123">64</span></span>

<span data-ttu-id="83b25-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83b25-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="83b25-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-126">65</span><span class="sxs-lookup"><span data-stu-id="83b25-126">65</span></span>

<span data-ttu-id="83b25-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="83b25-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="83b25-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-129">66</span><span class="sxs-lookup"><span data-stu-id="83b25-129">66</span></span>

<span data-ttu-id="83b25-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="83b25-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="83b25-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-132">67</span><span class="sxs-lookup"><span data-stu-id="83b25-132">67</span></span>

<span data-ttu-id="83b25-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="83b25-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="83b25-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-135">68</span><span class="sxs-lookup"><span data-stu-id="83b25-135">68</span></span>

<span data-ttu-id="83b25-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="83b25-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="83b25-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-138">69</span><span class="sxs-lookup"><span data-stu-id="83b25-138">69</span></span>

<span data-ttu-id="83b25-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="83b25-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="83b25-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-141">70</span><span class="sxs-lookup"><span data-stu-id="83b25-141">70</span></span>

<span data-ttu-id="83b25-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="83b25-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="83b25-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-144">71</span><span class="sxs-lookup"><span data-stu-id="83b25-144">71</span></span>

<span data-ttu-id="83b25-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="83b25-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="83b25-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-147">72</span><span class="sxs-lookup"><span data-stu-id="83b25-147">72</span></span>

<span data-ttu-id="83b25-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="83b25-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="83b25-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-150">73</span><span class="sxs-lookup"><span data-stu-id="83b25-150">73</span></span>

<span data-ttu-id="83b25-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="83b25-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="83b25-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-153">74</span><span class="sxs-lookup"><span data-stu-id="83b25-153">74</span></span>

<span data-ttu-id="83b25-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="83b25-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="83b25-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-156">75</span><span class="sxs-lookup"><span data-stu-id="83b25-156">75</span></span>

<span data-ttu-id="83b25-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="83b25-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="83b25-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-159">76</span><span class="sxs-lookup"><span data-stu-id="83b25-159">76</span></span>

<span data-ttu-id="83b25-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="83b25-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="83b25-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-162">77</span><span class="sxs-lookup"><span data-stu-id="83b25-162">77</span></span>

<span data-ttu-id="83b25-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="83b25-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="83b25-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-165">78</span><span class="sxs-lookup"><span data-stu-id="83b25-165">78</span></span>

<span data-ttu-id="83b25-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="83b25-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="83b25-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-168">79</span><span class="sxs-lookup"><span data-stu-id="83b25-168">79</span></span>

<span data-ttu-id="83b25-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="83b25-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-171">80</span><span class="sxs-lookup"><span data-stu-id="83b25-171">80</span></span>

<span data-ttu-id="83b25-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="83b25-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-174">81</span><span class="sxs-lookup"><span data-stu-id="83b25-174">81</span></span>

<span data-ttu-id="83b25-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="83b25-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-177">82</span><span class="sxs-lookup"><span data-stu-id="83b25-177">82</span></span>

<span data-ttu-id="83b25-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="83b25-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="83b25-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-180">83</span><span class="sxs-lookup"><span data-stu-id="83b25-180">83</span></span>

<span data-ttu-id="83b25-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83b25-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="83b25-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-183">84</span><span class="sxs-lookup"><span data-stu-id="83b25-183">84</span></span>

<span data-ttu-id="83b25-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="83b25-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="83b25-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-186">85</span><span class="sxs-lookup"><span data-stu-id="83b25-186">85</span></span>

<span data-ttu-id="83b25-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="83b25-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="83b25-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-189">86</span><span class="sxs-lookup"><span data-stu-id="83b25-189">86</span></span>

<span data-ttu-id="83b25-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="83b25-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="83b25-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-192">87</span><span class="sxs-lookup"><span data-stu-id="83b25-192">87</span></span>

<span data-ttu-id="83b25-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="83b25-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="83b25-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-195">88</span><span class="sxs-lookup"><span data-stu-id="83b25-195">88</span></span>

<span data-ttu-id="83b25-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="83b25-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="83b25-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-198">89</span><span class="sxs-lookup"><span data-stu-id="83b25-198">89</span></span>

<span data-ttu-id="83b25-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="83b25-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="83b25-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-201">90</span><span class="sxs-lookup"><span data-stu-id="83b25-201">90</span></span>

<span data-ttu-id="83b25-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="83b25-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="83b25-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-204">91</span><span class="sxs-lookup"><span data-stu-id="83b25-204">91</span></span>

<span data-ttu-id="83b25-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="83b25-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="83b25-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-207">92</span><span class="sxs-lookup"><span data-stu-id="83b25-207">92</span></span>

<span data-ttu-id="83b25-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="83b25-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-210">93</span><span class="sxs-lookup"><span data-stu-id="83b25-210">93</span></span>

<span data-ttu-id="83b25-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="83b25-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-213">94</span><span class="sxs-lookup"><span data-stu-id="83b25-213">94</span></span>

<span data-ttu-id="83b25-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="83b25-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-216">95</span><span class="sxs-lookup"><span data-stu-id="83b25-216">95</span></span>

<span data-ttu-id="83b25-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="83b25-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-219">96</span><span class="sxs-lookup"><span data-stu-id="83b25-219">96</span></span>

<span data-ttu-id="83b25-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="83b25-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="83b25-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-222">97</span><span class="sxs-lookup"><span data-stu-id="83b25-222">97</span></span>

<span data-ttu-id="83b25-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="83b25-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="83b25-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-225">98</span><span class="sxs-lookup"><span data-stu-id="83b25-225">98</span></span>

<span data-ttu-id="83b25-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="83b25-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="83b25-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-228">100</span><span class="sxs-lookup"><span data-stu-id="83b25-228">100</span></span>

<span data-ttu-id="83b25-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="83b25-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="83b25-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="83b25-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="83b25-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="83b25-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="83b25-232">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83b25-232">Examples</span></span>

<span data-ttu-id="83b25-233">Das Beispiel zum [Ändern von ARP-Abfragen zum Verwenden des Quell Routings](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript in der TechNet Gallery verwendet " **starpalwayssourceroute** ", um TCP/IP so zu konfigurieren, dass immer das Quell Routing in allen Token Ring Netzwerken verwendet wird</span><span class="sxs-lookup"><span data-stu-id="83b25-233">The [Modify ARP Queries to Use Source Routing](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript sample on TechNet Gallery uses **SetArpAlwaysSourceRoute** to configure TCP/IP to always use source routing on all Token Ring networks.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b25-234">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83b25-234">Requirements</span></span>



| <span data-ttu-id="83b25-235">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83b25-235">Requirement</span></span> | <span data-ttu-id="83b25-236">Wert</span><span class="sxs-lookup"><span data-stu-id="83b25-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83b25-237">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83b25-237">Minimum supported client</span></span><br/> | <span data-ttu-id="83b25-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83b25-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83b25-239">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83b25-239">Minimum supported server</span></span><br/> | <span data-ttu-id="83b25-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83b25-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83b25-241">Namespace</span><span class="sxs-lookup"><span data-stu-id="83b25-241">Namespace</span></span><br/>                | <span data-ttu-id="83b25-242">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="83b25-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83b25-243">MOF</span><span class="sxs-lookup"><span data-stu-id="83b25-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83b25-244"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="83b25-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83b25-245">DLL</span><span class="sxs-lookup"><span data-stu-id="83b25-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83b25-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83b25-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83b25-247">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83b25-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b25-248">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="83b25-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="83b25-249">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="83b25-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="83b25-250">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="83b25-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="83b25-251">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="83b25-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="83b25-252">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="83b25-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

