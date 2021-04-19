---
description: Die Methode DisableIPSec WMI-Klasse wird verwendet, um die Internet Protokoll Sicherheit (IPSec) auf diesem TCP/IP-fähigen Netzwerkadapter zu deaktivieren.
ms.assetid: 6fff2721-1ee2-42b4-bbf9-fd36b97318e3
ms.tgt_platform: multiple
title: DisableIPSec-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.DisableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b2a17bbfa0f10c08edb581b4a4bf51173facfea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342753"
---
# <a name="disableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d1391-103">DisableIPSec-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1391-103">DisableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d1391-104">Die Methode **DisableIPSec** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Internet Protokoll Sicherheit (IPSec) auf diesem TCP/IP-fähigen Netzwerkadapter zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1391-104">The **DisableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method is used to disable Internet Protocol security (IPsec) on this TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="d1391-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1391-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d1391-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d1391-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1391-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1391-107">Syntax</span></span>


```mof
uint32 DisableIPSec();
```



## <a name="parameters"></a><span data-ttu-id="d1391-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1391-108">Parameters</span></span>

<span data-ttu-id="d1391-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d1391-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1391-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1391-110">Return value</span></span>

<span data-ttu-id="d1391-111">Gibt einen Wert von 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und jede andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="d1391-111">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="d1391-112">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d1391-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d1391-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d1391-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d1391-114">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d1391-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-115">0</span><span class="sxs-lookup"><span data-stu-id="d1391-115">0</span></span>

<span data-ttu-id="d1391-116">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1391-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-117">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d1391-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-118">1</span><span class="sxs-lookup"><span data-stu-id="d1391-118">1</span></span>

<span data-ttu-id="d1391-119">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1391-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-120">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="d1391-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-121">64</span><span class="sxs-lookup"><span data-stu-id="d1391-121">64</span></span>

<span data-ttu-id="d1391-122">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1391-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-123">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d1391-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-124">65</span><span class="sxs-lookup"><span data-stu-id="d1391-124">65</span></span>

<span data-ttu-id="d1391-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d1391-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-126">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="d1391-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-127">66</span><span class="sxs-lookup"><span data-stu-id="d1391-127">66</span></span>

<span data-ttu-id="d1391-128">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="d1391-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-129">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="d1391-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-130">67</span><span class="sxs-lookup"><span data-stu-id="d1391-130">67</span></span>

<span data-ttu-id="d1391-131">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d1391-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-132">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="d1391-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-133">68</span><span class="sxs-lookup"><span data-stu-id="d1391-133">68</span></span>

<span data-ttu-id="d1391-134">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="d1391-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-135">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="d1391-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-136">69</span><span class="sxs-lookup"><span data-stu-id="d1391-136">69</span></span>

<span data-ttu-id="d1391-137">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1391-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-138">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="d1391-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-139">70</span><span class="sxs-lookup"><span data-stu-id="d1391-139">70</span></span>

<span data-ttu-id="d1391-140">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d1391-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-141">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="d1391-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-142">71</span><span class="sxs-lookup"><span data-stu-id="d1391-142">71</span></span>

<span data-ttu-id="d1391-143">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d1391-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-144">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="d1391-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-145">72</span><span class="sxs-lookup"><span data-stu-id="d1391-145">72</span></span>

<span data-ttu-id="d1391-146">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="d1391-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-147">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="d1391-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-148">73</span><span class="sxs-lookup"><span data-stu-id="d1391-148">73</span></span>

<span data-ttu-id="d1391-149">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="d1391-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-150">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="d1391-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-151">74</span><span class="sxs-lookup"><span data-stu-id="d1391-151">74</span></span>

<span data-ttu-id="d1391-152">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="d1391-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-153">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="d1391-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-154">75</span><span class="sxs-lookup"><span data-stu-id="d1391-154">75</span></span>

<span data-ttu-id="d1391-155">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="d1391-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-156">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="d1391-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-157">76</span><span class="sxs-lookup"><span data-stu-id="d1391-157">76</span></span>

<span data-ttu-id="d1391-158">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="d1391-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-159">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="d1391-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-160">77</span><span class="sxs-lookup"><span data-stu-id="d1391-160">77</span></span>

<span data-ttu-id="d1391-161">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="d1391-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-162">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="d1391-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-163">78</span><span class="sxs-lookup"><span data-stu-id="d1391-163">78</span></span>

<span data-ttu-id="d1391-164">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="d1391-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-165">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="d1391-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-166">79</span><span class="sxs-lookup"><span data-stu-id="d1391-166">79</span></span>

<span data-ttu-id="d1391-167">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="d1391-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-168">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-169">80</span><span class="sxs-lookup"><span data-stu-id="d1391-169">80</span></span>

<span data-ttu-id="d1391-170">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d1391-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-171">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-172">81</span><span class="sxs-lookup"><span data-stu-id="d1391-172">81</span></span>

<span data-ttu-id="d1391-173">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d1391-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-174">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-175">82</span><span class="sxs-lookup"><span data-stu-id="d1391-175">82</span></span>

<span data-ttu-id="d1391-176">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="d1391-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-177">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="d1391-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-178">83</span><span class="sxs-lookup"><span data-stu-id="d1391-178">83</span></span>

<span data-ttu-id="d1391-179">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1391-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-180">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="d1391-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-181">84</span><span class="sxs-lookup"><span data-stu-id="d1391-181">84</span></span>

<span data-ttu-id="d1391-182">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d1391-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-183">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="d1391-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-184">85</span><span class="sxs-lookup"><span data-stu-id="d1391-184">85</span></span>

<span data-ttu-id="d1391-185">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d1391-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-186">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="d1391-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-187">86</span><span class="sxs-lookup"><span data-stu-id="d1391-187">86</span></span>

<span data-ttu-id="d1391-188">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="d1391-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-189">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="d1391-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-190">87</span><span class="sxs-lookup"><span data-stu-id="d1391-190">87</span></span>

<span data-ttu-id="d1391-191">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="d1391-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-192">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="d1391-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-193">88</span><span class="sxs-lookup"><span data-stu-id="d1391-193">88</span></span>

<span data-ttu-id="d1391-194">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="d1391-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-195">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="d1391-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-196">89</span><span class="sxs-lookup"><span data-stu-id="d1391-196">89</span></span>

<span data-ttu-id="d1391-197">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="d1391-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-198">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="d1391-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-199">90</span><span class="sxs-lookup"><span data-stu-id="d1391-199">90</span></span>

<span data-ttu-id="d1391-200">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="d1391-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-201">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="d1391-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-202">91</span><span class="sxs-lookup"><span data-stu-id="d1391-202">91</span></span>

<span data-ttu-id="d1391-203">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="d1391-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-204">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="d1391-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-205">92</span><span class="sxs-lookup"><span data-stu-id="d1391-205">92</span></span>

<span data-ttu-id="d1391-206">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d1391-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-207">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-208">93</span><span class="sxs-lookup"><span data-stu-id="d1391-208">93</span></span>

<span data-ttu-id="d1391-209">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d1391-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-210">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-211">94</span><span class="sxs-lookup"><span data-stu-id="d1391-211">94</span></span>

<span data-ttu-id="d1391-212">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d1391-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-213">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-214">95</span><span class="sxs-lookup"><span data-stu-id="d1391-214">95</span></span>

<span data-ttu-id="d1391-215">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="d1391-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-216">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-217">96</span><span class="sxs-lookup"><span data-stu-id="d1391-217">96</span></span>

<span data-ttu-id="d1391-218">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="d1391-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-219">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="d1391-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-220">97</span><span class="sxs-lookup"><span data-stu-id="d1391-220">97</span></span>

<span data-ttu-id="d1391-221">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="d1391-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-222">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="d1391-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-223">98</span><span class="sxs-lookup"><span data-stu-id="d1391-223">98</span></span>

<span data-ttu-id="d1391-224">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="d1391-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-225">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="d1391-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-226">100</span><span class="sxs-lookup"><span data-stu-id="d1391-226">100</span></span>

<span data-ttu-id="d1391-227">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d1391-227">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d1391-228">**Andere**</span><span class="sxs-lookup"><span data-stu-id="d1391-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d1391-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d1391-229">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d1391-230">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1391-230">Examples</span></span>

<span data-ttu-id="d1391-231">Im folgenden VBScript-Beispiel wird die IP-Sicherheit auf einem Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d1391-231">The following VBScript sample disables the IP Security on a computer.</span></span> <span data-ttu-id="d1391-232">Beachten Sie, dass der tatsächliche Rückruf von disableipaus Sicherheitsgründen auskommentiert wird.</span><span class="sxs-lookup"><span data-stu-id="d1391-232">Note that the actual call to DisableIPSec is commented out, for safety purposes.</span></span>


```VB
strServer = "."

Set objWMI = GetObject("winmgmts:\\" & strServer & "\root\cimv2")

strWQL = "select * from Win32_NetworkAdapterConfiguration"
Set objInstances = objWMI.ExecQuery(strWQL,,48)

For Each objInstance in objInstances

 ' Uncomment next line to disable security
 ' intResult = objInstance.DisableIPSec

Next
```



## <a name="requirements"></a><span data-ttu-id="d1391-233">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1391-233">Requirements</span></span>



| <span data-ttu-id="d1391-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1391-234">Requirement</span></span> | <span data-ttu-id="d1391-235">Wert</span><span class="sxs-lookup"><span data-stu-id="d1391-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1391-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1391-236">Minimum supported client</span></span><br/> | <span data-ttu-id="d1391-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1391-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1391-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1391-238">Minimum supported server</span></span><br/> | <span data-ttu-id="d1391-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1391-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1391-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1391-240">Namespace</span></span><br/>                | <span data-ttu-id="d1391-241">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1391-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1391-242">MOF</span><span class="sxs-lookup"><span data-stu-id="d1391-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1391-243"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1391-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1391-244">DLL</span><span class="sxs-lookup"><span data-stu-id="d1391-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1391-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1391-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1391-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1391-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1391-247">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="d1391-247">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d1391-248">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="d1391-248">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d1391-249">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d1391-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d1391-250">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="d1391-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d1391-251">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="d1391-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

