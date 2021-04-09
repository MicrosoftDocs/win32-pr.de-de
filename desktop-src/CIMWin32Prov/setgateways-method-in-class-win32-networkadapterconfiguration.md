---
description: Die SetGateways &\# 32; WMI-Klassenmethode gibt eine Liste von Gateways für das Routing von Paketen an ein Subnetz an, das sich von dem Subnetz unterscheidet, mit dem der Netzwerkadapter verbunden ist.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: SetGateways-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861316"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d1579-103">SetGateways-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1579-103">SetGateways method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d1579-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetGateways** gibt eine Liste von Gateways für das Routing von Paketen an ein Subnetz an, das sich von dem Subnetz unterscheidet, mit dem der Netzwerkadapter verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d1579-104">The **SetGateways** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method specifies a list of gateways for routing packets to a subnet that is different from the subnet that the network adapter is connected to.</span></span>

<span data-ttu-id="d1579-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1579-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d1579-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d1579-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1579-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1579-107">Syntax</span></span>


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a><span data-ttu-id="d1579-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1579-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1579-109">*DefaultIPGateway* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1579-109">*DefaultIPGateway* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1579-110">Liste der IP-Adressen für Gateways, an die Netzwerkpakete weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="d1579-110">List of IP addresses to gateways where network packets are routed.</span></span>

</dd> <dt>

<span data-ttu-id="d1579-111">*GatewayCostMetric* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d1579-111">*GatewayCostMetric* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1579-112">Weist einen Wert zwischen 1 und 9999 zu, der verwendet wird, um die schnellsten und zuverlässigsten Routen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d1579-112">Assigns a value that ranges from 1 to 9999, which is used to calculate the fastest and most reliable routes.</span></span> <span data-ttu-id="d1579-113">Die Werte dieses Parameters entsprechen den Werten im *DefaultIPGateway* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d1579-113">The values of this parameter correspond with the values in the *DefaultIPGateway* parameter.</span></span> <span data-ttu-id="d1579-114">Der Standardwert für ein Gateway ist 1.</span><span class="sxs-lookup"><span data-stu-id="d1579-114">The default value for a gateway is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1579-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1579-115">Return value</span></span>

<span data-ttu-id="d1579-116">Gibt einen Wert von 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und ein beliebiger anderer Wert, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="d1579-116">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other value if there is an error.</span></span> <span data-ttu-id="d1579-117">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d1579-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d1579-118">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d1579-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d1579-119">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d1579-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-120">0</span><span class="sxs-lookup"><span data-stu-id="d1579-120">0</span></span>

</dd> <dt>

<span data-ttu-id="d1579-121">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d1579-121">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-122">1</span><span class="sxs-lookup"><span data-stu-id="d1579-122">1</span></span>

</dd> <dt>

<span data-ttu-id="d1579-123">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="d1579-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-124">64</span><span class="sxs-lookup"><span data-stu-id="d1579-124">64</span></span>

<span data-ttu-id="d1579-125">Methode wird nicht unterstützt, wenn sich die NIC im DHCP-Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="d1579-125">Method not supported when the NIC is in DHCP mode.</span></span>

</dd> <dt>

<span data-ttu-id="d1579-126">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d1579-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-127">65</span><span class="sxs-lookup"><span data-stu-id="d1579-127">65</span></span>

</dd> <dt>

<span data-ttu-id="d1579-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="d1579-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-129">66</span><span class="sxs-lookup"><span data-stu-id="d1579-129">66</span></span>

</dd> <dt>

<span data-ttu-id="d1579-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="d1579-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-131">67</span><span class="sxs-lookup"><span data-stu-id="d1579-131">67</span></span>

</dd> <dt>

<span data-ttu-id="d1579-132">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="d1579-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-133">68</span><span class="sxs-lookup"><span data-stu-id="d1579-133">68</span></span>

</dd> <dt>

<span data-ttu-id="d1579-134">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="d1579-134">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-135">69</span><span class="sxs-lookup"><span data-stu-id="d1579-135">69</span></span>

</dd> <dt>

<span data-ttu-id="d1579-136">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="d1579-136">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-137">70</span><span class="sxs-lookup"><span data-stu-id="d1579-137">70</span></span>

</dd> <dt>

<span data-ttu-id="d1579-138">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="d1579-138">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-139">71</span><span class="sxs-lookup"><span data-stu-id="d1579-139">71</span></span>

</dd> <dt>

<span data-ttu-id="d1579-140">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="d1579-140">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-141">72</span><span class="sxs-lookup"><span data-stu-id="d1579-141">72</span></span>

</dd> <dt>

<span data-ttu-id="d1579-142">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="d1579-142">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-143">73</span><span class="sxs-lookup"><span data-stu-id="d1579-143">73</span></span>

</dd> <dt>

<span data-ttu-id="d1579-144">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="d1579-144">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-145">74</span><span class="sxs-lookup"><span data-stu-id="d1579-145">74</span></span>

</dd> <dt>

<span data-ttu-id="d1579-146">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="d1579-146">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-147">75</span><span class="sxs-lookup"><span data-stu-id="d1579-147">75</span></span>

</dd> <dt>

<span data-ttu-id="d1579-148">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="d1579-148">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-149">76</span><span class="sxs-lookup"><span data-stu-id="d1579-149">76</span></span>

</dd> <dt>

<span data-ttu-id="d1579-150">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="d1579-150">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-151">77</span><span class="sxs-lookup"><span data-stu-id="d1579-151">77</span></span>

</dd> <dt>

<span data-ttu-id="d1579-152">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="d1579-152">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-153">78</span><span class="sxs-lookup"><span data-stu-id="d1579-153">78</span></span>

</dd> <dt>

<span data-ttu-id="d1579-154">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="d1579-154">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-155">79</span><span class="sxs-lookup"><span data-stu-id="d1579-155">79</span></span>

</dd> <dt>

<span data-ttu-id="d1579-156">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-156">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-157">80</span><span class="sxs-lookup"><span data-stu-id="d1579-157">80</span></span>

</dd> <dt>

<span data-ttu-id="d1579-158">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-158">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-159">81</span><span class="sxs-lookup"><span data-stu-id="d1579-159">81</span></span>

</dd> <dt>

<span data-ttu-id="d1579-160">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-160">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-161">82</span><span class="sxs-lookup"><span data-stu-id="d1579-161">82</span></span>

</dd> <dt>

<span data-ttu-id="d1579-162">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="d1579-162">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-163">83</span><span class="sxs-lookup"><span data-stu-id="d1579-163">83</span></span>

</dd> <dt>

<span data-ttu-id="d1579-164">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="d1579-164">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-165">84</span><span class="sxs-lookup"><span data-stu-id="d1579-165">84</span></span>

</dd> <dt>

<span data-ttu-id="d1579-166">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="d1579-166">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-167">85</span><span class="sxs-lookup"><span data-stu-id="d1579-167">85</span></span>

</dd> <dt>

<span data-ttu-id="d1579-168">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="d1579-168">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-169">86</span><span class="sxs-lookup"><span data-stu-id="d1579-169">86</span></span>

</dd> <dt>

<span data-ttu-id="d1579-170">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="d1579-170">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-171">87</span><span class="sxs-lookup"><span data-stu-id="d1579-171">87</span></span>

</dd> <dt>

<span data-ttu-id="d1579-172">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="d1579-172">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-173">88</span><span class="sxs-lookup"><span data-stu-id="d1579-173">88</span></span>

</dd> <dt>

<span data-ttu-id="d1579-174">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="d1579-174">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-175">89</span><span class="sxs-lookup"><span data-stu-id="d1579-175">89</span></span>

</dd> <dt>

<span data-ttu-id="d1579-176">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="d1579-176">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-177">90</span><span class="sxs-lookup"><span data-stu-id="d1579-177">90</span></span>

</dd> <dt>

<span data-ttu-id="d1579-178">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="d1579-178">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-179">91</span><span class="sxs-lookup"><span data-stu-id="d1579-179">91</span></span>

</dd> <dt>

<span data-ttu-id="d1579-180">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="d1579-180">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-181">92</span><span class="sxs-lookup"><span data-stu-id="d1579-181">92</span></span>

</dd> <dt>

<span data-ttu-id="d1579-182">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-182">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-183">93</span><span class="sxs-lookup"><span data-stu-id="d1579-183">93</span></span>

</dd> <dt>

<span data-ttu-id="d1579-184">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-184">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-185">94</span><span class="sxs-lookup"><span data-stu-id="d1579-185">94</span></span>

</dd> <dt>

<span data-ttu-id="d1579-186">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-186">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-187">95</span><span class="sxs-lookup"><span data-stu-id="d1579-187">95</span></span>

</dd> <dt>

<span data-ttu-id="d1579-188">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-188">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-189">96</span><span class="sxs-lookup"><span data-stu-id="d1579-189">96</span></span>

</dd> <dt>

<span data-ttu-id="d1579-190">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="d1579-190">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-191">97</span><span class="sxs-lookup"><span data-stu-id="d1579-191">97</span></span>

</dd> <dt>

<span data-ttu-id="d1579-192">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1579-192">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-193">98</span><span class="sxs-lookup"><span data-stu-id="d1579-193">98</span></span>

</dd> <dt>

<span data-ttu-id="d1579-194">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="d1579-194">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-195">100</span><span class="sxs-lookup"><span data-stu-id="d1579-195">100</span></span>

</dd> <dt>

<span data-ttu-id="d1579-196">**Andere**</span><span class="sxs-lookup"><span data-stu-id="d1579-196">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d1579-197">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d1579-197">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1579-198">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1579-198">Remarks</span></span>

<span data-ttu-id="d1579-199">Diese Methode funktioniert nur, wenn sich die Netzwerkschnittstellenkarte (NIC) im statischen IP-Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="d1579-199">This method only works when the Network Interface Card (NIC) is in the static IP mode.</span></span>

<span data-ttu-id="d1579-200">Um das Gateway zu löschen, legen Sie das Gateway auf die gleiche IP-Adresse fest, die Sie in [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1579-200">To clear the gateway, set your gateway to the same IP you use on [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d1579-201">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1579-201">Examples</span></span>

<span data-ttu-id="d1579-202">Im Beispiel [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript werden zwei Gateways für einen Netzwerkadapter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d1579-202">The [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript sample configures two gateways for a network adapter.</span></span>

<span data-ttu-id="d1579-203">Im Beispiel [Zuweisen einer statischen IP-Adresse](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) (VBScript) werden die IP-Adresse und das Gateway eines Computers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d1579-203">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript sample sets the IP address and gateway of a computer.</span></span>

<span data-ttu-id="d1579-204">Die [statische IP-Adresse und die anschließende Verknüpfung mit einem Domänen-](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell-Beispiel unterstützt die Neuerstellung von</span><span class="sxs-lookup"><span data-stu-id="d1579-204">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell sample assists in rebuilding machines.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1579-205">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1579-205">Requirements</span></span>



| <span data-ttu-id="d1579-206">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1579-206">Requirement</span></span> | <span data-ttu-id="d1579-207">Wert</span><span class="sxs-lookup"><span data-stu-id="d1579-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1579-208">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1579-208">Minimum supported client</span></span><br/> | <span data-ttu-id="d1579-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1579-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1579-210">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1579-210">Minimum supported server</span></span><br/> | <span data-ttu-id="d1579-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1579-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1579-212">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1579-212">Namespace</span></span><br/>                | <span data-ttu-id="d1579-213">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1579-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1579-214">MOF</span><span class="sxs-lookup"><span data-stu-id="d1579-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1579-215"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1579-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1579-216">DLL</span><span class="sxs-lookup"><span data-stu-id="d1579-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1579-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1579-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1579-218">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1579-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1579-219">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="d1579-219">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d1579-220">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="d1579-220">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d1579-221">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d1579-221">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d1579-222">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="d1579-222">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d1579-223">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="d1579-223">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

