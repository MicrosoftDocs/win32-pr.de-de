---
description: Die Methode der EnableDHCP-WMI-Klasse aktiviert das Dynamic Host Configuration-Protokoll (DHCP) für den Dienst mit diesem Netzwerkadapter. DHCP ermöglicht das dynamische Zuordnen von IP-Adressen.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: EnableDHCP-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958314"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ce569-104">EnableDHCP-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce569-104">EnableDHCP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ce569-105">Die Methode der **EnableDHCP** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) aktiviert das Dynamic Host Configuration-Protokoll (DHCP) für den Dienst mit diesem Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="ce569-105">The **EnableDHCP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span> <span data-ttu-id="ce569-106">DHCP ermöglicht das dynamische Zuordnen von IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="ce569-106">DHCP allows IP addresses to be dynamically allocated.</span></span>

<span data-ttu-id="ce569-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce569-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ce569-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ce569-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce569-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce569-109">Syntax</span></span>


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a><span data-ttu-id="ce569-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce569-110">Parameters</span></span>

<span data-ttu-id="ce569-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ce569-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce569-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce569-112">Return value</span></span>

<span data-ttu-id="ce569-113">Gibt einen Wert von 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und jede andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ce569-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="ce569-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ce569-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ce569-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ce569-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ce569-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ce569-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-117">0</span><span class="sxs-lookup"><span data-stu-id="ce569-117">0</span></span>

<span data-ttu-id="ce569-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce569-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ce569-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-120">1</span><span class="sxs-lookup"><span data-stu-id="ce569-120">1</span></span>

<span data-ttu-id="ce569-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce569-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="ce569-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-123">64</span><span class="sxs-lookup"><span data-stu-id="ce569-123">64</span></span>

<span data-ttu-id="ce569-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce569-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="ce569-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-126">65</span><span class="sxs-lookup"><span data-stu-id="ce569-126">65</span></span>

<span data-ttu-id="ce569-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ce569-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="ce569-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-129">66</span><span class="sxs-lookup"><span data-stu-id="ce569-129">66</span></span>

<span data-ttu-id="ce569-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="ce569-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="ce569-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-132">67</span><span class="sxs-lookup"><span data-stu-id="ce569-132">67</span></span>

<span data-ttu-id="ce569-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ce569-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="ce569-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-135">68</span><span class="sxs-lookup"><span data-stu-id="ce569-135">68</span></span>

<span data-ttu-id="ce569-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="ce569-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="ce569-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-138">69</span><span class="sxs-lookup"><span data-stu-id="ce569-138">69</span></span>

<span data-ttu-id="ce569-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce569-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="ce569-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-141">70</span><span class="sxs-lookup"><span data-stu-id="ce569-141">70</span></span>

<span data-ttu-id="ce569-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ce569-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="ce569-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-144">71</span><span class="sxs-lookup"><span data-stu-id="ce569-144">71</span></span>

<span data-ttu-id="ce569-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ce569-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="ce569-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-147">72</span><span class="sxs-lookup"><span data-stu-id="ce569-147">72</span></span>

<span data-ttu-id="ce569-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="ce569-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="ce569-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-150">73</span><span class="sxs-lookup"><span data-stu-id="ce569-150">73</span></span>

<span data-ttu-id="ce569-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="ce569-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="ce569-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-153">74</span><span class="sxs-lookup"><span data-stu-id="ce569-153">74</span></span>

<span data-ttu-id="ce569-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="ce569-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="ce569-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-156">75</span><span class="sxs-lookup"><span data-stu-id="ce569-156">75</span></span>

<span data-ttu-id="ce569-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="ce569-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="ce569-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-159">76</span><span class="sxs-lookup"><span data-stu-id="ce569-159">76</span></span>

<span data-ttu-id="ce569-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="ce569-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="ce569-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-162">77</span><span class="sxs-lookup"><span data-stu-id="ce569-162">77</span></span>

<span data-ttu-id="ce569-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="ce569-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="ce569-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-165">78</span><span class="sxs-lookup"><span data-stu-id="ce569-165">78</span></span>

<span data-ttu-id="ce569-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="ce569-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="ce569-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-168">79</span><span class="sxs-lookup"><span data-stu-id="ce569-168">79</span></span>

<span data-ttu-id="ce569-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="ce569-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-171">80</span><span class="sxs-lookup"><span data-stu-id="ce569-171">80</span></span>

<span data-ttu-id="ce569-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-174">81</span><span class="sxs-lookup"><span data-stu-id="ce569-174">81</span></span>

<span data-ttu-id="ce569-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-177">82</span><span class="sxs-lookup"><span data-stu-id="ce569-177">82</span></span>

<span data-ttu-id="ce569-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="ce569-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-180">83</span><span class="sxs-lookup"><span data-stu-id="ce569-180">83</span></span>

<span data-ttu-id="ce569-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ce569-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-183">84</span><span class="sxs-lookup"><span data-stu-id="ce569-183">84</span></span>

<span data-ttu-id="ce569-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ce569-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ce569-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-186">85</span><span class="sxs-lookup"><span data-stu-id="ce569-186">85</span></span>

<span data-ttu-id="ce569-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ce569-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="ce569-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-189">86</span><span class="sxs-lookup"><span data-stu-id="ce569-189">86</span></span>

<span data-ttu-id="ce569-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="ce569-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="ce569-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-192">87</span><span class="sxs-lookup"><span data-stu-id="ce569-192">87</span></span>

<span data-ttu-id="ce569-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="ce569-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="ce569-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-195">88</span><span class="sxs-lookup"><span data-stu-id="ce569-195">88</span></span>

<span data-ttu-id="ce569-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="ce569-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="ce569-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-198">89</span><span class="sxs-lookup"><span data-stu-id="ce569-198">89</span></span>

<span data-ttu-id="ce569-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="ce569-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="ce569-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-201">90</span><span class="sxs-lookup"><span data-stu-id="ce569-201">90</span></span>

<span data-ttu-id="ce569-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="ce569-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="ce569-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-204">91</span><span class="sxs-lookup"><span data-stu-id="ce569-204">91</span></span>

<span data-ttu-id="ce569-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="ce569-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="ce569-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-207">92</span><span class="sxs-lookup"><span data-stu-id="ce569-207">92</span></span>

<span data-ttu-id="ce569-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ce569-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-210">93</span><span class="sxs-lookup"><span data-stu-id="ce569-210">93</span></span>

<span data-ttu-id="ce569-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ce569-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-213">94</span><span class="sxs-lookup"><span data-stu-id="ce569-213">94</span></span>

<span data-ttu-id="ce569-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ce569-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-216">95</span><span class="sxs-lookup"><span data-stu-id="ce569-216">95</span></span>

<span data-ttu-id="ce569-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-219">96</span><span class="sxs-lookup"><span data-stu-id="ce569-219">96</span></span>

<span data-ttu-id="ce569-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="ce569-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-222">97</span><span class="sxs-lookup"><span data-stu-id="ce569-222">97</span></span>

<span data-ttu-id="ce569-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="ce569-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="ce569-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-225">98</span><span class="sxs-lookup"><span data-stu-id="ce569-225">98</span></span>

<span data-ttu-id="ce569-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ce569-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-228">100</span><span class="sxs-lookup"><span data-stu-id="ce569-228">100</span></span>

<span data-ttu-id="ce569-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ce569-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce569-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="ce569-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ce569-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ce569-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce569-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce569-232">Remarks</span></span>

<span data-ttu-id="ce569-233">Mit dieser Methode werden keine statischen Standard Gateways gelöscht, die auf dem Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ce569-233">This method does not clears any static default gateways present on the machine.</span></span>

## <a name="examples"></a><span data-ttu-id="ce569-234">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce569-234">Examples</span></span>

<span data-ttu-id="ce569-235">Das Codebeispiel zum [Aktivieren von DHCP und zum Zuweisen von DNS-Servern](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript in der TechNet Gallery verwendet EnableDHCP zum Aktivieren von DHCP und Zuweisen von DNS-Servern zu einem Computer.</span><span class="sxs-lookup"><span data-stu-id="ce569-235">The [Enable DHCP and Assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript code sample on TechNet Gallery uses EnableDHCP to enable DHCP and assign DNS servers to a computer.</span></span>

<span data-ttu-id="ce569-236">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie die DHCP-Verwendung für eine Instanz von [**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md) aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ce569-236">The following VBScript code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="ce569-237">In diesem Fall geben wir den Adapter mit einem Index von 0 an.</span><span class="sxs-lookup"><span data-stu-id="ce569-237">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="ce569-238">Der richtige Index sollte aus den Win32- \_ NetworkAdapter-Instanzen für andere Schnittstellen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-238">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="ce569-239">Wird nur auf NT-Plattformen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce569-239">Supported on NT platforms only.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



<span data-ttu-id="ce569-240">Im folgenden perl-Codebeispiel wird veranschaulicht, wie die Verwendung von DHCP für eine Instanz von [**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md) aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ce569-240">The following Perl code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="ce569-241">In diesem Fall geben wir den Adapter mit einem Index von 0 an.</span><span class="sxs-lookup"><span data-stu-id="ce569-241">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="ce569-242">Der richtige Index sollte aus den Win32- \_ NetworkAdapter-Instanzen für andere Schnittstellen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ce569-242">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="ce569-243">Wird nur auf NT-Plattformen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce569-243">Supported on NT platforms only.</span></span>

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="ce569-244">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce569-244">Requirements</span></span>



| <span data-ttu-id="ce569-245">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce569-245">Requirement</span></span> | <span data-ttu-id="ce569-246">Wert</span><span class="sxs-lookup"><span data-stu-id="ce569-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce569-247">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce569-247">Minimum supported client</span></span><br/> | <span data-ttu-id="ce569-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce569-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce569-249">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce569-249">Minimum supported server</span></span><br/> | <span data-ttu-id="ce569-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce569-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce569-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce569-251">Namespace</span></span><br/>                | <span data-ttu-id="ce569-252">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ce569-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce569-253">MOF</span><span class="sxs-lookup"><span data-stu-id="ce569-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce569-254"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ce569-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce569-255">DLL</span><span class="sxs-lookup"><span data-stu-id="ce569-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce569-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce569-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce569-257">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce569-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce569-258">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="ce569-258">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ce569-259">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="ce569-259">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ce569-260">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ce569-260">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ce569-261">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="ce569-261">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ce569-262">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="ce569-262">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

