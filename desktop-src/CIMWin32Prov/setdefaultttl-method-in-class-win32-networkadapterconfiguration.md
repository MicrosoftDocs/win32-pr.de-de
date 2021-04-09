---
description: Die statische Methode setdefaultttl WMI-Klasse wird verwendet, um den Standardwert für die Gültigkeitsdauer (Time to Live, TTL) im Header von ausgehenden IP-Paketen festzulegen.
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Setdefaultttl-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860592"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9aef3-103">Setdefaultttl-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="9aef3-103">SetDefaultTTL method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9aef3-104">Die statische Methode **setdefaultttl** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um den Standardwert für die Gültigkeitsdauer (Time to Live, TTL) im Header von ausgehenden IP-Paketen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9aef3-104">The **SetDefaultTTL** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span>

<span data-ttu-id="9aef3-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9aef3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9aef3-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9aef3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9aef3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9aef3-107">Syntax</span></span>


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a><span data-ttu-id="9aef3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9aef3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aef3-109">*DefaultTTL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aef3-109">*DefaultTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-110">Der Gültigkeitsdauer Wert, der im Header der ausgehenden IP-Pakete festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9aef3-110">Time to Live value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="9aef3-111">Der Standardwert ist 32; Gültiger Bereich: 1-255</span><span class="sxs-lookup"><span data-stu-id="9aef3-111">The default value is 32; Valid range: 1 - 255</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aef3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9aef3-112">Return value</span></span>

<span data-ttu-id="9aef3-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="9aef3-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="9aef3-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9aef3-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9aef3-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9aef3-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9aef3-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9aef3-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-117">0</span><span class="sxs-lookup"><span data-stu-id="9aef3-117">0</span></span>

<span data-ttu-id="9aef3-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9aef3-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9aef3-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-120">1</span><span class="sxs-lookup"><span data-stu-id="9aef3-120">1</span></span>

<span data-ttu-id="9aef3-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9aef3-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-123">64</span><span class="sxs-lookup"><span data-stu-id="9aef3-123">64</span></span>

<span data-ttu-id="9aef3-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9aef3-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-126">65</span><span class="sxs-lookup"><span data-stu-id="9aef3-126">65</span></span>

<span data-ttu-id="9aef3-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9aef3-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-129">66</span><span class="sxs-lookup"><span data-stu-id="9aef3-129">66</span></span>

<span data-ttu-id="9aef3-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="9aef3-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-132">67</span><span class="sxs-lookup"><span data-stu-id="9aef3-132">67</span></span>

<span data-ttu-id="9aef3-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9aef3-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="9aef3-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-135">68</span><span class="sxs-lookup"><span data-stu-id="9aef3-135">68</span></span>

<span data-ttu-id="9aef3-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="9aef3-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-138">69</span><span class="sxs-lookup"><span data-stu-id="9aef3-138">69</span></span>

<span data-ttu-id="9aef3-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="9aef3-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="9aef3-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-141">70</span><span class="sxs-lookup"><span data-stu-id="9aef3-141">70</span></span>

<span data-ttu-id="9aef3-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9aef3-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="9aef3-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-144">71</span><span class="sxs-lookup"><span data-stu-id="9aef3-144">71</span></span>

<span data-ttu-id="9aef3-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9aef3-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-147">72</span><span class="sxs-lookup"><span data-stu-id="9aef3-147">72</span></span>

<span data-ttu-id="9aef3-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="9aef3-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="9aef3-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-150">73</span><span class="sxs-lookup"><span data-stu-id="9aef3-150">73</span></span>

<span data-ttu-id="9aef3-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="9aef3-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="9aef3-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-153">74</span><span class="sxs-lookup"><span data-stu-id="9aef3-153">74</span></span>

<span data-ttu-id="9aef3-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="9aef3-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-156">75</span><span class="sxs-lookup"><span data-stu-id="9aef3-156">75</span></span>

<span data-ttu-id="9aef3-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="9aef3-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="9aef3-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-159">76</span><span class="sxs-lookup"><span data-stu-id="9aef3-159">76</span></span>

<span data-ttu-id="9aef3-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="9aef3-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-162">77</span><span class="sxs-lookup"><span data-stu-id="9aef3-162">77</span></span>

<span data-ttu-id="9aef3-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="9aef3-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="9aef3-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-165">78</span><span class="sxs-lookup"><span data-stu-id="9aef3-165">78</span></span>

<span data-ttu-id="9aef3-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="9aef3-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="9aef3-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-168">79</span><span class="sxs-lookup"><span data-stu-id="9aef3-168">79</span></span>

<span data-ttu-id="9aef3-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="9aef3-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-171">80</span><span class="sxs-lookup"><span data-stu-id="9aef3-171">80</span></span>

<span data-ttu-id="9aef3-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-174">81</span><span class="sxs-lookup"><span data-stu-id="9aef3-174">81</span></span>

<span data-ttu-id="9aef3-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-177">82</span><span class="sxs-lookup"><span data-stu-id="9aef3-177">82</span></span>

<span data-ttu-id="9aef3-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="9aef3-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-180">83</span><span class="sxs-lookup"><span data-stu-id="9aef3-180">83</span></span>

<span data-ttu-id="9aef3-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-183">84</span><span class="sxs-lookup"><span data-stu-id="9aef3-183">84</span></span>

<span data-ttu-id="9aef3-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9aef3-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-186">85</span><span class="sxs-lookup"><span data-stu-id="9aef3-186">85</span></span>

<span data-ttu-id="9aef3-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9aef3-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-189">86</span><span class="sxs-lookup"><span data-stu-id="9aef3-189">86</span></span>

<span data-ttu-id="9aef3-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="9aef3-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="9aef3-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-192">87</span><span class="sxs-lookup"><span data-stu-id="9aef3-192">87</span></span>

<span data-ttu-id="9aef3-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="9aef3-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="9aef3-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-195">88</span><span class="sxs-lookup"><span data-stu-id="9aef3-195">88</span></span>

<span data-ttu-id="9aef3-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="9aef3-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="9aef3-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-198">89</span><span class="sxs-lookup"><span data-stu-id="9aef3-198">89</span></span>

<span data-ttu-id="9aef3-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="9aef3-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="9aef3-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-201">90</span><span class="sxs-lookup"><span data-stu-id="9aef3-201">90</span></span>

<span data-ttu-id="9aef3-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="9aef3-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="9aef3-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-204">91</span><span class="sxs-lookup"><span data-stu-id="9aef3-204">91</span></span>

<span data-ttu-id="9aef3-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="9aef3-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="9aef3-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-207">92</span><span class="sxs-lookup"><span data-stu-id="9aef3-207">92</span></span>

<span data-ttu-id="9aef3-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9aef3-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-210">93</span><span class="sxs-lookup"><span data-stu-id="9aef3-210">93</span></span>

<span data-ttu-id="9aef3-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-213">94</span><span class="sxs-lookup"><span data-stu-id="9aef3-213">94</span></span>

<span data-ttu-id="9aef3-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-216">95</span><span class="sxs-lookup"><span data-stu-id="9aef3-216">95</span></span>

<span data-ttu-id="9aef3-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-219">96</span><span class="sxs-lookup"><span data-stu-id="9aef3-219">96</span></span>

<span data-ttu-id="9aef3-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="9aef3-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-222">97</span><span class="sxs-lookup"><span data-stu-id="9aef3-222">97</span></span>

<span data-ttu-id="9aef3-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="9aef3-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-225">98</span><span class="sxs-lookup"><span data-stu-id="9aef3-225">98</span></span>

<span data-ttu-id="9aef3-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="9aef3-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="9aef3-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-228">100</span><span class="sxs-lookup"><span data-stu-id="9aef3-228">100</span></span>

<span data-ttu-id="9aef3-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9aef3-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9aef3-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="9aef3-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9aef3-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9aef3-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9aef3-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9aef3-232">Remarks</span></span>

<span data-ttu-id="9aef3-233">Die Gültigkeitsdauer gibt an, wie viele Router ein IP-Paket durchlaufen kann, um das Ziel zu erreichen, bevor es verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="9aef3-233">The TTL specifies the number of routers an IP packet may pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="9aef3-234">Jeder Router verringert die TTL-Anzahl eines Pakets um eins und verwirft die Pakete mit einer Gültigkeitsdauer von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9aef3-234">Each router decrements the TTL count of a packet by one and discards the packets with a TTL of 0 (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="9aef3-235">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9aef3-235">Examples</span></span>

<span data-ttu-id="9aef3-236">Im Beispiel [Modify the default time to Live for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript wird **setdefaultttl** verwendet, um den Standardwert für die Gültigkeitsdauer im Header der ausgehenden IP-Pakete auf 64 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9aef3-236">The [Modify the Default Time-to-Live for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript sample uses **SetDefaultTTL** to set the default time-to-live value in the header of outgoing IP packets to 64</span></span>

## <a name="requirements"></a><span data-ttu-id="9aef3-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aef3-237">Requirements</span></span>



| <span data-ttu-id="9aef3-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aef3-238">Requirement</span></span> | <span data-ttu-id="9aef3-239">Wert</span><span class="sxs-lookup"><span data-stu-id="9aef3-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aef3-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9aef3-240">Minimum supported client</span></span><br/> | <span data-ttu-id="9aef3-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9aef3-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9aef3-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9aef3-242">Minimum supported server</span></span><br/> | <span data-ttu-id="9aef3-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aef3-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9aef3-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="9aef3-244">Namespace</span></span><br/>                | <span data-ttu-id="9aef3-245">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9aef3-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9aef3-246">MOF</span><span class="sxs-lookup"><span data-stu-id="9aef3-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9aef3-247"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9aef3-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9aef3-248">DLL</span><span class="sxs-lookup"><span data-stu-id="9aef3-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aef3-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aef3-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aef3-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aef3-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aef3-251">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9aef3-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9aef3-252">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="9aef3-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9aef3-253">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="9aef3-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9aef3-254">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="9aef3-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9aef3-255">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="9aef3-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

