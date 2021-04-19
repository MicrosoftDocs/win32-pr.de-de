---
description: Die statische Methode der ReleaseDHCPLeaseAll-WMI-Klasse gibt die IP-Adressen frei, die an alle DHCP-fähigen Netzwerkadapter gebunden sind.
ms.assetid: d9f83953-f3da-419d-8c84-649c39b4945e
ms.tgt_platform: multiple
title: ReleaseDHCPLeaseAll-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e7b1f7cf2f09fa20f7bf19b15e82f536ca0aa50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343184"
---
# <a name="releasedhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8e784-103">ReleaseDHCPLeaseAll-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e784-103">ReleaseDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8e784-104">Die statische Methode der **ReleaseDHCPLeaseAll** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) gibt die IP-Adressen frei, die an alle DHCP-fähigen Netzwerkadapter gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="8e784-104">The **ReleaseDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method releases the IP addresses bound to all DHCP-enabled network adapters.</span></span>

> [!Note]  
> <span data-ttu-id="8e784-105">Warnung wenn DHCP auf dem lokalen Computersystem aktiviert ist, werden alle DHCP-TCP/IP-Verbindungen beendet.</span><span class="sxs-lookup"><span data-stu-id="8e784-105">Warning If DHCP is enabled on the local computer system, the option will terminate all DHCP TCP/IP connections.</span></span>

 

<span data-ttu-id="8e784-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e784-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e784-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8e784-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e784-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e784-108">Syntax</span></span>


```mof
uint32 ReleaseDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="8e784-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e784-109">Parameters</span></span>

<span data-ttu-id="8e784-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e784-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e784-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e784-111">Return value</span></span>

<span data-ttu-id="8e784-112">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="8e784-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8e784-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8e784-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8e784-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8e784-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8e784-115">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8e784-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-116">0</span><span class="sxs-lookup"><span data-stu-id="8e784-116">0</span></span>

<span data-ttu-id="8e784-117">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8e784-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-118">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8e784-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-119">1</span><span class="sxs-lookup"><span data-stu-id="8e784-119">1</span></span>

<span data-ttu-id="8e784-120">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8e784-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-121">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="8e784-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-122">64</span><span class="sxs-lookup"><span data-stu-id="8e784-122">64</span></span>

<span data-ttu-id="8e784-123">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e784-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-124">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="8e784-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-125">65</span><span class="sxs-lookup"><span data-stu-id="8e784-125">65</span></span>

<span data-ttu-id="8e784-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8e784-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-127">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="8e784-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-128">66</span><span class="sxs-lookup"><span data-stu-id="8e784-128">66</span></span>

<span data-ttu-id="8e784-129">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="8e784-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="8e784-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-131">67</span><span class="sxs-lookup"><span data-stu-id="8e784-131">67</span></span>

<span data-ttu-id="8e784-132">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8e784-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-133">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="8e784-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-134">68</span><span class="sxs-lookup"><span data-stu-id="8e784-134">68</span></span>

<span data-ttu-id="8e784-135">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="8e784-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-136">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="8e784-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-137">69</span><span class="sxs-lookup"><span data-stu-id="8e784-137">69</span></span>

<span data-ttu-id="8e784-138">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="8e784-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-139">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="8e784-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-140">70</span><span class="sxs-lookup"><span data-stu-id="8e784-140">70</span></span>

<span data-ttu-id="8e784-141">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8e784-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-142">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="8e784-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-143">71</span><span class="sxs-lookup"><span data-stu-id="8e784-143">71</span></span>

<span data-ttu-id="8e784-144">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8e784-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-145">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="8e784-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-146">72</span><span class="sxs-lookup"><span data-stu-id="8e784-146">72</span></span>

<span data-ttu-id="8e784-147">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="8e784-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-148">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="8e784-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-149">73</span><span class="sxs-lookup"><span data-stu-id="8e784-149">73</span></span>

<span data-ttu-id="8e784-150">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="8e784-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-151">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="8e784-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-152">74</span><span class="sxs-lookup"><span data-stu-id="8e784-152">74</span></span>

<span data-ttu-id="8e784-153">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="8e784-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-154">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="8e784-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-155">75</span><span class="sxs-lookup"><span data-stu-id="8e784-155">75</span></span>

<span data-ttu-id="8e784-156">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="8e784-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-157">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="8e784-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-158">76</span><span class="sxs-lookup"><span data-stu-id="8e784-158">76</span></span>

<span data-ttu-id="8e784-159">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="8e784-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-160">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="8e784-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-161">77</span><span class="sxs-lookup"><span data-stu-id="8e784-161">77</span></span>

<span data-ttu-id="8e784-162">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="8e784-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-163">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="8e784-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-164">78</span><span class="sxs-lookup"><span data-stu-id="8e784-164">78</span></span>

<span data-ttu-id="8e784-165">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="8e784-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-166">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="8e784-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-167">79</span><span class="sxs-lookup"><span data-stu-id="8e784-167">79</span></span>

<span data-ttu-id="8e784-168">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="8e784-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-169">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-170">80</span><span class="sxs-lookup"><span data-stu-id="8e784-170">80</span></span>

<span data-ttu-id="8e784-171">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-172">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-173">81</span><span class="sxs-lookup"><span data-stu-id="8e784-173">81</span></span>

<span data-ttu-id="8e784-174">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-175">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-176">82</span><span class="sxs-lookup"><span data-stu-id="8e784-176">82</span></span>

<span data-ttu-id="8e784-177">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-178">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="8e784-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-179">83</span><span class="sxs-lookup"><span data-stu-id="8e784-179">83</span></span>

<span data-ttu-id="8e784-180">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-181">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8e784-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-182">84</span><span class="sxs-lookup"><span data-stu-id="8e784-182">84</span></span>

<span data-ttu-id="8e784-183">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e784-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-184">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8e784-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-185">85</span><span class="sxs-lookup"><span data-stu-id="8e784-185">85</span></span>

<span data-ttu-id="8e784-186">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e784-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-187">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="8e784-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-188">86</span><span class="sxs-lookup"><span data-stu-id="8e784-188">86</span></span>

<span data-ttu-id="8e784-189">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="8e784-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-190">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="8e784-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-191">87</span><span class="sxs-lookup"><span data-stu-id="8e784-191">87</span></span>

<span data-ttu-id="8e784-192">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="8e784-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-193">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="8e784-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-194">88</span><span class="sxs-lookup"><span data-stu-id="8e784-194">88</span></span>

<span data-ttu-id="8e784-195">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="8e784-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-196">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="8e784-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-197">89</span><span class="sxs-lookup"><span data-stu-id="8e784-197">89</span></span>

<span data-ttu-id="8e784-198">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="8e784-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-199">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="8e784-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-200">90</span><span class="sxs-lookup"><span data-stu-id="8e784-200">90</span></span>

<span data-ttu-id="8e784-201">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="8e784-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-202">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="8e784-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-203">91</span><span class="sxs-lookup"><span data-stu-id="8e784-203">91</span></span>

<span data-ttu-id="8e784-204">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="8e784-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-205">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="8e784-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-206">92</span><span class="sxs-lookup"><span data-stu-id="8e784-206">92</span></span>

<span data-ttu-id="8e784-207">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8e784-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-208">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-209">93</span><span class="sxs-lookup"><span data-stu-id="8e784-209">93</span></span>

<span data-ttu-id="8e784-210">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8e784-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-211">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-212">94</span><span class="sxs-lookup"><span data-stu-id="8e784-212">94</span></span>

<span data-ttu-id="8e784-213">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="8e784-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-214">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-215">95</span><span class="sxs-lookup"><span data-stu-id="8e784-215">95</span></span>

<span data-ttu-id="8e784-216">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-217">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-218">96</span><span class="sxs-lookup"><span data-stu-id="8e784-218">96</span></span>

<span data-ttu-id="8e784-219">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-220">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="8e784-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-221">97</span><span class="sxs-lookup"><span data-stu-id="8e784-221">97</span></span>

<span data-ttu-id="8e784-222">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="8e784-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-223">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="8e784-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-224">98</span><span class="sxs-lookup"><span data-stu-id="8e784-224">98</span></span>

<span data-ttu-id="8e784-225">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-226">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8e784-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-227">100</span><span class="sxs-lookup"><span data-stu-id="8e784-227">100</span></span>

<span data-ttu-id="8e784-228">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e784-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e784-229">**Andere**</span><span class="sxs-lookup"><span data-stu-id="8e784-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8e784-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8e784-230">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8e784-231">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e784-231">Examples</span></span>

<span data-ttu-id="8e784-232">Im folgenden VBScript-Codebeispiel werden alle DHCP-Leases freigegeben, die zurzeit auf einem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e784-232">The following VBScript code sample releases all the DHCP leases currently in use on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.ReleaseDHCPLeaseAll() 
```



## <a name="requirements"></a><span data-ttu-id="8e784-233">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e784-233">Requirements</span></span>



| <span data-ttu-id="8e784-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e784-234">Requirement</span></span> | <span data-ttu-id="8e784-235">Wert</span><span class="sxs-lookup"><span data-stu-id="8e784-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e784-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e784-236">Minimum supported client</span></span><br/> | <span data-ttu-id="8e784-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e784-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e784-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e784-238">Minimum supported server</span></span><br/> | <span data-ttu-id="8e784-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e784-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e784-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e784-240">Namespace</span></span><br/>                | <span data-ttu-id="8e784-241">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e784-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e784-242">MOF</span><span class="sxs-lookup"><span data-stu-id="8e784-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e784-243"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e784-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e784-244">DLL</span><span class="sxs-lookup"><span data-stu-id="8e784-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e784-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e784-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e784-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e784-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e784-247">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e784-247">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8e784-248">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="8e784-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8e784-249">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="8e784-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8e784-250">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="8e784-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8e784-251">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="8e784-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

