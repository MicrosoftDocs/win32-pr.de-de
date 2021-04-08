---
description: Die statische Methode SetPMTUDiscovery WMI-Klasse wird verwendet, um die Ermittlung von maximalen Übertragungs Einheiten (MTU) über den Pfad zu einem Remote Host zu aktivieren.
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: SetPMTUDiscovery-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748561"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="919d8-103">SetPMTUDiscovery-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="919d8-103">SetPMTUDiscovery method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="919d8-104">Die statische Methode **SetPMTUDiscovery** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Ermittlung von maximalen Übertragungs Einheiten (MTU) über den Pfad zu einem Remote Host zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="919d8-104">The **SetPMTUDiscovery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Maximum Transmission Unit (MTU) discovery over the path to a remote host.</span></span>

<span data-ttu-id="919d8-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="919d8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="919d8-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="919d8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="919d8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="919d8-107">Syntax</span></span>


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="919d8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="919d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="919d8-109">*Pmtudiscoveryaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="919d8-109">*PMTUDiscoveryEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="919d8-110">Bei " **true**" wird TCP aktiviert, um zu versuchen, die maximale Übertragungseinheit (MTU) oder die größte Paketgröße über den Pfad zu einem Remote Host zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="919d8-110">If **true**, TCP is enabled to attempt to discover the Maximum Transmission Unit (MTU) or largest packet size over the path to a remote host.</span></span> <span data-ttu-id="919d8-111">Der Standardwert ist **true**.</span><span class="sxs-lookup"><span data-stu-id="919d8-111">The default is **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="919d8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="919d8-112">Return value</span></span>

<span data-ttu-id="919d8-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="919d8-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="919d8-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="919d8-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="919d8-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="919d8-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="919d8-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="919d8-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-117">0</span><span class="sxs-lookup"><span data-stu-id="919d8-117">0</span></span>

<span data-ttu-id="919d8-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="919d8-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="919d8-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-120">1</span><span class="sxs-lookup"><span data-stu-id="919d8-120">1</span></span>

<span data-ttu-id="919d8-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="919d8-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="919d8-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-123">64</span><span class="sxs-lookup"><span data-stu-id="919d8-123">64</span></span>

<span data-ttu-id="919d8-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="919d8-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="919d8-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-126">65</span><span class="sxs-lookup"><span data-stu-id="919d8-126">65</span></span>

<span data-ttu-id="919d8-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="919d8-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="919d8-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-129">66</span><span class="sxs-lookup"><span data-stu-id="919d8-129">66</span></span>

<span data-ttu-id="919d8-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="919d8-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="919d8-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-132">67</span><span class="sxs-lookup"><span data-stu-id="919d8-132">67</span></span>

<span data-ttu-id="919d8-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="919d8-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="919d8-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-135">68</span><span class="sxs-lookup"><span data-stu-id="919d8-135">68</span></span>

<span data-ttu-id="919d8-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="919d8-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="919d8-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-138">69</span><span class="sxs-lookup"><span data-stu-id="919d8-138">69</span></span>

<span data-ttu-id="919d8-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="919d8-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="919d8-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-141">70</span><span class="sxs-lookup"><span data-stu-id="919d8-141">70</span></span>

<span data-ttu-id="919d8-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="919d8-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="919d8-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-144">71</span><span class="sxs-lookup"><span data-stu-id="919d8-144">71</span></span>

<span data-ttu-id="919d8-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="919d8-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="919d8-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-147">72</span><span class="sxs-lookup"><span data-stu-id="919d8-147">72</span></span>

<span data-ttu-id="919d8-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="919d8-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="919d8-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-150">73</span><span class="sxs-lookup"><span data-stu-id="919d8-150">73</span></span>

<span data-ttu-id="919d8-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="919d8-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="919d8-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-153">74</span><span class="sxs-lookup"><span data-stu-id="919d8-153">74</span></span>

<span data-ttu-id="919d8-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="919d8-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="919d8-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-156">75</span><span class="sxs-lookup"><span data-stu-id="919d8-156">75</span></span>

<span data-ttu-id="919d8-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="919d8-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="919d8-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-159">76</span><span class="sxs-lookup"><span data-stu-id="919d8-159">76</span></span>

<span data-ttu-id="919d8-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="919d8-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="919d8-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-162">77</span><span class="sxs-lookup"><span data-stu-id="919d8-162">77</span></span>

<span data-ttu-id="919d8-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="919d8-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="919d8-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-165">78</span><span class="sxs-lookup"><span data-stu-id="919d8-165">78</span></span>

<span data-ttu-id="919d8-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="919d8-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="919d8-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-168">79</span><span class="sxs-lookup"><span data-stu-id="919d8-168">79</span></span>

<span data-ttu-id="919d8-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="919d8-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-171">80</span><span class="sxs-lookup"><span data-stu-id="919d8-171">80</span></span>

<span data-ttu-id="919d8-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="919d8-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-174">81</span><span class="sxs-lookup"><span data-stu-id="919d8-174">81</span></span>

<span data-ttu-id="919d8-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="919d8-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-177">82</span><span class="sxs-lookup"><span data-stu-id="919d8-177">82</span></span>

<span data-ttu-id="919d8-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="919d8-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="919d8-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-180">83</span><span class="sxs-lookup"><span data-stu-id="919d8-180">83</span></span>

<span data-ttu-id="919d8-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="919d8-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="919d8-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-183">84</span><span class="sxs-lookup"><span data-stu-id="919d8-183">84</span></span>

<span data-ttu-id="919d8-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="919d8-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="919d8-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-186">85</span><span class="sxs-lookup"><span data-stu-id="919d8-186">85</span></span>

<span data-ttu-id="919d8-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="919d8-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="919d8-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-189">86</span><span class="sxs-lookup"><span data-stu-id="919d8-189">86</span></span>

<span data-ttu-id="919d8-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="919d8-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="919d8-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-192">87</span><span class="sxs-lookup"><span data-stu-id="919d8-192">87</span></span>

<span data-ttu-id="919d8-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="919d8-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="919d8-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-195">88</span><span class="sxs-lookup"><span data-stu-id="919d8-195">88</span></span>

<span data-ttu-id="919d8-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="919d8-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="919d8-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-198">89</span><span class="sxs-lookup"><span data-stu-id="919d8-198">89</span></span>

<span data-ttu-id="919d8-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="919d8-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="919d8-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-201">90</span><span class="sxs-lookup"><span data-stu-id="919d8-201">90</span></span>

<span data-ttu-id="919d8-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="919d8-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="919d8-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-204">91</span><span class="sxs-lookup"><span data-stu-id="919d8-204">91</span></span>

<span data-ttu-id="919d8-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="919d8-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="919d8-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-207">92</span><span class="sxs-lookup"><span data-stu-id="919d8-207">92</span></span>

<span data-ttu-id="919d8-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="919d8-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-210">93</span><span class="sxs-lookup"><span data-stu-id="919d8-210">93</span></span>

<span data-ttu-id="919d8-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="919d8-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-213">94</span><span class="sxs-lookup"><span data-stu-id="919d8-213">94</span></span>

<span data-ttu-id="919d8-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="919d8-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-216">95</span><span class="sxs-lookup"><span data-stu-id="919d8-216">95</span></span>

<span data-ttu-id="919d8-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="919d8-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-219">96</span><span class="sxs-lookup"><span data-stu-id="919d8-219">96</span></span>

<span data-ttu-id="919d8-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="919d8-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="919d8-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-222">97</span><span class="sxs-lookup"><span data-stu-id="919d8-222">97</span></span>

<span data-ttu-id="919d8-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="919d8-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="919d8-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-225">98</span><span class="sxs-lookup"><span data-stu-id="919d8-225">98</span></span>

<span data-ttu-id="919d8-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="919d8-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="919d8-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-228">100</span><span class="sxs-lookup"><span data-stu-id="919d8-228">100</span></span>

<span data-ttu-id="919d8-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="919d8-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="919d8-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="919d8-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="919d8-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="919d8-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="919d8-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="919d8-232">Remarks</span></span>

<span data-ttu-id="919d8-233">Wenn Sie den Pfad der MTU ermitteln und TCP-Segmente auf diese Größe beschränken, kann TCP die Fragmentierung auf Routern entlang des Pfads eliminieren, der Netzwerke mit verschiedenen MTUs verbindet.</span><span class="sxs-lookup"><span data-stu-id="919d8-233">By discovering the Path MTU and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="919d8-234">Die Fragmentierung beeinträchtigt den TCP-Durchsatz und die Überlastung des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="919d8-234">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="919d8-235">Wenn Sie diesen Parameter auf **false** festlegen, wird eine MTU von 576 Bytes für alle Verbindungen verwendet, die nicht zu Computern im lokalen Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="919d8-235">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet</span></span>

## <a name="examples"></a><span data-ttu-id="919d8-236">Beispiele</span><span class="sxs-lookup"><span data-stu-id="919d8-236">Examples</span></span>

<span data-ttu-id="919d8-237">Das Beispiel [enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript ermöglicht einem Computer das automatische ermitteln der maximalen Übertragungseinheit in einem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="919d8-237">The [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript sample enables a computer to automatically discover the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="919d8-238">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="919d8-238">Requirements</span></span>



| <span data-ttu-id="919d8-239">Anforderung</span><span class="sxs-lookup"><span data-stu-id="919d8-239">Requirement</span></span> | <span data-ttu-id="919d8-240">Wert</span><span class="sxs-lookup"><span data-stu-id="919d8-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="919d8-241">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="919d8-241">Minimum supported client</span></span><br/> | <span data-ttu-id="919d8-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="919d8-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="919d8-243">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="919d8-243">Minimum supported server</span></span><br/> | <span data-ttu-id="919d8-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="919d8-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="919d8-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="919d8-245">Namespace</span></span><br/>                | <span data-ttu-id="919d8-246">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="919d8-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="919d8-247">MOF</span><span class="sxs-lookup"><span data-stu-id="919d8-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="919d8-248"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="919d8-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="919d8-249">DLL</span><span class="sxs-lookup"><span data-stu-id="919d8-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="919d8-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="919d8-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="919d8-251">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="919d8-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919d8-252">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="919d8-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="919d8-253">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="919d8-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="919d8-254">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="919d8-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="919d8-255">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="919d8-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="919d8-256">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="919d8-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

