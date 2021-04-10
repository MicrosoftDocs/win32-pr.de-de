---
description: Die Methode "erneutem WMI" erneuert die IP-Adresse auf bestimmten DHCP-fähigen Netzwerkadaptern.
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Erneuerdhcplease-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041532"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ad869-103">Erneuerdhcplease-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad869-103">RenewDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ad869-104">Die Methode " **erneutem** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) " erneuert die IP-Adresse auf bestimmten DHCP-fähigen Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="ad869-104">The **RenewDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renews the IP address on specific DHCP-enabled network adapters.</span></span>

<span data-ttu-id="ad869-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad869-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ad869-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ad869-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad869-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad869-107">Syntax</span></span>


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="ad869-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad869-108">Parameters</span></span>

<span data-ttu-id="ad869-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ad869-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad869-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad869-110">Return value</span></span>

<span data-ttu-id="ad869-111">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ad869-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="ad869-112">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ad869-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ad869-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ad869-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ad869-114">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ad869-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-115">0</span><span class="sxs-lookup"><span data-stu-id="ad869-115">0</span></span>

<span data-ttu-id="ad869-116">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad869-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-117">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ad869-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-118">1</span><span class="sxs-lookup"><span data-stu-id="ad869-118">1</span></span>

<span data-ttu-id="ad869-119">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad869-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-120">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="ad869-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-121">64</span><span class="sxs-lookup"><span data-stu-id="ad869-121">64</span></span>

<span data-ttu-id="ad869-122">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad869-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-123">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="ad869-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-124">65</span><span class="sxs-lookup"><span data-stu-id="ad869-124">65</span></span>

<span data-ttu-id="ad869-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ad869-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-126">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="ad869-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-127">66</span><span class="sxs-lookup"><span data-stu-id="ad869-127">66</span></span>

<span data-ttu-id="ad869-128">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="ad869-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-129">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="ad869-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-130">67</span><span class="sxs-lookup"><span data-stu-id="ad869-130">67</span></span>

<span data-ttu-id="ad869-131">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ad869-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-132">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="ad869-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-133">68</span><span class="sxs-lookup"><span data-stu-id="ad869-133">68</span></span>

<span data-ttu-id="ad869-134">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="ad869-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-135">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="ad869-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-136">69</span><span class="sxs-lookup"><span data-stu-id="ad869-136">69</span></span>

<span data-ttu-id="ad869-137">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="ad869-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-138">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="ad869-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-139">70</span><span class="sxs-lookup"><span data-stu-id="ad869-139">70</span></span>

<span data-ttu-id="ad869-140">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ad869-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-141">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="ad869-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-142">71</span><span class="sxs-lookup"><span data-stu-id="ad869-142">71</span></span>

<span data-ttu-id="ad869-143">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ad869-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-144">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="ad869-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-145">72</span><span class="sxs-lookup"><span data-stu-id="ad869-145">72</span></span>

<span data-ttu-id="ad869-146">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="ad869-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-147">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="ad869-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-148">73</span><span class="sxs-lookup"><span data-stu-id="ad869-148">73</span></span>

<span data-ttu-id="ad869-149">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="ad869-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-150">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="ad869-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-151">74</span><span class="sxs-lookup"><span data-stu-id="ad869-151">74</span></span>

<span data-ttu-id="ad869-152">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="ad869-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-153">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="ad869-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-154">75</span><span class="sxs-lookup"><span data-stu-id="ad869-154">75</span></span>

<span data-ttu-id="ad869-155">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="ad869-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-156">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="ad869-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-157">76</span><span class="sxs-lookup"><span data-stu-id="ad869-157">76</span></span>

<span data-ttu-id="ad869-158">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="ad869-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-159">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="ad869-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-160">77</span><span class="sxs-lookup"><span data-stu-id="ad869-160">77</span></span>

<span data-ttu-id="ad869-161">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="ad869-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-162">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="ad869-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-163">78</span><span class="sxs-lookup"><span data-stu-id="ad869-163">78</span></span>

<span data-ttu-id="ad869-164">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="ad869-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-165">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="ad869-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-166">79</span><span class="sxs-lookup"><span data-stu-id="ad869-166">79</span></span>

<span data-ttu-id="ad869-167">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="ad869-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-168">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-169">80</span><span class="sxs-lookup"><span data-stu-id="ad869-169">80</span></span>

<span data-ttu-id="ad869-170">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ad869-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-171">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-172">81</span><span class="sxs-lookup"><span data-stu-id="ad869-172">81</span></span>

<span data-ttu-id="ad869-173">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ad869-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-174">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-175">82</span><span class="sxs-lookup"><span data-stu-id="ad869-175">82</span></span>

<span data-ttu-id="ad869-176">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="ad869-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-177">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="ad869-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-178">83</span><span class="sxs-lookup"><span data-stu-id="ad869-178">83</span></span>

<span data-ttu-id="ad869-179">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad869-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-180">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ad869-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-181">84</span><span class="sxs-lookup"><span data-stu-id="ad869-181">84</span></span>

<span data-ttu-id="ad869-182">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ad869-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-183">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ad869-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-184">85</span><span class="sxs-lookup"><span data-stu-id="ad869-184">85</span></span>

<span data-ttu-id="ad869-185">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ad869-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-186">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="ad869-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-187">86</span><span class="sxs-lookup"><span data-stu-id="ad869-187">86</span></span>

<span data-ttu-id="ad869-188">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="ad869-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-189">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="ad869-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-190">87</span><span class="sxs-lookup"><span data-stu-id="ad869-190">87</span></span>

<span data-ttu-id="ad869-191">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="ad869-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-192">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="ad869-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-193">88</span><span class="sxs-lookup"><span data-stu-id="ad869-193">88</span></span>

<span data-ttu-id="ad869-194">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="ad869-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-195">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="ad869-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-196">89</span><span class="sxs-lookup"><span data-stu-id="ad869-196">89</span></span>

<span data-ttu-id="ad869-197">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="ad869-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-198">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="ad869-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-199">90</span><span class="sxs-lookup"><span data-stu-id="ad869-199">90</span></span>

<span data-ttu-id="ad869-200">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="ad869-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-201">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="ad869-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-202">91</span><span class="sxs-lookup"><span data-stu-id="ad869-202">91</span></span>

<span data-ttu-id="ad869-203">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="ad869-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-204">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="ad869-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-205">92</span><span class="sxs-lookup"><span data-stu-id="ad869-205">92</span></span>

<span data-ttu-id="ad869-206">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ad869-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-207">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-208">93</span><span class="sxs-lookup"><span data-stu-id="ad869-208">93</span></span>

<span data-ttu-id="ad869-209">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ad869-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-210">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-211">94</span><span class="sxs-lookup"><span data-stu-id="ad869-211">94</span></span>

<span data-ttu-id="ad869-212">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ad869-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-213">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-214">95</span><span class="sxs-lookup"><span data-stu-id="ad869-214">95</span></span>

<span data-ttu-id="ad869-215">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad869-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-216">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-217">96</span><span class="sxs-lookup"><span data-stu-id="ad869-217">96</span></span>

<span data-ttu-id="ad869-218">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad869-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-219">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="ad869-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-220">97</span><span class="sxs-lookup"><span data-stu-id="ad869-220">97</span></span>

<span data-ttu-id="ad869-221">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="ad869-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-222">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="ad869-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-223">98</span><span class="sxs-lookup"><span data-stu-id="ad869-223">98</span></span>

<span data-ttu-id="ad869-224">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="ad869-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-225">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ad869-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-226">100</span><span class="sxs-lookup"><span data-stu-id="ad869-226">100</span></span>

<span data-ttu-id="ad869-227">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ad869-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ad869-228">**Andere**</span><span class="sxs-lookup"><span data-stu-id="ad869-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ad869-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ad869-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad869-230">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad869-230">Remarks</span></span>

<span data-ttu-id="ad869-231">Die Lease für die von einem DHCP-Server zugewiesene IP-Adresse weist ein Ablaufdatum auf, das der Client erneuern muss, wenn die zugewiesene IP-Adresse weiterhin verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad869-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="ad869-232">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad869-232">Examples</span></span>

<span data-ttu-id="ad869-233">[Mit dem PowerShell-Beispiel "Release Renew IP Adresses using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell" in der TechNet Gallery wird die IP-Adresse mit " **erneuerdhcplease** " freigegeben und erneuert</span><span class="sxs-lookup"><span data-stu-id="ad869-233">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **RenewDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="ad869-234">Das Beispiel zum [Erneuern der DHCP-Lease für ein Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript in der TechNet Gallery verwendet **erneuerdhcplease** zum Erneuern der DHCP-Lease für jeden TCP/IP-gebundenen Netzwerkadapter in einem Computer.</span><span class="sxs-lookup"><span data-stu-id="ad869-234">The [Renew the DHCP Lease for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript sample on TechNet Gallery uses **RenewDHCPLease** to renew the DHCP lease for each TCP/IP-bound network adapter in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad869-235">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad869-235">Requirements</span></span>



| <span data-ttu-id="ad869-236">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad869-236">Requirement</span></span> | <span data-ttu-id="ad869-237">Wert</span><span class="sxs-lookup"><span data-stu-id="ad869-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad869-238">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad869-238">Minimum supported client</span></span><br/> | <span data-ttu-id="ad869-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad869-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad869-240">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad869-240">Minimum supported server</span></span><br/> | <span data-ttu-id="ad869-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad869-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad869-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad869-242">Namespace</span></span><br/>                | <span data-ttu-id="ad869-243">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ad869-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad869-244">MOF</span><span class="sxs-lookup"><span data-stu-id="ad869-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad869-245"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ad869-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad869-246">DLL</span><span class="sxs-lookup"><span data-stu-id="ad869-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad869-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad869-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad869-248">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad869-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad869-249">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="ad869-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ad869-250">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="ad869-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ad869-251">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ad869-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ad869-252">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="ad869-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ad869-253">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="ad869-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

