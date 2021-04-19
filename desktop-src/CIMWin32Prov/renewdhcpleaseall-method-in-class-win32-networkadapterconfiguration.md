---
description: Mit der statischen Methode "erneuerdhcpleaseall" werden die IP-Adressen auf allen DHCP-fähigen Netzwerkadaptern erneuert.
ms.assetid: cbe0a607-cb3b-47c4-ad3a-c4fa03fe688c
ms.tgt_platform: multiple
title: Erneuerdhcpleaseall-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3ed94b44a629f619617186415ed3822387c6967
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346459"
---
# <a name="renewdhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9cc1a-103">Erneuerdhcpleaseall-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="9cc1a-103">RenewDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9cc1a-104">Mit [der statischen Methode](/windows/desktop/WmiSdk/retrieving-a-class) " **erneuerdhcpleaseall** " werden die IP-Adressen auf allen DHCP-fähigen Netzwerkadaptern erneuert.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-104">The **RenewDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method renews the IP addresses on all DHCP-enabled network adapters.</span></span>

<span data-ttu-id="9cc1a-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9cc1a-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9cc1a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc1a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cc1a-107">Syntax</span></span>


```mof
uint32 RenewDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="9cc1a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cc1a-108">Parameters</span></span>

<span data-ttu-id="9cc1a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9cc1a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cc1a-110">Return value</span></span>

<span data-ttu-id="9cc1a-111">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="9cc1a-112">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9cc1a-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9cc1a-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9cc1a-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9cc1a-114">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-115">0</span><span class="sxs-lookup"><span data-stu-id="9cc1a-115">0</span></span>

<span data-ttu-id="9cc1a-116">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-117">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-118">1</span><span class="sxs-lookup"><span data-stu-id="9cc1a-118">1</span></span>

<span data-ttu-id="9cc1a-119">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-120">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-121">64</span><span class="sxs-lookup"><span data-stu-id="9cc1a-121">64</span></span>

<span data-ttu-id="9cc1a-122">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-123">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-124">65</span><span class="sxs-lookup"><span data-stu-id="9cc1a-124">65</span></span>

<span data-ttu-id="9cc1a-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-126">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-127">66</span><span class="sxs-lookup"><span data-stu-id="9cc1a-127">66</span></span>

<span data-ttu-id="9cc1a-128">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-129">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-130">67</span><span class="sxs-lookup"><span data-stu-id="9cc1a-130">67</span></span>

<span data-ttu-id="9cc1a-131">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-132">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-133">68</span><span class="sxs-lookup"><span data-stu-id="9cc1a-133">68</span></span>

<span data-ttu-id="9cc1a-134">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-135">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-136">69</span><span class="sxs-lookup"><span data-stu-id="9cc1a-136">69</span></span>

<span data-ttu-id="9cc1a-137">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-138">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-139">70</span><span class="sxs-lookup"><span data-stu-id="9cc1a-139">70</span></span>

<span data-ttu-id="9cc1a-140">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-141">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-142">71</span><span class="sxs-lookup"><span data-stu-id="9cc1a-142">71</span></span>

<span data-ttu-id="9cc1a-143">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-144">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-145">72</span><span class="sxs-lookup"><span data-stu-id="9cc1a-145">72</span></span>

<span data-ttu-id="9cc1a-146">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-147">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-148">73</span><span class="sxs-lookup"><span data-stu-id="9cc1a-148">73</span></span>

<span data-ttu-id="9cc1a-149">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-150">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-151">74</span><span class="sxs-lookup"><span data-stu-id="9cc1a-151">74</span></span>

<span data-ttu-id="9cc1a-152">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-153">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-154">75</span><span class="sxs-lookup"><span data-stu-id="9cc1a-154">75</span></span>

<span data-ttu-id="9cc1a-155">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="9cc1a-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-156">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-157">76</span><span class="sxs-lookup"><span data-stu-id="9cc1a-157">76</span></span>

<span data-ttu-id="9cc1a-158">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-159">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-160">77</span><span class="sxs-lookup"><span data-stu-id="9cc1a-160">77</span></span>

<span data-ttu-id="9cc1a-161">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-162">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-163">78</span><span class="sxs-lookup"><span data-stu-id="9cc1a-163">78</span></span>

<span data-ttu-id="9cc1a-164">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-165">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-166">79</span><span class="sxs-lookup"><span data-stu-id="9cc1a-166">79</span></span>

<span data-ttu-id="9cc1a-167">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-168">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-169">80</span><span class="sxs-lookup"><span data-stu-id="9cc1a-169">80</span></span>

<span data-ttu-id="9cc1a-170">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-171">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-172">81</span><span class="sxs-lookup"><span data-stu-id="9cc1a-172">81</span></span>

<span data-ttu-id="9cc1a-173">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-174">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-175">82</span><span class="sxs-lookup"><span data-stu-id="9cc1a-175">82</span></span>

<span data-ttu-id="9cc1a-176">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-177">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-178">83</span><span class="sxs-lookup"><span data-stu-id="9cc1a-178">83</span></span>

<span data-ttu-id="9cc1a-179">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-180">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-181">84</span><span class="sxs-lookup"><span data-stu-id="9cc1a-181">84</span></span>

<span data-ttu-id="9cc1a-182">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-183">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-184">85</span><span class="sxs-lookup"><span data-stu-id="9cc1a-184">85</span></span>

<span data-ttu-id="9cc1a-185">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-186">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-187">86</span><span class="sxs-lookup"><span data-stu-id="9cc1a-187">86</span></span>

<span data-ttu-id="9cc1a-188">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-189">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-190">87</span><span class="sxs-lookup"><span data-stu-id="9cc1a-190">87</span></span>

<span data-ttu-id="9cc1a-191">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-192">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-193">88</span><span class="sxs-lookup"><span data-stu-id="9cc1a-193">88</span></span>

<span data-ttu-id="9cc1a-194">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-195">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-196">89</span><span class="sxs-lookup"><span data-stu-id="9cc1a-196">89</span></span>

<span data-ttu-id="9cc1a-197">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-198">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-199">90</span><span class="sxs-lookup"><span data-stu-id="9cc1a-199">90</span></span>

<span data-ttu-id="9cc1a-200">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-201">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-202">91</span><span class="sxs-lookup"><span data-stu-id="9cc1a-202">91</span></span>

<span data-ttu-id="9cc1a-203">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-204">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-205">92</span><span class="sxs-lookup"><span data-stu-id="9cc1a-205">92</span></span>

<span data-ttu-id="9cc1a-206">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-207">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-208">93</span><span class="sxs-lookup"><span data-stu-id="9cc1a-208">93</span></span>

<span data-ttu-id="9cc1a-209">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-210">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-211">94</span><span class="sxs-lookup"><span data-stu-id="9cc1a-211">94</span></span>

<span data-ttu-id="9cc1a-212">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-213">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-214">95</span><span class="sxs-lookup"><span data-stu-id="9cc1a-214">95</span></span>

<span data-ttu-id="9cc1a-215">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-216">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-217">96</span><span class="sxs-lookup"><span data-stu-id="9cc1a-217">96</span></span>

<span data-ttu-id="9cc1a-218">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-219">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-220">97</span><span class="sxs-lookup"><span data-stu-id="9cc1a-220">97</span></span>

<span data-ttu-id="9cc1a-221">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-222">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-223">98</span><span class="sxs-lookup"><span data-stu-id="9cc1a-223">98</span></span>

<span data-ttu-id="9cc1a-224">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-225">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-226">100</span><span class="sxs-lookup"><span data-stu-id="9cc1a-226">100</span></span>

<span data-ttu-id="9cc1a-227">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9cc1a-228">**Andere**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9cc1a-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9cc1a-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cc1a-230">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cc1a-230">Remarks</span></span>

<span data-ttu-id="9cc1a-231">Die Lease für die von einem DHCP-Server zugewiesene IP-Adresse weist ein Ablaufdatum auf, das der Client erneuern muss, wenn die zugewiesene IP-Adresse weiterhin verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="9cc1a-232">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cc1a-232">Examples</span></span>

<span data-ttu-id="9cc1a-233">Das Beispiel [Renew All DHCP Leases](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) VBScript in der TechNet Gallery erneuert alle DHCP-Leases, die zurzeit auf einem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9cc1a-233">The [Renew All DHCP Leases](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) VBScript example on TechNet Gallery renews all the DHCP leases currently in use on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc1a-234">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cc1a-234">Requirements</span></span>



| <span data-ttu-id="9cc1a-235">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cc1a-235">Requirement</span></span> | <span data-ttu-id="9cc1a-236">Wert</span><span class="sxs-lookup"><span data-stu-id="9cc1a-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc1a-237">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9cc1a-237">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc1a-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cc1a-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cc1a-239">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9cc1a-239">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc1a-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cc1a-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cc1a-241">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cc1a-241">Namespace</span></span><br/>                | <span data-ttu-id="9cc1a-242">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9cc1a-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9cc1a-243">MOF</span><span class="sxs-lookup"><span data-stu-id="9cc1a-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cc1a-244"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9cc1a-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cc1a-245">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc1a-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc1a-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cc1a-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc1a-247">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cc1a-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc1a-248">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9cc1a-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9cc1a-249">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="9cc1a-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9cc1a-250">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="9cc1a-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9cc1a-251">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="9cc1a-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9cc1a-252">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="9cc1a-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

