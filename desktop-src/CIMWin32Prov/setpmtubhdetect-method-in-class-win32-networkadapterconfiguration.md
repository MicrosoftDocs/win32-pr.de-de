---
description: Die statische Methode SetPMTUBHDetect der WMI-Klasse wird verwendet, um die Erkennung von Black-Hole-Routern bei der Verwendung von Path MTU Discovery zu aktivieren.
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: SetPMTUBHDetect-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 098652c6ea0a53f9d3b1f616def3dd8b5e7228af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127057"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="89148-103">SetPMTUBHDetect-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="89148-103">SetPMTUBHDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="89148-104">Die statische Methode **SetPMTUBHDetect** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Erkennung von Black-Hole-Routern bei der Verwendung von Path MTU Discovery zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="89148-104">The **SetPMTUBHDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable the detection of Black Hole routers while doing Path MTU Discovery.</span></span>

<span data-ttu-id="89148-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="89148-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="89148-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="89148-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="89148-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89148-107">Syntax</span></span>


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="89148-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89148-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89148-109">*PMTUBHDetectEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89148-109">*PMTUBHDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89148-110">**True** gibt an, dass TCP versucht, schwarze Löcher zu ermitteln und Pakete in verschiedenen Netzwerkpfaden weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="89148-110">If **true**, TCP attempts to discover Black Hole and route packets in different network paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89148-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89148-111">Return value</span></span>

<span data-ttu-id="89148-112">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="89148-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="89148-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="89148-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="89148-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="89148-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="89148-115">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="89148-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="89148-116">0</span><span class="sxs-lookup"><span data-stu-id="89148-116">0</span></span>

<span data-ttu-id="89148-117">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89148-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="89148-118">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="89148-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="89148-119">1</span><span class="sxs-lookup"><span data-stu-id="89148-119">1</span></span>

<span data-ttu-id="89148-120">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89148-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="89148-121">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="89148-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="89148-122">64</span><span class="sxs-lookup"><span data-stu-id="89148-122">64</span></span>

<span data-ttu-id="89148-123">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89148-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="89148-124">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="89148-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="89148-125">65</span><span class="sxs-lookup"><span data-stu-id="89148-125">65</span></span>

<span data-ttu-id="89148-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="89148-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="89148-127">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="89148-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="89148-128">66</span><span class="sxs-lookup"><span data-stu-id="89148-128">66</span></span>

<span data-ttu-id="89148-129">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="89148-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="89148-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="89148-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="89148-131">67</span><span class="sxs-lookup"><span data-stu-id="89148-131">67</span></span>

<span data-ttu-id="89148-132">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="89148-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="89148-133">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="89148-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="89148-134">68</span><span class="sxs-lookup"><span data-stu-id="89148-134">68</span></span>

<span data-ttu-id="89148-135">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="89148-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="89148-136">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="89148-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="89148-137">69</span><span class="sxs-lookup"><span data-stu-id="89148-137">69</span></span>

<span data-ttu-id="89148-138">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="89148-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="89148-139">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="89148-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="89148-140">70</span><span class="sxs-lookup"><span data-stu-id="89148-140">70</span></span>

<span data-ttu-id="89148-141">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="89148-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="89148-142">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="89148-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="89148-143">71</span><span class="sxs-lookup"><span data-stu-id="89148-143">71</span></span>

<span data-ttu-id="89148-144">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="89148-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="89148-145">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="89148-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="89148-146">72</span><span class="sxs-lookup"><span data-stu-id="89148-146">72</span></span>

<span data-ttu-id="89148-147">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="89148-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="89148-148">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="89148-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="89148-149">73</span><span class="sxs-lookup"><span data-stu-id="89148-149">73</span></span>

<span data-ttu-id="89148-150">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="89148-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="89148-151">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="89148-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="89148-152">74</span><span class="sxs-lookup"><span data-stu-id="89148-152">74</span></span>

<span data-ttu-id="89148-153">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="89148-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="89148-154">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="89148-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="89148-155">75</span><span class="sxs-lookup"><span data-stu-id="89148-155">75</span></span>

<span data-ttu-id="89148-156">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="89148-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="89148-157">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="89148-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="89148-158">76</span><span class="sxs-lookup"><span data-stu-id="89148-158">76</span></span>

<span data-ttu-id="89148-159">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="89148-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="89148-160">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="89148-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="89148-161">77</span><span class="sxs-lookup"><span data-stu-id="89148-161">77</span></span>

<span data-ttu-id="89148-162">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="89148-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="89148-163">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="89148-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="89148-164">78</span><span class="sxs-lookup"><span data-stu-id="89148-164">78</span></span>

<span data-ttu-id="89148-165">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="89148-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="89148-166">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="89148-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="89148-167">79</span><span class="sxs-lookup"><span data-stu-id="89148-167">79</span></span>

<span data-ttu-id="89148-168">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="89148-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="89148-169">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="89148-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="89148-170">80</span><span class="sxs-lookup"><span data-stu-id="89148-170">80</span></span>

<span data-ttu-id="89148-171">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="89148-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="89148-172">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="89148-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="89148-173">81</span><span class="sxs-lookup"><span data-stu-id="89148-173">81</span></span>

<span data-ttu-id="89148-174">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="89148-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="89148-175">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="89148-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="89148-176">82</span><span class="sxs-lookup"><span data-stu-id="89148-176">82</span></span>

<span data-ttu-id="89148-177">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="89148-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="89148-178">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="89148-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="89148-179">83</span><span class="sxs-lookup"><span data-stu-id="89148-179">83</span></span>

<span data-ttu-id="89148-180">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89148-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="89148-181">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="89148-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="89148-182">84</span><span class="sxs-lookup"><span data-stu-id="89148-182">84</span></span>

<span data-ttu-id="89148-183">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="89148-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="89148-184">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="89148-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="89148-185">85</span><span class="sxs-lookup"><span data-stu-id="89148-185">85</span></span>

<span data-ttu-id="89148-186">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="89148-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="89148-187">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="89148-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="89148-188">86</span><span class="sxs-lookup"><span data-stu-id="89148-188">86</span></span>

<span data-ttu-id="89148-189">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="89148-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="89148-190">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="89148-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="89148-191">87</span><span class="sxs-lookup"><span data-stu-id="89148-191">87</span></span>

<span data-ttu-id="89148-192">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="89148-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="89148-193">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="89148-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="89148-194">88</span><span class="sxs-lookup"><span data-stu-id="89148-194">88</span></span>

<span data-ttu-id="89148-195">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="89148-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="89148-196">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="89148-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="89148-197">89</span><span class="sxs-lookup"><span data-stu-id="89148-197">89</span></span>

<span data-ttu-id="89148-198">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="89148-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="89148-199">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="89148-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="89148-200">90</span><span class="sxs-lookup"><span data-stu-id="89148-200">90</span></span>

<span data-ttu-id="89148-201">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="89148-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="89148-202">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="89148-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="89148-203">91</span><span class="sxs-lookup"><span data-stu-id="89148-203">91</span></span>

<span data-ttu-id="89148-204">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="89148-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="89148-205">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="89148-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="89148-206">92</span><span class="sxs-lookup"><span data-stu-id="89148-206">92</span></span>

<span data-ttu-id="89148-207">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="89148-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="89148-208">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="89148-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="89148-209">93</span><span class="sxs-lookup"><span data-stu-id="89148-209">93</span></span>

<span data-ttu-id="89148-210">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="89148-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="89148-211">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="89148-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="89148-212">94</span><span class="sxs-lookup"><span data-stu-id="89148-212">94</span></span>

<span data-ttu-id="89148-213">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="89148-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="89148-214">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="89148-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="89148-215">95</span><span class="sxs-lookup"><span data-stu-id="89148-215">95</span></span>

<span data-ttu-id="89148-216">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="89148-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="89148-217">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="89148-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="89148-218">96</span><span class="sxs-lookup"><span data-stu-id="89148-218">96</span></span>

<span data-ttu-id="89148-219">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="89148-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="89148-220">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="89148-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="89148-221">97</span><span class="sxs-lookup"><span data-stu-id="89148-221">97</span></span>

<span data-ttu-id="89148-222">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="89148-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="89148-223">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="89148-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="89148-224">98</span><span class="sxs-lookup"><span data-stu-id="89148-224">98</span></span>

<span data-ttu-id="89148-225">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="89148-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="89148-226">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="89148-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="89148-227">100</span><span class="sxs-lookup"><span data-stu-id="89148-227">100</span></span>

<span data-ttu-id="89148-228">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="89148-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="89148-229">**Andere**</span><span class="sxs-lookup"><span data-stu-id="89148-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="89148-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="89148-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89148-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89148-231">Remarks</span></span>

<span data-ttu-id="89148-232">Ein schwarzer Loch Router gibt keine Nachrichten für das ICMP (Internet Control Message Protocol)-Ziel zurück, wenn er ein IP-Datagramm mit dem Bitsatz "nicht Fragment" fragmentieren muss.</span><span class="sxs-lookup"><span data-stu-id="89148-232">A Black Hole router does not return the Internet Control Message Protocol (ICMP) Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="89148-233">TCP ist davon abhängig, dass diese Nachrichten zum Durchführen der MTU-Ermittlung empfangen werden</span><span class="sxs-lookup"><span data-stu-id="89148-233">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span>

<span data-ttu-id="89148-234">Wenn diese Funktion aktiviert ist, versucht TCP, Segmente ohne das Bit "nicht Fragment" zu senden, wenn mehrere Neuübertragungen eines Segments nicht bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="89148-234">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="89148-235">Wenn das Segment als Ergebnis bestätigt wird, wird die maximale Segmentgröße (MSS) verringert, und das Bit "nicht Fragment" wird in zukünftigen Paketen der Verbindung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89148-235">If the segment is acknowledged as a result, the maximum segment size (MSS) will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="89148-236">Das Aktivieren der Black Hole-Erkennung erhöht die maximale Anzahl von erneuten Übertragungen, die für ein bestimmtes Segment ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="89148-236">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span>

## <a name="examples"></a><span data-ttu-id="89148-237">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89148-237">Examples</span></span>

<span data-ttu-id="89148-238">Durch die [Änderung der PMTUBH-Erkennung auf allen Netzwerkadaptern](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) wird die automatische Ermittlung von Black-Hole-Routern bei der Ermittlung der maximalen Übertragungseinheit in einem Netzwerk ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="89148-238">The [Modify PMTUBH Detection on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) enables the auto-discovery of black hole routers when determining the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="89148-239">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89148-239">Requirements</span></span>



| <span data-ttu-id="89148-240">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89148-240">Requirement</span></span> | <span data-ttu-id="89148-241">Wert</span><span class="sxs-lookup"><span data-stu-id="89148-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89148-242">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89148-242">Minimum supported client</span></span><br/> | <span data-ttu-id="89148-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89148-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89148-244">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89148-244">Minimum supported server</span></span><br/> | <span data-ttu-id="89148-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89148-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89148-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="89148-246">Namespace</span></span><br/>                | <span data-ttu-id="89148-247">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="89148-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89148-248">MOF</span><span class="sxs-lookup"><span data-stu-id="89148-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89148-249"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="89148-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89148-250">DLL</span><span class="sxs-lookup"><span data-stu-id="89148-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89148-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89148-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89148-252">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89148-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89148-253">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="89148-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="89148-254">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="89148-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="89148-255">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="89148-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="89148-256">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="89148-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="89148-257">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="89148-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

