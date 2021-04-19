---
description: Diese Methode ist veraltet. Anwendungen sollten die Quality of Service (QoS)-API verwenden, um Typ von Dienst Bits (TOS) zu bearbeiten.
ms.assetid: 18860c13-7324-4a37-b83c-f3d15c425acb
ms.tgt_platform: multiple
title: Setdefaulttos-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTOS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5df55ff88c87047a48a84a122c8e58c8148a7cff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346034"
---
# <a name="setdefaulttos-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="30bbb-104">Setdefaulttos-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="30bbb-104">SetDefaultTOS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="30bbb-105">Diese Methode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="30bbb-105">This method is obsolete.</span></span> <span data-ttu-id="30bbb-106">Anwendungen sollten die Quality of Service (QoS)-API verwenden, um Typ von Dienst Bits (TOS) zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="30bbb-106">Applications should use the Quality of Service (QoS) API to manipulate Type of Service (TOS) bits.</span></span> <span data-ttu-id="30bbb-107">Weitere Informationen finden Sie unter [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span><span class="sxs-lookup"><span data-stu-id="30bbb-107">For more information, see [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span></span>

<span data-ttu-id="30bbb-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="30bbb-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="30bbb-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="30bbb-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="30bbb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="30bbb-110">Syntax</span></span>


```mof
uint32 SetDefaultTOS(
  [in] uint8 DefaultTOS
);
```



## <a name="parameters"></a><span data-ttu-id="30bbb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="30bbb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30bbb-112">*DefaultTOS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30bbb-112">*DefaultTOS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-113">Der Typ des Dienst Werts (TOS), der im Header von ausgehenden IP-Paketen abgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="30bbb-113">Type of Service (TOS) value put in the header of outgoing IP packets.</span></span> <span data-ttu-id="30bbb-114">Eine Definition der Werte finden Sie unter RFC 791.</span><span class="sxs-lookup"><span data-stu-id="30bbb-114">For a definition of the values, see RFC 791.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30bbb-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30bbb-115">Return value</span></span>

<span data-ttu-id="30bbb-116">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="30bbb-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="30bbb-117">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="30bbb-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="30bbb-118">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="30bbb-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="30bbb-119">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="30bbb-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-120">0</span><span class="sxs-lookup"><span data-stu-id="30bbb-120">0</span></span>

<span data-ttu-id="30bbb-121">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="30bbb-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-122">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="30bbb-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-123">1</span><span class="sxs-lookup"><span data-stu-id="30bbb-123">1</span></span>

<span data-ttu-id="30bbb-124">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="30bbb-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-125">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-126">64</span><span class="sxs-lookup"><span data-stu-id="30bbb-126">64</span></span>

<span data-ttu-id="30bbb-127">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30bbb-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-128">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-129">65</span><span class="sxs-lookup"><span data-stu-id="30bbb-129">65</span></span>

<span data-ttu-id="30bbb-130">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="30bbb-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-131">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-132">66</span><span class="sxs-lookup"><span data-stu-id="30bbb-132">66</span></span>

<span data-ttu-id="30bbb-133">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="30bbb-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-134">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-135">67</span><span class="sxs-lookup"><span data-stu-id="30bbb-135">67</span></span>

<span data-ttu-id="30bbb-136">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="30bbb-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-137">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="30bbb-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-138">68</span><span class="sxs-lookup"><span data-stu-id="30bbb-138">68</span></span>

<span data-ttu-id="30bbb-139">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="30bbb-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-140">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-141">69</span><span class="sxs-lookup"><span data-stu-id="30bbb-141">69</span></span>

<span data-ttu-id="30bbb-142">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="30bbb-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-143">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="30bbb-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-144">70</span><span class="sxs-lookup"><span data-stu-id="30bbb-144">70</span></span>

<span data-ttu-id="30bbb-145">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="30bbb-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-146">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="30bbb-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-147">71</span><span class="sxs-lookup"><span data-stu-id="30bbb-147">71</span></span>

<span data-ttu-id="30bbb-148">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="30bbb-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-149">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-150">72</span><span class="sxs-lookup"><span data-stu-id="30bbb-150">72</span></span>

<span data-ttu-id="30bbb-151">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="30bbb-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-152">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="30bbb-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-153">73</span><span class="sxs-lookup"><span data-stu-id="30bbb-153">73</span></span>

<span data-ttu-id="30bbb-154">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="30bbb-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-155">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="30bbb-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-156">74</span><span class="sxs-lookup"><span data-stu-id="30bbb-156">74</span></span>

<span data-ttu-id="30bbb-157">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="30bbb-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-158">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-159">75</span><span class="sxs-lookup"><span data-stu-id="30bbb-159">75</span></span>

<span data-ttu-id="30bbb-160">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="30bbb-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-161">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="30bbb-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-162">76</span><span class="sxs-lookup"><span data-stu-id="30bbb-162">76</span></span>

<span data-ttu-id="30bbb-163">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="30bbb-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-164">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-165">77</span><span class="sxs-lookup"><span data-stu-id="30bbb-165">77</span></span>

<span data-ttu-id="30bbb-166">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="30bbb-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-167">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="30bbb-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-168">78</span><span class="sxs-lookup"><span data-stu-id="30bbb-168">78</span></span>

<span data-ttu-id="30bbb-169">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="30bbb-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-170">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="30bbb-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-171">79</span><span class="sxs-lookup"><span data-stu-id="30bbb-171">79</span></span>

<span data-ttu-id="30bbb-172">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="30bbb-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-173">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-174">80</span><span class="sxs-lookup"><span data-stu-id="30bbb-174">80</span></span>

<span data-ttu-id="30bbb-175">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-176">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-177">81</span><span class="sxs-lookup"><span data-stu-id="30bbb-177">81</span></span>

<span data-ttu-id="30bbb-178">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-179">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-180">82</span><span class="sxs-lookup"><span data-stu-id="30bbb-180">82</span></span>

<span data-ttu-id="30bbb-181">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-182">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="30bbb-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-183">83</span><span class="sxs-lookup"><span data-stu-id="30bbb-183">83</span></span>

<span data-ttu-id="30bbb-184">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-185">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-186">84</span><span class="sxs-lookup"><span data-stu-id="30bbb-186">84</span></span>

<span data-ttu-id="30bbb-187">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="30bbb-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-188">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-189">85</span><span class="sxs-lookup"><span data-stu-id="30bbb-189">85</span></span>

<span data-ttu-id="30bbb-190">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="30bbb-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-191">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-192">86</span><span class="sxs-lookup"><span data-stu-id="30bbb-192">86</span></span>

<span data-ttu-id="30bbb-193">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="30bbb-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-194">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="30bbb-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-195">87</span><span class="sxs-lookup"><span data-stu-id="30bbb-195">87</span></span>

<span data-ttu-id="30bbb-196">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="30bbb-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-197">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="30bbb-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-198">88</span><span class="sxs-lookup"><span data-stu-id="30bbb-198">88</span></span>

<span data-ttu-id="30bbb-199">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="30bbb-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-200">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="30bbb-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-201">89</span><span class="sxs-lookup"><span data-stu-id="30bbb-201">89</span></span>

<span data-ttu-id="30bbb-202">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="30bbb-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-203">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="30bbb-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-204">90</span><span class="sxs-lookup"><span data-stu-id="30bbb-204">90</span></span>

<span data-ttu-id="30bbb-205">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="30bbb-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-206">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="30bbb-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-207">91</span><span class="sxs-lookup"><span data-stu-id="30bbb-207">91</span></span>

<span data-ttu-id="30bbb-208">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="30bbb-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-209">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="30bbb-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-210">92</span><span class="sxs-lookup"><span data-stu-id="30bbb-210">92</span></span>

<span data-ttu-id="30bbb-211">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="30bbb-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-212">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-213">93</span><span class="sxs-lookup"><span data-stu-id="30bbb-213">93</span></span>

<span data-ttu-id="30bbb-214">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-215">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-216">94</span><span class="sxs-lookup"><span data-stu-id="30bbb-216">94</span></span>

<span data-ttu-id="30bbb-217">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-218">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-219">95</span><span class="sxs-lookup"><span data-stu-id="30bbb-219">95</span></span>

<span data-ttu-id="30bbb-220">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-221">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-222">96</span><span class="sxs-lookup"><span data-stu-id="30bbb-222">96</span></span>

<span data-ttu-id="30bbb-223">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-224">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="30bbb-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-225">97</span><span class="sxs-lookup"><span data-stu-id="30bbb-225">97</span></span>

<span data-ttu-id="30bbb-226">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="30bbb-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-227">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-228">98</span><span class="sxs-lookup"><span data-stu-id="30bbb-228">98</span></span>

<span data-ttu-id="30bbb-229">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="30bbb-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-230">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="30bbb-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-231">100</span><span class="sxs-lookup"><span data-stu-id="30bbb-231">100</span></span>

<span data-ttu-id="30bbb-232">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="30bbb-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="30bbb-233">**Andere**</span><span class="sxs-lookup"><span data-stu-id="30bbb-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="30bbb-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="30bbb-234">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30bbb-235">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30bbb-235">Remarks</span></span>

<span data-ttu-id="30bbb-236">Die statische Methode **setdefaulttos** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um den Standardwert von TOS im Header von ausgehenden IP-Paketen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="30bbb-236">The **SetDefaultTOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default TOS value in the header of outgoing IP packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="30bbb-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30bbb-237">Requirements</span></span>



| <span data-ttu-id="30bbb-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30bbb-238">Requirement</span></span> | <span data-ttu-id="30bbb-239">Wert</span><span class="sxs-lookup"><span data-stu-id="30bbb-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30bbb-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30bbb-240">Minimum supported client</span></span><br/> | <span data-ttu-id="30bbb-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30bbb-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30bbb-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30bbb-242">Minimum supported server</span></span><br/> | <span data-ttu-id="30bbb-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30bbb-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30bbb-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="30bbb-244">Namespace</span></span><br/>                | <span data-ttu-id="30bbb-245">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="30bbb-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="30bbb-246">MOF</span><span class="sxs-lookup"><span data-stu-id="30bbb-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30bbb-247"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="30bbb-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="30bbb-248">DLL</span><span class="sxs-lookup"><span data-stu-id="30bbb-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30bbb-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30bbb-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30bbb-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30bbb-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bbb-251">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="30bbb-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="30bbb-252">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="30bbb-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="30bbb-253">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="30bbb-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="30bbb-254">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="30bbb-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="30bbb-255">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="30bbb-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

