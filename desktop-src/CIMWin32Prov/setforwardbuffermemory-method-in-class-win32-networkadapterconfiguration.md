---
description: Die statische Methode SetForwardBufferMemory WMI-Klasse wird verwendet, um anzugeben, wie viel Arbeitsspeicher-IP zum Speichern von Paketdaten in der Routerpaketwarteschlange zugeordnet wird.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: SetForwardBufferMemory-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861319"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5e325-103">SetForwardBufferMemory-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e325-103">SetForwardBufferMemory method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5e325-104">Die statische Methode **SetForwardBufferMemory** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um anzugeben, wie viel Arbeitsspeicher-IP zum Speichern von Paketdaten in der Routerpaketwarteschlange zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="5e325-104">The **SetForwardBufferMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify how much memory IP allocates to store packet data in the router packet queue.</span></span>

<span data-ttu-id="5e325-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e325-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5e325-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5e325-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e325-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e325-107">Syntax</span></span>


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a><span data-ttu-id="5e325-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e325-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e325-109">*ForwardBufferMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e325-109">*ForwardBufferMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e325-110">Größe (in Bytes) der Routerpaketwarteschlange, die zum Speichern von Paketdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e325-110">Size, in bytes, of the router packet queue used to store packet data.</span></span> <span data-ttu-id="5e325-111">Der Standardwert ist 74240 (50 1480-Byte-Pakete, gerundet auf ein Vielfaches von 256).</span><span class="sxs-lookup"><span data-stu-id="5e325-111">The default value is 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e325-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e325-112">Return value</span></span>

<span data-ttu-id="5e325-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="5e325-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="5e325-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5e325-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5e325-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5e325-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5e325-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5e325-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-117">0</span><span class="sxs-lookup"><span data-stu-id="5e325-117">0</span></span>

<span data-ttu-id="5e325-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e325-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5e325-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-120">1</span><span class="sxs-lookup"><span data-stu-id="5e325-120">1</span></span>

<span data-ttu-id="5e325-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e325-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="5e325-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-123">64</span><span class="sxs-lookup"><span data-stu-id="5e325-123">64</span></span>

<span data-ttu-id="5e325-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e325-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="5e325-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-126">65</span><span class="sxs-lookup"><span data-stu-id="5e325-126">65</span></span>

<span data-ttu-id="5e325-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="5e325-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="5e325-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-129">66</span><span class="sxs-lookup"><span data-stu-id="5e325-129">66</span></span>

<span data-ttu-id="5e325-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="5e325-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="5e325-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-132">67</span><span class="sxs-lookup"><span data-stu-id="5e325-132">67</span></span>

<span data-ttu-id="5e325-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5e325-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="5e325-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-135">68</span><span class="sxs-lookup"><span data-stu-id="5e325-135">68</span></span>

<span data-ttu-id="5e325-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5e325-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="5e325-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-138">69</span><span class="sxs-lookup"><span data-stu-id="5e325-138">69</span></span>

<span data-ttu-id="5e325-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="5e325-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="5e325-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-141">70</span><span class="sxs-lookup"><span data-stu-id="5e325-141">70</span></span>

<span data-ttu-id="5e325-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5e325-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="5e325-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-144">71</span><span class="sxs-lookup"><span data-stu-id="5e325-144">71</span></span>

<span data-ttu-id="5e325-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5e325-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="5e325-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-147">72</span><span class="sxs-lookup"><span data-stu-id="5e325-147">72</span></span>

<span data-ttu-id="5e325-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="5e325-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="5e325-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-150">73</span><span class="sxs-lookup"><span data-stu-id="5e325-150">73</span></span>

<span data-ttu-id="5e325-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="5e325-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="5e325-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-153">74</span><span class="sxs-lookup"><span data-stu-id="5e325-153">74</span></span>

<span data-ttu-id="5e325-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="5e325-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="5e325-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-156">75</span><span class="sxs-lookup"><span data-stu-id="5e325-156">75</span></span>

<span data-ttu-id="5e325-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="5e325-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="5e325-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-159">76</span><span class="sxs-lookup"><span data-stu-id="5e325-159">76</span></span>

<span data-ttu-id="5e325-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="5e325-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="5e325-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-162">77</span><span class="sxs-lookup"><span data-stu-id="5e325-162">77</span></span>

<span data-ttu-id="5e325-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="5e325-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="5e325-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-165">78</span><span class="sxs-lookup"><span data-stu-id="5e325-165">78</span></span>

<span data-ttu-id="5e325-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="5e325-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="5e325-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-168">79</span><span class="sxs-lookup"><span data-stu-id="5e325-168">79</span></span>

<span data-ttu-id="5e325-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="5e325-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-171">80</span><span class="sxs-lookup"><span data-stu-id="5e325-171">80</span></span>

<span data-ttu-id="5e325-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5e325-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-174">81</span><span class="sxs-lookup"><span data-stu-id="5e325-174">81</span></span>

<span data-ttu-id="5e325-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5e325-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-177">82</span><span class="sxs-lookup"><span data-stu-id="5e325-177">82</span></span>

<span data-ttu-id="5e325-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="5e325-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="5e325-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-180">83</span><span class="sxs-lookup"><span data-stu-id="5e325-180">83</span></span>

<span data-ttu-id="5e325-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e325-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5e325-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-183">84</span><span class="sxs-lookup"><span data-stu-id="5e325-183">84</span></span>

<span data-ttu-id="5e325-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e325-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5e325-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-186">85</span><span class="sxs-lookup"><span data-stu-id="5e325-186">85</span></span>

<span data-ttu-id="5e325-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e325-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="5e325-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-189">86</span><span class="sxs-lookup"><span data-stu-id="5e325-189">86</span></span>

<span data-ttu-id="5e325-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="5e325-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="5e325-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-192">87</span><span class="sxs-lookup"><span data-stu-id="5e325-192">87</span></span>

<span data-ttu-id="5e325-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="5e325-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="5e325-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-195">88</span><span class="sxs-lookup"><span data-stu-id="5e325-195">88</span></span>

<span data-ttu-id="5e325-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="5e325-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="5e325-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-198">89</span><span class="sxs-lookup"><span data-stu-id="5e325-198">89</span></span>

<span data-ttu-id="5e325-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="5e325-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="5e325-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-201">90</span><span class="sxs-lookup"><span data-stu-id="5e325-201">90</span></span>

<span data-ttu-id="5e325-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5e325-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="5e325-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-204">91</span><span class="sxs-lookup"><span data-stu-id="5e325-204">91</span></span>

<span data-ttu-id="5e325-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5e325-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="5e325-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-207">92</span><span class="sxs-lookup"><span data-stu-id="5e325-207">92</span></span>

<span data-ttu-id="5e325-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5e325-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-210">93</span><span class="sxs-lookup"><span data-stu-id="5e325-210">93</span></span>

<span data-ttu-id="5e325-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5e325-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-213">94</span><span class="sxs-lookup"><span data-stu-id="5e325-213">94</span></span>

<span data-ttu-id="5e325-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="5e325-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-216">95</span><span class="sxs-lookup"><span data-stu-id="5e325-216">95</span></span>

<span data-ttu-id="5e325-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5e325-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-219">96</span><span class="sxs-lookup"><span data-stu-id="5e325-219">96</span></span>

<span data-ttu-id="5e325-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5e325-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="5e325-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-222">97</span><span class="sxs-lookup"><span data-stu-id="5e325-222">97</span></span>

<span data-ttu-id="5e325-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="5e325-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e325-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-225">98</span><span class="sxs-lookup"><span data-stu-id="5e325-225">98</span></span>

<span data-ttu-id="5e325-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="5e325-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5e325-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-228">100</span><span class="sxs-lookup"><span data-stu-id="5e325-228">100</span></span>

<span data-ttu-id="5e325-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e325-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e325-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="5e325-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5e325-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="5e325-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e325-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e325-232">Remarks</span></span>

<span data-ttu-id="5e325-233">Wenn dieser Pufferbereich ausgefüllt ist, beginnt der Router, Pakete zufällig aus der Warteschlange zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="5e325-233">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span>

<span data-ttu-id="5e325-234">Der Datenpuffer für die Paket Warteschlange beträgt 256 Bytes, sodass der Wert des *ForwardBufferMemory* -Parameters ein Vielfaches von 256 sein sollte.</span><span class="sxs-lookup"><span data-stu-id="5e325-234">Packet queue data buffers are 256 bytes in length, so the value of the *ForwardBufferMemory* parameter should be a multiple of 256.</span></span> <span data-ttu-id="5e325-235">Mehrere Puffer werden für größere Pakete miteinander verkettet.</span><span class="sxs-lookup"><span data-stu-id="5e325-235">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="5e325-236">Der IP-Header für ein Paket wird separat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5e325-236">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="5e325-237">Dieser Parameter wird ignoriert, und es werden keine Puffer zugewiesen, wenn der IP-Router nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5e325-237">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="5e325-238">Die Puffergröße kann zwischen der Netzwerk-maximalen Übertragungseinheit (MTU) und einem Wert kleiner als 0xffffffff liegen.</span><span class="sxs-lookup"><span data-stu-id="5e325-238">The buffer size can range from the network Maximum Transmission Unit (MTU) to a value smaller than 0xFFFFFFFF.</span></span>

## <a name="examples"></a><span data-ttu-id="5e325-239">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e325-239">Examples</span></span>

<span data-ttu-id="5e325-240">Im Beispiel [Ändern des Forward-Pufferspeichers für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript wird der vorwärts Puffer Arbeitsspeicher für alle Netzwerkadapter auf einem Computer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5e325-240">The [Modify the Forward Buffer Memory for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript sample configures the forward buffer memory for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e325-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e325-241">Requirements</span></span>



| <span data-ttu-id="5e325-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e325-242">Requirement</span></span> | <span data-ttu-id="5e325-243">Wert</span><span class="sxs-lookup"><span data-stu-id="5e325-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e325-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e325-244">Minimum supported client</span></span><br/> | <span data-ttu-id="5e325-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e325-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e325-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e325-246">Minimum supported server</span></span><br/> | <span data-ttu-id="5e325-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e325-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e325-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e325-248">Namespace</span></span><br/>                | <span data-ttu-id="5e325-249">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5e325-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e325-250">MOF</span><span class="sxs-lookup"><span data-stu-id="5e325-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e325-251"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5e325-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e325-252">DLL</span><span class="sxs-lookup"><span data-stu-id="5e325-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e325-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e325-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e325-254">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e325-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e325-255">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="5e325-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5e325-256">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="5e325-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="5e325-257">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="5e325-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="5e325-258">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="5e325-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="5e325-259">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="5e325-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

