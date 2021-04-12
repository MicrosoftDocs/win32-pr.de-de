---
description: Die statische Methode setdeadgwdetect WMI-Klasse wird verwendet, um die Erkennung von unzustellbaren Gateways zu aktivieren.
ms.assetid: c813aaef-7215-4759-b68f-7808fd203d9c
ms.tgt_platform: multiple
title: Setdeadgwdetect-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDeadGWDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f62d84af193be99850f1a82b720a2983ca77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482987"
---
# <a name="setdeadgwdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f6e6e-103">Setdeadgwdetect-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6e6e-103">SetDeadGWDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f6e6e-104">Die statische Methode **setdeadgwdetect** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Erkennung von unzustellbaren Gateways zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-104">The **SetDeadGWDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable dead gateway detection.</span></span>

<span data-ttu-id="f6e6e-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f6e6e-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f6e6e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e6e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6e6e-107">Syntax</span></span>


```mof
uint32 SetDeadGWDetect(
  [in] boolean DeadGWDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f6e6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6e6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6e6e-109">*DeadGWDetectEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6e6e-109">*DeadGWDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-110">**True** gibt an, dass die Erkennung von deadlockgateways aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-110">If **true**, dead gateway detection should be enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6e6e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6e6e-111">Return value</span></span>

<span data-ttu-id="f6e6e-112">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f6e6e-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f6e6e-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f6e6e-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f6e6e-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f6e6e-115">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-116">0</span><span class="sxs-lookup"><span data-stu-id="f6e6e-116">0</span></span>

<span data-ttu-id="f6e6e-117">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-118">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-119">1</span><span class="sxs-lookup"><span data-stu-id="f6e6e-119">1</span></span>

<span data-ttu-id="f6e6e-120">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-121">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-122">64</span><span class="sxs-lookup"><span data-stu-id="f6e6e-122">64</span></span>

<span data-ttu-id="f6e6e-123">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-124">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-125">65</span><span class="sxs-lookup"><span data-stu-id="f6e6e-125">65</span></span>

<span data-ttu-id="f6e6e-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-127">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-128">66</span><span class="sxs-lookup"><span data-stu-id="f6e6e-128">66</span></span>

<span data-ttu-id="f6e6e-129">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-131">67</span><span class="sxs-lookup"><span data-stu-id="f6e6e-131">67</span></span>

<span data-ttu-id="f6e6e-132">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-133">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-134">68</span><span class="sxs-lookup"><span data-stu-id="f6e6e-134">68</span></span>

<span data-ttu-id="f6e6e-135">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-136">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-137">69</span><span class="sxs-lookup"><span data-stu-id="f6e6e-137">69</span></span>

<span data-ttu-id="f6e6e-138">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-139">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-140">70</span><span class="sxs-lookup"><span data-stu-id="f6e6e-140">70</span></span>

<span data-ttu-id="f6e6e-141">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-142">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-143">71</span><span class="sxs-lookup"><span data-stu-id="f6e6e-143">71</span></span>

<span data-ttu-id="f6e6e-144">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-145">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-146">72</span><span class="sxs-lookup"><span data-stu-id="f6e6e-146">72</span></span>

<span data-ttu-id="f6e6e-147">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-148">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-149">73</span><span class="sxs-lookup"><span data-stu-id="f6e6e-149">73</span></span>

<span data-ttu-id="f6e6e-150">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-151">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-152">74</span><span class="sxs-lookup"><span data-stu-id="f6e6e-152">74</span></span>

<span data-ttu-id="f6e6e-153">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-154">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-155">75</span><span class="sxs-lookup"><span data-stu-id="f6e6e-155">75</span></span>

<span data-ttu-id="f6e6e-156">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="f6e6e-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-157">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-158">76</span><span class="sxs-lookup"><span data-stu-id="f6e6e-158">76</span></span>

<span data-ttu-id="f6e6e-159">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-160">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-161">77</span><span class="sxs-lookup"><span data-stu-id="f6e6e-161">77</span></span>

<span data-ttu-id="f6e6e-162">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-163">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-164">78</span><span class="sxs-lookup"><span data-stu-id="f6e6e-164">78</span></span>

<span data-ttu-id="f6e6e-165">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-166">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-167">79</span><span class="sxs-lookup"><span data-stu-id="f6e6e-167">79</span></span>

<span data-ttu-id="f6e6e-168">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-169">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-170">80</span><span class="sxs-lookup"><span data-stu-id="f6e6e-170">80</span></span>

<span data-ttu-id="f6e6e-171">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-172">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-173">81</span><span class="sxs-lookup"><span data-stu-id="f6e6e-173">81</span></span>

<span data-ttu-id="f6e6e-174">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-175">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-176">82</span><span class="sxs-lookup"><span data-stu-id="f6e6e-176">82</span></span>

<span data-ttu-id="f6e6e-177">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-178">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-179">83</span><span class="sxs-lookup"><span data-stu-id="f6e6e-179">83</span></span>

<span data-ttu-id="f6e6e-180">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-181">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-182">84</span><span class="sxs-lookup"><span data-stu-id="f6e6e-182">84</span></span>

<span data-ttu-id="f6e6e-183">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-184">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-185">85</span><span class="sxs-lookup"><span data-stu-id="f6e6e-185">85</span></span>

<span data-ttu-id="f6e6e-186">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-187">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-188">86</span><span class="sxs-lookup"><span data-stu-id="f6e6e-188">86</span></span>

<span data-ttu-id="f6e6e-189">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-190">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-191">87</span><span class="sxs-lookup"><span data-stu-id="f6e6e-191">87</span></span>

<span data-ttu-id="f6e6e-192">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-193">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-194">88</span><span class="sxs-lookup"><span data-stu-id="f6e6e-194">88</span></span>

<span data-ttu-id="f6e6e-195">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-196">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-197">89</span><span class="sxs-lookup"><span data-stu-id="f6e6e-197">89</span></span>

<span data-ttu-id="f6e6e-198">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-199">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-200">90</span><span class="sxs-lookup"><span data-stu-id="f6e6e-200">90</span></span>

<span data-ttu-id="f6e6e-201">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-202">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-203">91</span><span class="sxs-lookup"><span data-stu-id="f6e6e-203">91</span></span>

<span data-ttu-id="f6e6e-204">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-205">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-206">92</span><span class="sxs-lookup"><span data-stu-id="f6e6e-206">92</span></span>

<span data-ttu-id="f6e6e-207">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-208">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-209">93</span><span class="sxs-lookup"><span data-stu-id="f6e6e-209">93</span></span>

<span data-ttu-id="f6e6e-210">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-211">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-212">94</span><span class="sxs-lookup"><span data-stu-id="f6e6e-212">94</span></span>

<span data-ttu-id="f6e6e-213">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-214">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-215">95</span><span class="sxs-lookup"><span data-stu-id="f6e6e-215">95</span></span>

<span data-ttu-id="f6e6e-216">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-217">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-218">96</span><span class="sxs-lookup"><span data-stu-id="f6e6e-218">96</span></span>

<span data-ttu-id="f6e6e-219">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-220">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-221">97</span><span class="sxs-lookup"><span data-stu-id="f6e6e-221">97</span></span>

<span data-ttu-id="f6e6e-222">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-223">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-224">98</span><span class="sxs-lookup"><span data-stu-id="f6e6e-224">98</span></span>

<span data-ttu-id="f6e6e-225">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-226">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-227">100</span><span class="sxs-lookup"><span data-stu-id="f6e6e-227">100</span></span>

<span data-ttu-id="f6e6e-228">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6e-229">**Andere**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f6e6e-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f6e6e-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6e6e-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6e6e-231">Remarks</span></span>

<span data-ttu-id="f6e6e-232">Wenn diese Funktion aktiviert ist, fordert TCP die IP-Adresse auf, um zu einem Sicherungs Gateway zu wechseln, wenn ein Segment mehrmals neu übermittelt wird, ohne eine Antwort zu erhalten</span><span class="sxs-lookup"><span data-stu-id="f6e6e-232">With this feature enabled, TCP asks IP to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

## <a name="examples"></a><span data-ttu-id="f6e6e-233">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6e6e-233">Examples</span></span>

<span data-ttu-id="f6e6e-234">Das Beispiel Aktivieren der Erkennung von unzustellbaren Gateways [für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript in der TechNet Gallery verwendet **setdeadgwdetect** , um alle Netzwerkadapter auf einem Computer so zu konfigurieren, dass unzustellbare Gateways automatisch erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f6e6e-234">The [Enable Dead Gateway Detection for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript sample on TechNet Gallery uses **SetDeadGWDetect** to configure all network adapters on a computer to automatically detect dead gateways.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e6e-235">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6e6e-235">Requirements</span></span>



| <span data-ttu-id="f6e6e-236">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6e6e-236">Requirement</span></span> | <span data-ttu-id="f6e6e-237">Wert</span><span class="sxs-lookup"><span data-stu-id="f6e6e-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e6e-238">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6e6e-238">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e6e-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6e6e-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6e6e-240">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6e6e-240">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e6e-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6e6e-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6e6e-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6e6e-242">Namespace</span></span><br/>                | <span data-ttu-id="f6e6e-243">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f6e6e-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6e6e-244">MOF</span><span class="sxs-lookup"><span data-stu-id="f6e6e-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6e6e-245"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6e6e-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6e6e-246">DLL</span><span class="sxs-lookup"><span data-stu-id="f6e6e-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6e6e-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6e6e-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6e6e-248">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6e6e-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e6e-249">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="f6e6e-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f6e6e-250">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="f6e6e-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f6e6e-251">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f6e6e-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f6e6e-252">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="f6e6e-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f6e6e-253">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="f6e6e-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

