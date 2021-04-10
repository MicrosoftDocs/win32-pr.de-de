---
description: Die WMI-Klassenmethode SetDNSDomain ermöglicht die Einstellung der DNS-Domäne.
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: SetDNSDomain-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c440d8cb5c720bf6922707f04bc75e2383755c1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214250"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="19355-103">SetDNSDomain-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="19355-103">SetDNSDomain method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="19355-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetDNSDomain** ermöglicht die Einstellung der DNS-Domäne.</span><span class="sxs-lookup"><span data-stu-id="19355-104">The **SetDNSDomain** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows for the setting of the DNS domain.</span></span>

<span data-ttu-id="19355-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="19355-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="19355-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="19355-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="19355-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="19355-107">Syntax</span></span>


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a><span data-ttu-id="19355-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19355-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19355-109">*DNSDomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19355-109">*DNSDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19355-110">Domäne, der der DNS zugeordnet ist, dargestellt durch einen Organisationsnamen, gefolgt von einem Zeitraum und einer Erweiterung, die den Typ der Organisation angibt.</span><span class="sxs-lookup"><span data-stu-id="19355-110">Domain with which the DNS is associated, represented by an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="19355-111">Beispiel: "Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="19355-111">Example: "microsoft.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19355-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19355-112">Return value</span></span>

<span data-ttu-id="19355-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="19355-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required and a different number if there is an error.</span></span> <span data-ttu-id="19355-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="19355-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="19355-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="19355-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="19355-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="19355-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="19355-117">0</span><span class="sxs-lookup"><span data-stu-id="19355-117">0</span></span>

<span data-ttu-id="19355-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19355-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="19355-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="19355-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="19355-120">1</span><span class="sxs-lookup"><span data-stu-id="19355-120">1</span></span>

<span data-ttu-id="19355-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19355-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="19355-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="19355-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="19355-123">64</span><span class="sxs-lookup"><span data-stu-id="19355-123">64</span></span>

<span data-ttu-id="19355-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19355-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="19355-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="19355-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="19355-126">65</span><span class="sxs-lookup"><span data-stu-id="19355-126">65</span></span>

<span data-ttu-id="19355-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="19355-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="19355-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="19355-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="19355-129">66</span><span class="sxs-lookup"><span data-stu-id="19355-129">66</span></span>

<span data-ttu-id="19355-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="19355-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="19355-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="19355-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="19355-132">67</span><span class="sxs-lookup"><span data-stu-id="19355-132">67</span></span>

<span data-ttu-id="19355-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="19355-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="19355-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="19355-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="19355-135">68</span><span class="sxs-lookup"><span data-stu-id="19355-135">68</span></span>

<span data-ttu-id="19355-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="19355-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="19355-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="19355-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="19355-138">69</span><span class="sxs-lookup"><span data-stu-id="19355-138">69</span></span>

<span data-ttu-id="19355-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="19355-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="19355-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="19355-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="19355-141">70</span><span class="sxs-lookup"><span data-stu-id="19355-141">70</span></span>

<span data-ttu-id="19355-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="19355-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="19355-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="19355-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="19355-144">71</span><span class="sxs-lookup"><span data-stu-id="19355-144">71</span></span>

<span data-ttu-id="19355-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="19355-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="19355-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="19355-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="19355-147">72</span><span class="sxs-lookup"><span data-stu-id="19355-147">72</span></span>

<span data-ttu-id="19355-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="19355-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="19355-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="19355-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="19355-150">73</span><span class="sxs-lookup"><span data-stu-id="19355-150">73</span></span>

<span data-ttu-id="19355-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="19355-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="19355-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="19355-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="19355-153">74</span><span class="sxs-lookup"><span data-stu-id="19355-153">74</span></span>

<span data-ttu-id="19355-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="19355-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="19355-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="19355-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="19355-156">75</span><span class="sxs-lookup"><span data-stu-id="19355-156">75</span></span>

<span data-ttu-id="19355-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="19355-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="19355-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="19355-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="19355-159">76</span><span class="sxs-lookup"><span data-stu-id="19355-159">76</span></span>

<span data-ttu-id="19355-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="19355-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="19355-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="19355-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="19355-162">77</span><span class="sxs-lookup"><span data-stu-id="19355-162">77</span></span>

<span data-ttu-id="19355-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="19355-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="19355-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="19355-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="19355-165">78</span><span class="sxs-lookup"><span data-stu-id="19355-165">78</span></span>

<span data-ttu-id="19355-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="19355-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="19355-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="19355-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="19355-168">79</span><span class="sxs-lookup"><span data-stu-id="19355-168">79</span></span>

<span data-ttu-id="19355-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="19355-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="19355-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="19355-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="19355-171">80</span><span class="sxs-lookup"><span data-stu-id="19355-171">80</span></span>

<span data-ttu-id="19355-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="19355-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="19355-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="19355-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="19355-174">81</span><span class="sxs-lookup"><span data-stu-id="19355-174">81</span></span>

<span data-ttu-id="19355-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="19355-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="19355-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="19355-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="19355-177">82</span><span class="sxs-lookup"><span data-stu-id="19355-177">82</span></span>

<span data-ttu-id="19355-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="19355-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="19355-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="19355-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="19355-180">83</span><span class="sxs-lookup"><span data-stu-id="19355-180">83</span></span>

<span data-ttu-id="19355-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19355-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="19355-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="19355-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="19355-183">84</span><span class="sxs-lookup"><span data-stu-id="19355-183">84</span></span>

<span data-ttu-id="19355-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19355-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="19355-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="19355-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="19355-186">85</span><span class="sxs-lookup"><span data-stu-id="19355-186">85</span></span>

<span data-ttu-id="19355-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19355-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="19355-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="19355-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="19355-189">86</span><span class="sxs-lookup"><span data-stu-id="19355-189">86</span></span>

<span data-ttu-id="19355-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="19355-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="19355-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="19355-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="19355-192">87</span><span class="sxs-lookup"><span data-stu-id="19355-192">87</span></span>

<span data-ttu-id="19355-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="19355-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="19355-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="19355-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="19355-195">88</span><span class="sxs-lookup"><span data-stu-id="19355-195">88</span></span>

<span data-ttu-id="19355-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="19355-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="19355-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="19355-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="19355-198">89</span><span class="sxs-lookup"><span data-stu-id="19355-198">89</span></span>

<span data-ttu-id="19355-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="19355-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="19355-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="19355-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="19355-201">90</span><span class="sxs-lookup"><span data-stu-id="19355-201">90</span></span>

<span data-ttu-id="19355-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="19355-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="19355-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="19355-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="19355-204">91</span><span class="sxs-lookup"><span data-stu-id="19355-204">91</span></span>

<span data-ttu-id="19355-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="19355-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="19355-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="19355-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="19355-207">92</span><span class="sxs-lookup"><span data-stu-id="19355-207">92</span></span>

<span data-ttu-id="19355-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="19355-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="19355-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="19355-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="19355-210">93</span><span class="sxs-lookup"><span data-stu-id="19355-210">93</span></span>

<span data-ttu-id="19355-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="19355-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="19355-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="19355-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="19355-213">94</span><span class="sxs-lookup"><span data-stu-id="19355-213">94</span></span>

<span data-ttu-id="19355-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="19355-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="19355-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="19355-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="19355-216">95</span><span class="sxs-lookup"><span data-stu-id="19355-216">95</span></span>

<span data-ttu-id="19355-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="19355-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="19355-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="19355-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="19355-219">96</span><span class="sxs-lookup"><span data-stu-id="19355-219">96</span></span>

<span data-ttu-id="19355-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="19355-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="19355-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="19355-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="19355-222">97</span><span class="sxs-lookup"><span data-stu-id="19355-222">97</span></span>

<span data-ttu-id="19355-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="19355-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="19355-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="19355-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="19355-225">98</span><span class="sxs-lookup"><span data-stu-id="19355-225">98</span></span>

<span data-ttu-id="19355-226">Nicht alle DHCP-Leases können freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="19355-226">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="19355-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="19355-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="19355-228">100</span><span class="sxs-lookup"><span data-stu-id="19355-228">100</span></span>

<span data-ttu-id="19355-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19355-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="19355-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="19355-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="19355-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="19355-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19355-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19355-232">Remarks</span></span>

<span data-ttu-id="19355-233">Dabei handelt es sich um einen instanzabhängigen Methoden Aufrufwert, der pro Adapter angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="19355-233">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="19355-234">Die Einstellung gilt für den Ziel Adapter.</span><span class="sxs-lookup"><span data-stu-id="19355-234">The setting applies to the targeted adapter.</span></span>

## <a name="examples"></a><span data-ttu-id="19355-235">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19355-235">Examples</span></span>

<span data-ttu-id="19355-236">Das Codebeispiel [Zuweisen der DNS-Domäne für einen Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript in der TechNet Gallery verwendet **SetDNSDomain** , um die DNS-Domäne für einen TCP/IP-gebundenen Netzwerk Adapter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="19355-236">The [Assign the DNS Domain for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript code sample on TechNet gallery uses **SetDNSDomain** to set the DNS domain for a TCP/IP-bound network adapter.</span></span>

<span data-ttu-id="19355-237">Das Codebeispiel zum [Ändern der TCP/IP-Konfiguration für einen Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) mit VBScript in der TechNet Gallery verwendet **SetDNSDomain** zum Ändern der TCP/IP-Einstellungen für einen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="19355-237">The [Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript code sample on TechNet Gallery uses **SetDNSDomain** to modify TCP/IP settings for a network adapter.</span></span>

<span data-ttu-id="19355-238">Das Beispiel [Enable DHCP settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript in der TechNet Gallery verwendet **SetDNSDomain** , um alle Einstellungen zu konfigurieren, die in der Regel zum Aktivieren von DHCP auf einem Computer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="19355-238">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample on TechNet Gallery uses **SetDNSDomain** to configure all the settings typically required to enable DHCP on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="19355-239">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19355-239">Requirements</span></span>



| <span data-ttu-id="19355-240">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19355-240">Requirement</span></span> | <span data-ttu-id="19355-241">Wert</span><span class="sxs-lookup"><span data-stu-id="19355-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19355-242">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19355-242">Minimum supported client</span></span><br/> | <span data-ttu-id="19355-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19355-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19355-244">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19355-244">Minimum supported server</span></span><br/> | <span data-ttu-id="19355-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19355-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19355-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="19355-246">Namespace</span></span><br/>                | <span data-ttu-id="19355-247">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19355-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19355-248">MOF</span><span class="sxs-lookup"><span data-stu-id="19355-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19355-249"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19355-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19355-250">DLL</span><span class="sxs-lookup"><span data-stu-id="19355-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19355-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19355-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19355-252">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19355-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19355-253">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="19355-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="19355-254">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="19355-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="19355-255">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="19355-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="19355-256">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="19355-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="19355-257">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="19355-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

