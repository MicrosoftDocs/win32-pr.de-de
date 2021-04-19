---
description: Die ReleaseDHCPLease WMI-Klassenmethode gibt die IP-Adresse frei, die an einen bestimmten DHCP-fähigen Netzwerkadapter gebunden ist.
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: ReleaseDHCPLease-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346033"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5852c-103">ReleaseDHCPLease-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="5852c-103">ReleaseDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5852c-104">Die **ReleaseDHCPLease** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode gibt die IP-Adresse frei, die an einen bestimmten DHCP-fähigen Netzwerkadapter gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="5852c-104">The **ReleaseDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method releases the IP address bound to a specific DHCP-enabled network adapter.</span></span>

<span data-ttu-id="5852c-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5852c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5852c-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5852c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5852c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5852c-107">Syntax</span></span>


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="5852c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5852c-108">Parameters</span></span>

<span data-ttu-id="5852c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5852c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5852c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5852c-110">Return value</span></span>

<span data-ttu-id="5852c-111">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="5852c-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="5852c-112">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5852c-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5852c-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5852c-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5852c-114">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5852c-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-115">0</span><span class="sxs-lookup"><span data-stu-id="5852c-115">0</span></span>

<span data-ttu-id="5852c-116">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5852c-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-117">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5852c-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-118">1</span><span class="sxs-lookup"><span data-stu-id="5852c-118">1</span></span>

<span data-ttu-id="5852c-119">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5852c-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-120">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="5852c-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-121">64</span><span class="sxs-lookup"><span data-stu-id="5852c-121">64</span></span>

<span data-ttu-id="5852c-122">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5852c-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-123">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="5852c-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-124">65</span><span class="sxs-lookup"><span data-stu-id="5852c-124">65</span></span>

<span data-ttu-id="5852c-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="5852c-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-126">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="5852c-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-127">66</span><span class="sxs-lookup"><span data-stu-id="5852c-127">66</span></span>

<span data-ttu-id="5852c-128">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="5852c-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-129">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="5852c-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-130">67</span><span class="sxs-lookup"><span data-stu-id="5852c-130">67</span></span>

<span data-ttu-id="5852c-131">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5852c-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-132">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="5852c-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-133">68</span><span class="sxs-lookup"><span data-stu-id="5852c-133">68</span></span>

<span data-ttu-id="5852c-134">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5852c-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-135">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="5852c-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-136">69</span><span class="sxs-lookup"><span data-stu-id="5852c-136">69</span></span>

<span data-ttu-id="5852c-137">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="5852c-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-138">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="5852c-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-139">70</span><span class="sxs-lookup"><span data-stu-id="5852c-139">70</span></span>

<span data-ttu-id="5852c-140">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5852c-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-141">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="5852c-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-142">71</span><span class="sxs-lookup"><span data-stu-id="5852c-142">71</span></span>

<span data-ttu-id="5852c-143">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5852c-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-144">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="5852c-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-145">72</span><span class="sxs-lookup"><span data-stu-id="5852c-145">72</span></span>

<span data-ttu-id="5852c-146">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="5852c-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-147">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="5852c-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-148">73</span><span class="sxs-lookup"><span data-stu-id="5852c-148">73</span></span>

<span data-ttu-id="5852c-149">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="5852c-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-150">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="5852c-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-151">74</span><span class="sxs-lookup"><span data-stu-id="5852c-151">74</span></span>

<span data-ttu-id="5852c-152">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="5852c-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-153">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="5852c-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-154">75</span><span class="sxs-lookup"><span data-stu-id="5852c-154">75</span></span>

<span data-ttu-id="5852c-155">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="5852c-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-156">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="5852c-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-157">76</span><span class="sxs-lookup"><span data-stu-id="5852c-157">76</span></span>

<span data-ttu-id="5852c-158">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="5852c-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-159">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="5852c-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-160">77</span><span class="sxs-lookup"><span data-stu-id="5852c-160">77</span></span>

<span data-ttu-id="5852c-161">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="5852c-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-162">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="5852c-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-163">78</span><span class="sxs-lookup"><span data-stu-id="5852c-163">78</span></span>

<span data-ttu-id="5852c-164">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="5852c-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-165">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="5852c-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-166">79</span><span class="sxs-lookup"><span data-stu-id="5852c-166">79</span></span>

<span data-ttu-id="5852c-167">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="5852c-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-168">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-169">80</span><span class="sxs-lookup"><span data-stu-id="5852c-169">80</span></span>

<span data-ttu-id="5852c-170">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5852c-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-171">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-172">81</span><span class="sxs-lookup"><span data-stu-id="5852c-172">81</span></span>

<span data-ttu-id="5852c-173">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5852c-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-174">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-175">82</span><span class="sxs-lookup"><span data-stu-id="5852c-175">82</span></span>

<span data-ttu-id="5852c-176">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="5852c-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-177">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="5852c-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-178">83</span><span class="sxs-lookup"><span data-stu-id="5852c-178">83</span></span>

<span data-ttu-id="5852c-179">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5852c-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-180">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5852c-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-181">84</span><span class="sxs-lookup"><span data-stu-id="5852c-181">84</span></span>

<span data-ttu-id="5852c-182">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5852c-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-183">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5852c-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-184">85</span><span class="sxs-lookup"><span data-stu-id="5852c-184">85</span></span>

<span data-ttu-id="5852c-185">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5852c-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-186">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="5852c-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-187">86</span><span class="sxs-lookup"><span data-stu-id="5852c-187">86</span></span>

<span data-ttu-id="5852c-188">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="5852c-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-189">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="5852c-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-190">87</span><span class="sxs-lookup"><span data-stu-id="5852c-190">87</span></span>

<span data-ttu-id="5852c-191">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="5852c-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-192">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="5852c-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-193">88</span><span class="sxs-lookup"><span data-stu-id="5852c-193">88</span></span>

<span data-ttu-id="5852c-194">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="5852c-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-195">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="5852c-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-196">89</span><span class="sxs-lookup"><span data-stu-id="5852c-196">89</span></span>

<span data-ttu-id="5852c-197">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="5852c-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-198">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="5852c-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-199">90</span><span class="sxs-lookup"><span data-stu-id="5852c-199">90</span></span>

<span data-ttu-id="5852c-200">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5852c-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-201">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="5852c-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-202">91</span><span class="sxs-lookup"><span data-stu-id="5852c-202">91</span></span>

<span data-ttu-id="5852c-203">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5852c-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-204">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="5852c-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-205">92</span><span class="sxs-lookup"><span data-stu-id="5852c-205">92</span></span>

<span data-ttu-id="5852c-206">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5852c-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-207">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-208">93</span><span class="sxs-lookup"><span data-stu-id="5852c-208">93</span></span>

<span data-ttu-id="5852c-209">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5852c-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-210">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-211">94</span><span class="sxs-lookup"><span data-stu-id="5852c-211">94</span></span>

<span data-ttu-id="5852c-212">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="5852c-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-213">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-214">95</span><span class="sxs-lookup"><span data-stu-id="5852c-214">95</span></span>

<span data-ttu-id="5852c-215">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5852c-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-216">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-217">96</span><span class="sxs-lookup"><span data-stu-id="5852c-217">96</span></span>

<span data-ttu-id="5852c-218">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5852c-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-219">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="5852c-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-220">97</span><span class="sxs-lookup"><span data-stu-id="5852c-220">97</span></span>

<span data-ttu-id="5852c-221">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="5852c-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-222">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="5852c-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-223">98</span><span class="sxs-lookup"><span data-stu-id="5852c-223">98</span></span>

<span data-ttu-id="5852c-224">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="5852c-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-225">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5852c-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-226">100</span><span class="sxs-lookup"><span data-stu-id="5852c-226">100</span></span>

<span data-ttu-id="5852c-227">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5852c-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5852c-228">**Andere**</span><span class="sxs-lookup"><span data-stu-id="5852c-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5852c-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="5852c-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5852c-230">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5852c-230">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5852c-231">Wenn DHCP auf dem lokalen Computersystem aktiviert ist, wird TCP/IP von der Option auf diesem speziellen Netzwerkadapter deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5852c-231">If DHCP is enabled on the local computer system, the option disables TCP/IP on this specific network adapter.</span></span> <span data-ttu-id="5852c-232">Wenn Sie keinen alternativen Pfad zum Zielsystem haben, d. h. einen anderen TCP/IP-gebundenen Netzwerkadapter, gehen alle TCP/IP-Kommunikationen verloren.</span><span class="sxs-lookup"><span data-stu-id="5852c-232">Unless you have an alternate path to the target system, that is, another TCP/IP bound network adapter, all TCP/IP communications will be lost.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5852c-233">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5852c-233">Examples</span></span>

<span data-ttu-id="5852c-234">[Mit dem PowerShell-Beispiel "Release Renew IP Adresses using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell" in der TechNet Gallery wird **ReleaseDHCPLease** zum Freigeben und erneuern einer IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="5852c-234">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **ReleaseDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="5852c-235">Der folgende VBScript-Code gibt die DHCP-Leases für alle TCP/IP-gebundenen Netzwerkadapter auf einem Computer frei.</span><span class="sxs-lookup"><span data-stu-id="5852c-235">The following VBScript code releases the DHCP leases for all TCP/IP-bound network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="5852c-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5852c-236">Requirements</span></span>



| <span data-ttu-id="5852c-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5852c-237">Requirement</span></span> | <span data-ttu-id="5852c-238">Wert</span><span class="sxs-lookup"><span data-stu-id="5852c-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5852c-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5852c-239">Minimum supported client</span></span><br/> | <span data-ttu-id="5852c-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5852c-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5852c-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5852c-241">Minimum supported server</span></span><br/> | <span data-ttu-id="5852c-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5852c-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5852c-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="5852c-243">Namespace</span></span><br/>                | <span data-ttu-id="5852c-244">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5852c-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5852c-245">MOF</span><span class="sxs-lookup"><span data-stu-id="5852c-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5852c-246"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5852c-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5852c-247">DLL</span><span class="sxs-lookup"><span data-stu-id="5852c-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5852c-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5852c-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5852c-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5852c-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5852c-250">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="5852c-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5852c-251">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="5852c-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="5852c-252">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="5852c-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="5852c-253">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="5852c-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="5852c-254">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="5852c-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

