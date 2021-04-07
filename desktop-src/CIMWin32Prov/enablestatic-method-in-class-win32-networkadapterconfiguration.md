---
description: Die EnableStatic-WMI-Klassenmethode ermöglicht die statische TCP/IP-Adressierung für den Zielnetzwerk Adapter. Das Ergebnis ist, dass DHCP für diesen Netzwerkadapter deaktiviert ist.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: EnableStatic-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748144"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="19cd5-104">EnableStatic-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="19cd5-104">EnableStatic method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="19cd5-105">Die **EnableStatic** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode ermöglicht die statische TCP/IP-Adressierung für den Zielnetzwerk Adapter.</span><span class="sxs-lookup"><span data-stu-id="19cd5-105">The **EnableStatic** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables static TCP/IP addressing for the target network adapter.</span></span> <span data-ttu-id="19cd5-106">Das Ergebnis ist, dass DHCP für diesen Netzwerkadapter deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="19cd5-106">As a result, DHCP for this network adapter is disabled.</span></span>

<span data-ttu-id="19cd5-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="19cd5-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="19cd5-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="19cd5-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="19cd5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19cd5-109">Syntax</span></span>


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a><span data-ttu-id="19cd5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19cd5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cd5-111">*IPAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19cd5-111">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-112">Listet alle statischen IP-Adressen für den aktuellen Netzwerkadapter auf.</span><span class="sxs-lookup"><span data-stu-id="19cd5-112">Lists all of the static IP addresses for the current network adapter.</span></span>

<span data-ttu-id="19cd5-113">Beispiel: 155.34.22.0.</span><span class="sxs-lookup"><span data-stu-id="19cd5-113">Example: 155.34.22.0.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-114">*Subnetzmaske* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19cd5-114">*SubnetMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-115">Subnetzmasken, die die Werte im *IPAddress* -Parameter ergänzen.</span><span class="sxs-lookup"><span data-stu-id="19cd5-115">Subnet masks that complement the values in the *IPAddress* parameter.</span></span>

<span data-ttu-id="19cd5-116">Beispiel: 255.255.0.0.</span><span class="sxs-lookup"><span data-stu-id="19cd5-116">Example: 255.255.0.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cd5-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19cd5-117">Return value</span></span>

<span data-ttu-id="19cd5-118">Gibt einen Wert von 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und jede andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="19cd5-118">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="19cd5-119">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="19cd5-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="19cd5-120">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="19cd5-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="19cd5-121">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="19cd5-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-122">0</span><span class="sxs-lookup"><span data-stu-id="19cd5-122">0</span></span>

<span data-ttu-id="19cd5-123">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19cd5-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-124">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="19cd5-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-125">1</span><span class="sxs-lookup"><span data-stu-id="19cd5-125">1</span></span>

<span data-ttu-id="19cd5-126">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19cd5-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-127">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-128">64</span><span class="sxs-lookup"><span data-stu-id="19cd5-128">64</span></span>

<span data-ttu-id="19cd5-129">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19cd5-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-130">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-131">65</span><span class="sxs-lookup"><span data-stu-id="19cd5-131">65</span></span>

<span data-ttu-id="19cd5-132">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="19cd5-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-133">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-134">66</span><span class="sxs-lookup"><span data-stu-id="19cd5-134">66</span></span>

<span data-ttu-id="19cd5-135">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="19cd5-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-136">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-137">67</span><span class="sxs-lookup"><span data-stu-id="19cd5-137">67</span></span>

<span data-ttu-id="19cd5-138">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="19cd5-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-139">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="19cd5-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-140">68</span><span class="sxs-lookup"><span data-stu-id="19cd5-140">68</span></span>

<span data-ttu-id="19cd5-141">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="19cd5-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-142">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-143">69</span><span class="sxs-lookup"><span data-stu-id="19cd5-143">69</span></span>

<span data-ttu-id="19cd5-144">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="19cd5-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-145">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="19cd5-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-146">70</span><span class="sxs-lookup"><span data-stu-id="19cd5-146">70</span></span>

<span data-ttu-id="19cd5-147">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="19cd5-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-148">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="19cd5-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-149">71</span><span class="sxs-lookup"><span data-stu-id="19cd5-149">71</span></span>

<span data-ttu-id="19cd5-150">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="19cd5-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-151">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-152">72</span><span class="sxs-lookup"><span data-stu-id="19cd5-152">72</span></span>

<span data-ttu-id="19cd5-153">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="19cd5-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-154">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="19cd5-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-155">73</span><span class="sxs-lookup"><span data-stu-id="19cd5-155">73</span></span>

<span data-ttu-id="19cd5-156">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="19cd5-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-157">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="19cd5-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-158">74</span><span class="sxs-lookup"><span data-stu-id="19cd5-158">74</span></span>

<span data-ttu-id="19cd5-159">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="19cd5-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-160">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-161">75</span><span class="sxs-lookup"><span data-stu-id="19cd5-161">75</span></span>

<span data-ttu-id="19cd5-162">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="19cd5-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-163">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="19cd5-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-164">76</span><span class="sxs-lookup"><span data-stu-id="19cd5-164">76</span></span>

<span data-ttu-id="19cd5-165">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="19cd5-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-166">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-167">77</span><span class="sxs-lookup"><span data-stu-id="19cd5-167">77</span></span>

<span data-ttu-id="19cd5-168">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="19cd5-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-169">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="19cd5-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-170">78</span><span class="sxs-lookup"><span data-stu-id="19cd5-170">78</span></span>

<span data-ttu-id="19cd5-171">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="19cd5-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-172">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="19cd5-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-173">79</span><span class="sxs-lookup"><span data-stu-id="19cd5-173">79</span></span>

<span data-ttu-id="19cd5-174">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="19cd5-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-175">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-176">80</span><span class="sxs-lookup"><span data-stu-id="19cd5-176">80</span></span>

<span data-ttu-id="19cd5-177">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-178">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-179">81</span><span class="sxs-lookup"><span data-stu-id="19cd5-179">81</span></span>

<span data-ttu-id="19cd5-180">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-180">Unable to configure DHCP service.</span></span> <span data-ttu-id="19cd5-181">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="19cd5-181">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-182">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-183">82</span><span class="sxs-lookup"><span data-stu-id="19cd5-183">82</span></span>

<span data-ttu-id="19cd5-184">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-185">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="19cd5-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-186">83</span><span class="sxs-lookup"><span data-stu-id="19cd5-186">83</span></span>

<span data-ttu-id="19cd5-187">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-188">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-189">84</span><span class="sxs-lookup"><span data-stu-id="19cd5-189">84</span></span>

<span data-ttu-id="19cd5-190">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19cd5-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-191">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-192">85</span><span class="sxs-lookup"><span data-stu-id="19cd5-192">85</span></span>

<span data-ttu-id="19cd5-193">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19cd5-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-194">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-195">86</span><span class="sxs-lookup"><span data-stu-id="19cd5-195">86</span></span>

<span data-ttu-id="19cd5-196">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="19cd5-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-197">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="19cd5-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-198">87</span><span class="sxs-lookup"><span data-stu-id="19cd5-198">87</span></span>

<span data-ttu-id="19cd5-199">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="19cd5-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-200">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="19cd5-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-201">88</span><span class="sxs-lookup"><span data-stu-id="19cd5-201">88</span></span>

<span data-ttu-id="19cd5-202">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="19cd5-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-203">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="19cd5-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-204">89</span><span class="sxs-lookup"><span data-stu-id="19cd5-204">89</span></span>

<span data-ttu-id="19cd5-205">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="19cd5-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-206">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="19cd5-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-207">90</span><span class="sxs-lookup"><span data-stu-id="19cd5-207">90</span></span>

<span data-ttu-id="19cd5-208">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="19cd5-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-209">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="19cd5-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-210">91</span><span class="sxs-lookup"><span data-stu-id="19cd5-210">91</span></span>

<span data-ttu-id="19cd5-211">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="19cd5-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-212">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="19cd5-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-213">92</span><span class="sxs-lookup"><span data-stu-id="19cd5-213">92</span></span>

<span data-ttu-id="19cd5-214">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="19cd5-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-215">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-216">93</span><span class="sxs-lookup"><span data-stu-id="19cd5-216">93</span></span>

<span data-ttu-id="19cd5-217">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-218">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-219">94</span><span class="sxs-lookup"><span data-stu-id="19cd5-219">94</span></span>

<span data-ttu-id="19cd5-220">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-221">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-222">95</span><span class="sxs-lookup"><span data-stu-id="19cd5-222">95</span></span>

<span data-ttu-id="19cd5-223">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-224">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-225">96</span><span class="sxs-lookup"><span data-stu-id="19cd5-225">96</span></span>

<span data-ttu-id="19cd5-226">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-227">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="19cd5-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-228">97</span><span class="sxs-lookup"><span data-stu-id="19cd5-228">97</span></span>

<span data-ttu-id="19cd5-229">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="19cd5-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-230">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-231">98</span><span class="sxs-lookup"><span data-stu-id="19cd5-231">98</span></span>

<span data-ttu-id="19cd5-232">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-233">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="19cd5-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-234">100</span><span class="sxs-lookup"><span data-stu-id="19cd5-234">100</span></span>

<span data-ttu-id="19cd5-235">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19cd5-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-236">**2147786788**</span><span class="sxs-lookup"><span data-stu-id="19cd5-236">**2147786788**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-237">Die Schreibsperre ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19cd5-237">Write lock not enabled.</span></span> <span data-ttu-id="19cd5-238">Weitere Informationen finden Sie unter [**inetcfglock:: acquirewrite telock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19cd5-238">For more information, see [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="19cd5-239">**Andere**</span><span class="sxs-lookup"><span data-stu-id="19cd5-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="19cd5-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="19cd5-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19cd5-241">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19cd5-241">Remarks</span></span>

<span data-ttu-id="19cd5-242">Wenn Sie **EnableStatic** zum Ändern der IP-Adresse des Remote Computers verwenden, während diese über diesen Adapter verbunden ist, ist die Verbindung mit dem Remote Computer wahrscheinlich nicht mehr möglich, und es wird eine Fehlermeldung zur RPC-Fehlermeldung empfangen.</span><span class="sxs-lookup"><span data-stu-id="19cd5-242">When using **EnableStatic** to change the IP address of the remote computer, while being connected through that adapter, you will likely loose connection to the remote computer, and receive an RPC not available error-message.</span></span> <span data-ttu-id="19cd5-243">(die Einstellungen werden jedoch geändert).</span><span class="sxs-lookup"><span data-stu-id="19cd5-243">(the settings are changed however).</span></span> <span data-ttu-id="19cd5-244">Um dieses Szenario zu vermeiden, sollten Sie die Gateway-und/oder DNS-Einstellungen ändern, bevor Sie die IP-Adresse des Adapters festlegen.</span><span class="sxs-lookup"><span data-stu-id="19cd5-244">To avoid this scenario, consider changing the Gateway and/or DNS-settings prior to setting the adapter's IP-address.</span></span>

<span data-ttu-id="19cd5-245">Wenn Sie mithilfe von **EnableStatic** einen Adapter mit einer statischen IP-Konfiguration versehen, gibt die Funktion den Wert "81-DHCP-Dienst kann nicht konfiguriert werden" zurück, wenn der Adapter bereits mit einer statischen Adresse konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="19cd5-245">When using **EnableStatic** to give an adapter a static IP configuration, the function returns an "81 - Unable to configure DHCP service" if the adapter is already configured with a static address.</span></span> <span data-ttu-id="19cd5-246">Die Funktion kann jedoch weiterhin mit dem neuen Vorgang festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-246">However, the function still succeeds in setting with the new operation.</span></span>

## <a name="examples"></a><span data-ttu-id="19cd5-247">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19cd5-247">Examples</span></span>

<span data-ttu-id="19cd5-248">Die [statische IP-Adresse und](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) die anschließende Verknüpfung mit einem PowerShell-Codebeispiel für eine Domäne in der TechNet Gallery verwendet **EnableStatic** zum Hinzufügen einer statischen IP-Adresse zu einem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="19cd5-248">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell code sample, on TechNet Gallery, uses **EnableStatic** to add a static IP to a local machine.</span></span>

<span data-ttu-id="19cd5-249">Im TechNet Gallery ( [Zuweisen einer statischen IP-Adresse](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript-Code) verwendet **EnableStatic** , um die IP-Adresse eines Computers festzulegen.</span><span class="sxs-lookup"><span data-stu-id="19cd5-249">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript code example, on TechNet Gallery, uses **EnableStatic** to set the IP address of a computer.</span></span>

<span data-ttu-id="19cd5-250">Das folgende VBScript-Beispiel veranschaulicht, wie die DHCP-Verwendung für eine Instanz von [**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md)deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="19cd5-250">The following VBScript sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="19cd5-251">In diesem Fall geben wir den Adapter mit einem Index von 0 an.</span><span class="sxs-lookup"><span data-stu-id="19cd5-251">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="19cd5-252">Der richtige Index sollte aus den Win32- \_ NetworkAdapter-Instanzen für andere Schnittstellen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-252">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="19cd5-253">Dieses Skript gilt nur für NT-basierte Systeme. ändern Sie die ipaddr-und subnetzvariablen unten zu den Werten, die Sie auf den Adapter anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="19cd5-253">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



<span data-ttu-id="19cd5-254">Das folgende perl-Beispiel veranschaulicht, wie die DHCP-Verwendung für eine Instanz von [**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md)deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="19cd5-254">The following Perl sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="19cd5-255">In diesem Fall geben wir den Adapter mit einem Index von 0 an.</span><span class="sxs-lookup"><span data-stu-id="19cd5-255">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="19cd5-256">Der richtige Index sollte aus den Win32- \_ NetworkAdapter-Instanzen für andere Schnittstellen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="19cd5-256">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="19cd5-257">Dieses Skript gilt nur für NT-basierte Systeme. ändern Sie die ipaddr-und subnetzvariablen unten zu den Werten, die Sie auf den Adapter anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="19cd5-257">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="19cd5-258">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19cd5-258">Requirements</span></span>



| <span data-ttu-id="19cd5-259">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19cd5-259">Requirement</span></span> | <span data-ttu-id="19cd5-260">Wert</span><span class="sxs-lookup"><span data-stu-id="19cd5-260">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19cd5-261">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19cd5-261">Minimum supported client</span></span><br/> | <span data-ttu-id="19cd5-262">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19cd5-262">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19cd5-263">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19cd5-263">Minimum supported server</span></span><br/> | <span data-ttu-id="19cd5-264">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19cd5-264">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19cd5-265">Namespace</span><span class="sxs-lookup"><span data-stu-id="19cd5-265">Namespace</span></span><br/>                | <span data-ttu-id="19cd5-266">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19cd5-266">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19cd5-267">MOF</span><span class="sxs-lookup"><span data-stu-id="19cd5-267">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19cd5-268"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19cd5-268"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19cd5-269">DLL</span><span class="sxs-lookup"><span data-stu-id="19cd5-269">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19cd5-270"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19cd5-270"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19cd5-271">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19cd5-271">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cd5-272">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="19cd5-272">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="19cd5-273">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="19cd5-273">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="19cd5-274">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="19cd5-274">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="19cd5-275">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="19cd5-275">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="19cd5-276">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="19cd5-276">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

