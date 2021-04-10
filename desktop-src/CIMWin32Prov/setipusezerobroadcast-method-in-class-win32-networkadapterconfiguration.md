---
description: Die statische Methode SetIPUseZeroBroadcast WMI-Klasse wird verwendet, um die Verwendung von IP Zero Broadcast festzulegen.
ms.assetid: d20ac6fc-a5d5-4ad9-a2a5-65142b4c7d02
ms.tgt_platform: multiple
title: Die ""-Methode der Klasse "Win32_NetworkAdapterConfiguration".
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPUseZeroBroadcast
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 564f122242407f4d6f5dd28da9fd4d151ab6b47f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127064"
---
# <a name="setipusezerobroadcast-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="968d5-103">""-Methode der " \_ networkadapterconfiguration"-Klasse von Win32</span><span class="sxs-lookup"><span data-stu-id="968d5-103">SetIPUseZeroBroadcast method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="968d5-104">Die statische Methode **SetIPUseZeroBroadcast** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Verwendung von IP Zero Broadcast festzulegen.</span><span class="sxs-lookup"><span data-stu-id="968d5-104">The **SetIPUseZeroBroadcast** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set IP zero broadcast usage.</span></span>

<span data-ttu-id="968d5-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="968d5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="968d5-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="968d5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="968d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="968d5-107">Syntax</span></span>


```mof
uint32 SetIPUseZeroBroadcast(
  [in] boolean IPUseZeroBroadcast
);
```



## <a name="parameters"></a><span data-ttu-id="968d5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="968d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="968d5-109">*Ipuabzerobroadcast* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="968d5-109">*IPUseZeroBroadcast* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="968d5-110">**True** gibt an, dass IP 0 (null) gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="968d5-110">If **true**, IP zero broadcast is used.</span></span> <span data-ttu-id="968d5-111">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="968d5-111">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="968d5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="968d5-112">Return value</span></span>

<span data-ttu-id="968d5-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="968d5-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="968d5-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="968d5-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="968d5-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="968d5-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="968d5-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="968d5-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-117">0</span><span class="sxs-lookup"><span data-stu-id="968d5-117">0</span></span>

<span data-ttu-id="968d5-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="968d5-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="968d5-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-120">1</span><span class="sxs-lookup"><span data-stu-id="968d5-120">1</span></span>

<span data-ttu-id="968d5-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="968d5-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="968d5-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-123">64</span><span class="sxs-lookup"><span data-stu-id="968d5-123">64</span></span>

<span data-ttu-id="968d5-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="968d5-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="968d5-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-126">65</span><span class="sxs-lookup"><span data-stu-id="968d5-126">65</span></span>

<span data-ttu-id="968d5-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="968d5-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="968d5-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-129">66</span><span class="sxs-lookup"><span data-stu-id="968d5-129">66</span></span>

<span data-ttu-id="968d5-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="968d5-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="968d5-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-132">67</span><span class="sxs-lookup"><span data-stu-id="968d5-132">67</span></span>

<span data-ttu-id="968d5-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="968d5-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="968d5-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-135">68</span><span class="sxs-lookup"><span data-stu-id="968d5-135">68</span></span>

<span data-ttu-id="968d5-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="968d5-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="968d5-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-138">69</span><span class="sxs-lookup"><span data-stu-id="968d5-138">69</span></span>

<span data-ttu-id="968d5-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="968d5-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="968d5-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-141">70</span><span class="sxs-lookup"><span data-stu-id="968d5-141">70</span></span>

<span data-ttu-id="968d5-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="968d5-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="968d5-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-144">71</span><span class="sxs-lookup"><span data-stu-id="968d5-144">71</span></span>

<span data-ttu-id="968d5-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="968d5-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="968d5-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-147">72</span><span class="sxs-lookup"><span data-stu-id="968d5-147">72</span></span>

<span data-ttu-id="968d5-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="968d5-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="968d5-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-150">73</span><span class="sxs-lookup"><span data-stu-id="968d5-150">73</span></span>

<span data-ttu-id="968d5-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="968d5-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="968d5-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-153">74</span><span class="sxs-lookup"><span data-stu-id="968d5-153">74</span></span>

<span data-ttu-id="968d5-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="968d5-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="968d5-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-156">75</span><span class="sxs-lookup"><span data-stu-id="968d5-156">75</span></span>

<span data-ttu-id="968d5-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="968d5-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="968d5-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-159">76</span><span class="sxs-lookup"><span data-stu-id="968d5-159">76</span></span>

<span data-ttu-id="968d5-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="968d5-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="968d5-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-162">77</span><span class="sxs-lookup"><span data-stu-id="968d5-162">77</span></span>

<span data-ttu-id="968d5-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="968d5-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="968d5-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-165">78</span><span class="sxs-lookup"><span data-stu-id="968d5-165">78</span></span>

<span data-ttu-id="968d5-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="968d5-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="968d5-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-168">79</span><span class="sxs-lookup"><span data-stu-id="968d5-168">79</span></span>

<span data-ttu-id="968d5-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="968d5-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-171">80</span><span class="sxs-lookup"><span data-stu-id="968d5-171">80</span></span>

<span data-ttu-id="968d5-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="968d5-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-174">81</span><span class="sxs-lookup"><span data-stu-id="968d5-174">81</span></span>

<span data-ttu-id="968d5-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="968d5-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-177">82</span><span class="sxs-lookup"><span data-stu-id="968d5-177">82</span></span>

<span data-ttu-id="968d5-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="968d5-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="968d5-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-180">83</span><span class="sxs-lookup"><span data-stu-id="968d5-180">83</span></span>

<span data-ttu-id="968d5-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="968d5-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="968d5-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-183">84</span><span class="sxs-lookup"><span data-stu-id="968d5-183">84</span></span>

<span data-ttu-id="968d5-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="968d5-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="968d5-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-186">85</span><span class="sxs-lookup"><span data-stu-id="968d5-186">85</span></span>

<span data-ttu-id="968d5-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="968d5-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="968d5-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-189">86</span><span class="sxs-lookup"><span data-stu-id="968d5-189">86</span></span>

<span data-ttu-id="968d5-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="968d5-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="968d5-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-192">87</span><span class="sxs-lookup"><span data-stu-id="968d5-192">87</span></span>

<span data-ttu-id="968d5-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="968d5-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="968d5-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-195">88</span><span class="sxs-lookup"><span data-stu-id="968d5-195">88</span></span>

<span data-ttu-id="968d5-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="968d5-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="968d5-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-198">89</span><span class="sxs-lookup"><span data-stu-id="968d5-198">89</span></span>

<span data-ttu-id="968d5-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="968d5-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="968d5-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-201">90</span><span class="sxs-lookup"><span data-stu-id="968d5-201">90</span></span>

<span data-ttu-id="968d5-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="968d5-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="968d5-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-204">91</span><span class="sxs-lookup"><span data-stu-id="968d5-204">91</span></span>

<span data-ttu-id="968d5-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="968d5-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="968d5-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-207">92</span><span class="sxs-lookup"><span data-stu-id="968d5-207">92</span></span>

<span data-ttu-id="968d5-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="968d5-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-210">93</span><span class="sxs-lookup"><span data-stu-id="968d5-210">93</span></span>

<span data-ttu-id="968d5-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="968d5-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-213">94</span><span class="sxs-lookup"><span data-stu-id="968d5-213">94</span></span>

<span data-ttu-id="968d5-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="968d5-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-216">95</span><span class="sxs-lookup"><span data-stu-id="968d5-216">95</span></span>

<span data-ttu-id="968d5-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="968d5-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-219">96</span><span class="sxs-lookup"><span data-stu-id="968d5-219">96</span></span>

<span data-ttu-id="968d5-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="968d5-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="968d5-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-222">97</span><span class="sxs-lookup"><span data-stu-id="968d5-222">97</span></span>

<span data-ttu-id="968d5-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="968d5-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="968d5-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-225">98</span><span class="sxs-lookup"><span data-stu-id="968d5-225">98</span></span>

<span data-ttu-id="968d5-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="968d5-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="968d5-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-228">100</span><span class="sxs-lookup"><span data-stu-id="968d5-228">100</span></span>

<span data-ttu-id="968d5-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="968d5-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="968d5-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="968d5-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="968d5-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="968d5-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="968d5-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="968d5-232">Remarks</span></span>

<span data-ttu-id="968d5-233">Wenn der *IPUseZeroBroadcast* -Parameter auf " **true**" festgelegt ist, verwendet IP keine Übertragungen (0.0.0.0) anstelle von einübertragungen (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="968d5-233">If the *IPUseZeroBroadcast* parameter is set to **TRUE**, then IP will use zero-broadcasts (0.0.0.0) instead of one-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="968d5-234">Die meisten Systeme verwenden einen Broadcast, aber Systeme, die von BSD-Implementierungen abgeleitet werden, verwenden keine Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="968d5-234">Most systems use one-broadcasts, but systems derived from BSD implementations use zero-broadcasts.</span></span> <span data-ttu-id="968d5-235">Systeme, die verschiedene Übertragungen verwenden, werden nicht im selben Netzwerk zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="968d5-235">Systems that use different broadcasts will not interoperate on the same network.</span></span>

## <a name="examples"></a><span data-ttu-id="968d5-236">Beispiele</span><span class="sxs-lookup"><span data-stu-id="968d5-236">Examples</span></span>

<span data-ttu-id="968d5-237">Im Beispiel [Modify Zero-Broadcast use for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript wird ein Computer so konfiguriert, dass er keine Übertragungen (0.0.0.0) anstelle von einem Broadcast (255.255.255.255) verwendet.</span><span class="sxs-lookup"><span data-stu-id="968d5-237">The [Modify Zero-Broadcast Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript sample configures a computer to use zero-broadcasts (0.0.0.0) rather than one-broadcasts (255.255.255.255).</span></span>

## <a name="requirements"></a><span data-ttu-id="968d5-238">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="968d5-238">Requirements</span></span>



| <span data-ttu-id="968d5-239">Anforderung</span><span class="sxs-lookup"><span data-stu-id="968d5-239">Requirement</span></span> | <span data-ttu-id="968d5-240">Wert</span><span class="sxs-lookup"><span data-stu-id="968d5-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="968d5-241">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="968d5-241">Minimum supported client</span></span><br/> | <span data-ttu-id="968d5-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="968d5-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="968d5-243">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="968d5-243">Minimum supported server</span></span><br/> | <span data-ttu-id="968d5-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="968d5-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="968d5-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="968d5-245">Namespace</span></span><br/>                | <span data-ttu-id="968d5-246">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="968d5-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="968d5-247">MOF</span><span class="sxs-lookup"><span data-stu-id="968d5-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="968d5-248"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="968d5-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="968d5-249">DLL</span><span class="sxs-lookup"><span data-stu-id="968d5-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="968d5-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="968d5-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="968d5-251">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="968d5-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968d5-252">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="968d5-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="968d5-253">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="968d5-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="968d5-254">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="968d5-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="968d5-255">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="968d5-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="968d5-256">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="968d5-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

