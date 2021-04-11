---
description: Die SetIPConnectionMetric-Methode wird verwendet, um die Routing Metrik festzulegen, die diesem IP-gebundenen Adapter zugeordnet ist.
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Die Methode "stipconnectionmetric" der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73d6dde0a8faea2aeaf0982459e3c377bb1ac51d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127065"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="42aa0-103">Die Methode "stipconnectionmetric" der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="42aa0-103">SetIPConnectionMetric method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="42aa0-104">Die **SetIPConnectionMetric** -Methode wird verwendet, um die Routing Metrik festzulegen, die diesem IP-gebundenen Adapter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="42aa0-104">The **SetIPConnectionMetric** method is used to set the routing metric associated with this IP-bound adapter.</span></span>

<span data-ttu-id="42aa0-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="42aa0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="42aa0-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="42aa0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="42aa0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="42aa0-107">Syntax</span></span>


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a><span data-ttu-id="42aa0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="42aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42aa0-109">*IPConnectionMetric* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42aa0-109">*IPConnectionMetric* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-110">Gibt die Kosten für die Verwendung der konfigurierten Routen für diesen IP-gebundenen Adapter an.</span><span class="sxs-lookup"><span data-stu-id="42aa0-110">Indicates the cost of using the configured routes for this IP-bound adapter.</span></span> <span data-ttu-id="42aa0-111">Der Wert wird für diese Routen in der IP-Routing Tabelle gewichtet.</span><span class="sxs-lookup"><span data-stu-id="42aa0-111">The value is weighted for those routes in the IP routing table.</span></span> <span data-ttu-id="42aa0-112">Wenn mehrere Routen zu einem Ziel in der Routing Tabelle vorhanden sind, wird die Route mit der niedrigsten Metrik verwendet.</span><span class="sxs-lookup"><span data-stu-id="42aa0-112">If there are multiple routes to a destination in the routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="42aa0-113">Der Bereich gültiger Werte liegt zwischen 1 und 9999.</span><span class="sxs-lookup"><span data-stu-id="42aa0-113">The range of valid values is 1 through 9999.</span></span> <span data-ttu-id="42aa0-114">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="42aa0-114">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42aa0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42aa0-115">Return value</span></span>

<span data-ttu-id="42aa0-116">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="42aa0-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="42aa0-117">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="42aa0-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="42aa0-118">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="42aa0-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="42aa0-119">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="42aa0-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-120">0</span><span class="sxs-lookup"><span data-stu-id="42aa0-120">0</span></span>

<span data-ttu-id="42aa0-121">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42aa0-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-122">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="42aa0-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-123">1</span><span class="sxs-lookup"><span data-stu-id="42aa0-123">1</span></span>

<span data-ttu-id="42aa0-124">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42aa0-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-125">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-126">64</span><span class="sxs-lookup"><span data-stu-id="42aa0-126">64</span></span>

<span data-ttu-id="42aa0-127">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42aa0-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-128">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-129">65</span><span class="sxs-lookup"><span data-stu-id="42aa0-129">65</span></span>

<span data-ttu-id="42aa0-130">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="42aa0-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-131">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-132">66</span><span class="sxs-lookup"><span data-stu-id="42aa0-132">66</span></span>

<span data-ttu-id="42aa0-133">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="42aa0-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-134">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-135">67</span><span class="sxs-lookup"><span data-stu-id="42aa0-135">67</span></span>

<span data-ttu-id="42aa0-136">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="42aa0-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-137">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="42aa0-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-138">68</span><span class="sxs-lookup"><span data-stu-id="42aa0-138">68</span></span>

<span data-ttu-id="42aa0-139">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="42aa0-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-140">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-141">69</span><span class="sxs-lookup"><span data-stu-id="42aa0-141">69</span></span>

<span data-ttu-id="42aa0-142">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="42aa0-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-143">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="42aa0-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-144">70</span><span class="sxs-lookup"><span data-stu-id="42aa0-144">70</span></span>

<span data-ttu-id="42aa0-145">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="42aa0-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-146">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="42aa0-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-147">71</span><span class="sxs-lookup"><span data-stu-id="42aa0-147">71</span></span>

<span data-ttu-id="42aa0-148">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="42aa0-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-149">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-150">72</span><span class="sxs-lookup"><span data-stu-id="42aa0-150">72</span></span>

<span data-ttu-id="42aa0-151">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="42aa0-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-152">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="42aa0-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-153">73</span><span class="sxs-lookup"><span data-stu-id="42aa0-153">73</span></span>

<span data-ttu-id="42aa0-154">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="42aa0-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-155">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="42aa0-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-156">74</span><span class="sxs-lookup"><span data-stu-id="42aa0-156">74</span></span>

<span data-ttu-id="42aa0-157">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="42aa0-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-158">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-159">75</span><span class="sxs-lookup"><span data-stu-id="42aa0-159">75</span></span>

<span data-ttu-id="42aa0-160">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="42aa0-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-161">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="42aa0-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-162">76</span><span class="sxs-lookup"><span data-stu-id="42aa0-162">76</span></span>

<span data-ttu-id="42aa0-163">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="42aa0-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-164">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-165">77</span><span class="sxs-lookup"><span data-stu-id="42aa0-165">77</span></span>

<span data-ttu-id="42aa0-166">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="42aa0-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-167">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="42aa0-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-168">78</span><span class="sxs-lookup"><span data-stu-id="42aa0-168">78</span></span>

<span data-ttu-id="42aa0-169">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="42aa0-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-170">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="42aa0-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-171">79</span><span class="sxs-lookup"><span data-stu-id="42aa0-171">79</span></span>

<span data-ttu-id="42aa0-172">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="42aa0-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-173">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-174">80</span><span class="sxs-lookup"><span data-stu-id="42aa0-174">80</span></span>

<span data-ttu-id="42aa0-175">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-176">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-177">81</span><span class="sxs-lookup"><span data-stu-id="42aa0-177">81</span></span>

<span data-ttu-id="42aa0-178">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-179">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-180">82</span><span class="sxs-lookup"><span data-stu-id="42aa0-180">82</span></span>

<span data-ttu-id="42aa0-181">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-182">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="42aa0-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-183">83</span><span class="sxs-lookup"><span data-stu-id="42aa0-183">83</span></span>

<span data-ttu-id="42aa0-184">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-185">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-186">84</span><span class="sxs-lookup"><span data-stu-id="42aa0-186">84</span></span>

<span data-ttu-id="42aa0-187">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="42aa0-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-188">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-189">85</span><span class="sxs-lookup"><span data-stu-id="42aa0-189">85</span></span>

<span data-ttu-id="42aa0-190">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="42aa0-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-191">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-192">86</span><span class="sxs-lookup"><span data-stu-id="42aa0-192">86</span></span>

<span data-ttu-id="42aa0-193">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="42aa0-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-194">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="42aa0-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-195">87</span><span class="sxs-lookup"><span data-stu-id="42aa0-195">87</span></span>

<span data-ttu-id="42aa0-196">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="42aa0-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-197">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="42aa0-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-198">88</span><span class="sxs-lookup"><span data-stu-id="42aa0-198">88</span></span>

<span data-ttu-id="42aa0-199">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="42aa0-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-200">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="42aa0-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-201">89</span><span class="sxs-lookup"><span data-stu-id="42aa0-201">89</span></span>

<span data-ttu-id="42aa0-202">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="42aa0-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-203">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="42aa0-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-204">90</span><span class="sxs-lookup"><span data-stu-id="42aa0-204">90</span></span>

<span data-ttu-id="42aa0-205">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="42aa0-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-206">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="42aa0-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-207">91</span><span class="sxs-lookup"><span data-stu-id="42aa0-207">91</span></span>

<span data-ttu-id="42aa0-208">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="42aa0-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-209">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="42aa0-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-210">92</span><span class="sxs-lookup"><span data-stu-id="42aa0-210">92</span></span>

<span data-ttu-id="42aa0-211">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="42aa0-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-212">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-213">93</span><span class="sxs-lookup"><span data-stu-id="42aa0-213">93</span></span>

<span data-ttu-id="42aa0-214">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-215">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-216">94</span><span class="sxs-lookup"><span data-stu-id="42aa0-216">94</span></span>

<span data-ttu-id="42aa0-217">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-218">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-219">95</span><span class="sxs-lookup"><span data-stu-id="42aa0-219">95</span></span>

<span data-ttu-id="42aa0-220">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-221">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-222">96</span><span class="sxs-lookup"><span data-stu-id="42aa0-222">96</span></span>

<span data-ttu-id="42aa0-223">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-224">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="42aa0-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-225">97</span><span class="sxs-lookup"><span data-stu-id="42aa0-225">97</span></span>

<span data-ttu-id="42aa0-226">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="42aa0-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-227">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-228">98</span><span class="sxs-lookup"><span data-stu-id="42aa0-228">98</span></span>

<span data-ttu-id="42aa0-229">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="42aa0-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-230">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="42aa0-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-231">100</span><span class="sxs-lookup"><span data-stu-id="42aa0-231">100</span></span>

<span data-ttu-id="42aa0-232">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="42aa0-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="42aa0-233">**Andere**</span><span class="sxs-lookup"><span data-stu-id="42aa0-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="42aa0-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="42aa0-234">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="42aa0-235">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42aa0-235">Examples</span></span>

<span data-ttu-id="42aa0-236">Im Beispiel [Ändern der IP-Verbindungs Metrik für ein Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) -VBScript wird die IP-Verbindungs Metrik für einen Netzwerkadapter auf 100 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42aa0-236">The [Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript sample sets the IP connection metric for a network adapter to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="42aa0-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42aa0-237">Requirements</span></span>



| <span data-ttu-id="42aa0-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42aa0-238">Requirement</span></span> | <span data-ttu-id="42aa0-239">Wert</span><span class="sxs-lookup"><span data-stu-id="42aa0-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42aa0-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42aa0-240">Minimum supported client</span></span><br/> | <span data-ttu-id="42aa0-241">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42aa0-241">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="42aa0-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42aa0-242">Minimum supported server</span></span><br/> | <span data-ttu-id="42aa0-243">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42aa0-243">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="42aa0-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="42aa0-244">Namespace</span></span><br/>                | <span data-ttu-id="42aa0-245">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="42aa0-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="42aa0-246">MOF</span><span class="sxs-lookup"><span data-stu-id="42aa0-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42aa0-247"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="42aa0-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="42aa0-248">DLL</span><span class="sxs-lookup"><span data-stu-id="42aa0-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42aa0-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42aa0-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42aa0-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42aa0-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42aa0-251">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="42aa0-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="42aa0-252">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="42aa0-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="42aa0-253">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="42aa0-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="42aa0-254">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="42aa0-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="42aa0-255">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="42aa0-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

