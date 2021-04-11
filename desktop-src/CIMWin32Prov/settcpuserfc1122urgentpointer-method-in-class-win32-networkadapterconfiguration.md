---
description: Die statische SetTcpUseRFC1122UrgentPointer WMI-Klasse wird verwendet, um anzugeben, ob TCP die RFC 1122-Spezifikation für dringende Daten oder den Modus verwendet, der von den von Berkeley (Berkeley Software Design) abgeleiteten Systemen verwendet wird.
ms.assetid: f8d07690-2723-4bc3-b15f-a24d575456a7
ms.tgt_platform: multiple
title: SetTcpUseRFC1122UrgentPointer-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpUseRFC1122UrgentPointer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 928a809211288eb7f024c735ce033b819e5d49f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126856"
---
# <a name="settcpuserfc1122urgentpointer-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5e81d-103">SetTcpUseRFC1122UrgentPointer-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e81d-103">SetTcpUseRFC1122UrgentPointer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5e81d-104">Die statische **SetTcpUseRFC1122UrgentPointer** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um anzugeben, ob TCP die RFC 1122-Spezifikation für dringende Daten oder den Modus verwendet, der von den von Berkeley (Berkeley Software Design) abgeleiteten Systemen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e81d-104">The **SetTcpUseRFC1122UrgentPointer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span>

<span data-ttu-id="5e81d-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e81d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5e81d-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5e81d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e81d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e81d-107">Syntax</span></span>


```mof
uint32 SetTcpUseRFC1122UrgentPointer(
  [in] boolean TcpUseRFC1122UrgentPointer
);
```



## <a name="parameters"></a><span data-ttu-id="5e81d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e81d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e81d-109">*TcpUseRFC1122UrgentPointer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e81d-109">*TcpUseRFC1122UrgentPointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-110">**True** gibt an, dass TCP die Spezifikation RFC 1122 verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e81d-110">If **true**, TCP uses the RFC 1122 specification.</span></span> <span data-ttu-id="5e81d-111">Wenn der Wert **false** ist, werden dringende Daten im Modus gesendet, der von den von BSD abgeleiteten Systemen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e81d-111">If **false**, urgent data is sent in the mode used by BSD-derived systems.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e81d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e81d-112">Return value</span></span>

<span data-ttu-id="5e81d-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="5e81d-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="5e81d-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5e81d-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5e81d-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5e81d-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5e81d-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5e81d-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-117">0</span><span class="sxs-lookup"><span data-stu-id="5e81d-117">0</span></span>

<span data-ttu-id="5e81d-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e81d-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5e81d-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-120">1</span><span class="sxs-lookup"><span data-stu-id="5e81d-120">1</span></span>

<span data-ttu-id="5e81d-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e81d-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-123">64</span><span class="sxs-lookup"><span data-stu-id="5e81d-123">64</span></span>

<span data-ttu-id="5e81d-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e81d-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-126">65</span><span class="sxs-lookup"><span data-stu-id="5e81d-126">65</span></span>

<span data-ttu-id="5e81d-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="5e81d-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-129">66</span><span class="sxs-lookup"><span data-stu-id="5e81d-129">66</span></span>

<span data-ttu-id="5e81d-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="5e81d-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-132">67</span><span class="sxs-lookup"><span data-stu-id="5e81d-132">67</span></span>

<span data-ttu-id="5e81d-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5e81d-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="5e81d-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-135">68</span><span class="sxs-lookup"><span data-stu-id="5e81d-135">68</span></span>

<span data-ttu-id="5e81d-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5e81d-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-138">69</span><span class="sxs-lookup"><span data-stu-id="5e81d-138">69</span></span>

<span data-ttu-id="5e81d-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="5e81d-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="5e81d-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-141">70</span><span class="sxs-lookup"><span data-stu-id="5e81d-141">70</span></span>

<span data-ttu-id="5e81d-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5e81d-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="5e81d-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-144">71</span><span class="sxs-lookup"><span data-stu-id="5e81d-144">71</span></span>

<span data-ttu-id="5e81d-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5e81d-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-147">72</span><span class="sxs-lookup"><span data-stu-id="5e81d-147">72</span></span>

<span data-ttu-id="5e81d-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="5e81d-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="5e81d-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-150">73</span><span class="sxs-lookup"><span data-stu-id="5e81d-150">73</span></span>

<span data-ttu-id="5e81d-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="5e81d-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="5e81d-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-153">74</span><span class="sxs-lookup"><span data-stu-id="5e81d-153">74</span></span>

<span data-ttu-id="5e81d-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="5e81d-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-156">75</span><span class="sxs-lookup"><span data-stu-id="5e81d-156">75</span></span>

<span data-ttu-id="5e81d-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="5e81d-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="5e81d-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-159">76</span><span class="sxs-lookup"><span data-stu-id="5e81d-159">76</span></span>

<span data-ttu-id="5e81d-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="5e81d-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-162">77</span><span class="sxs-lookup"><span data-stu-id="5e81d-162">77</span></span>

<span data-ttu-id="5e81d-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="5e81d-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="5e81d-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-165">78</span><span class="sxs-lookup"><span data-stu-id="5e81d-165">78</span></span>

<span data-ttu-id="5e81d-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="5e81d-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="5e81d-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-168">79</span><span class="sxs-lookup"><span data-stu-id="5e81d-168">79</span></span>

<span data-ttu-id="5e81d-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="5e81d-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-171">80</span><span class="sxs-lookup"><span data-stu-id="5e81d-171">80</span></span>

<span data-ttu-id="5e81d-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-174">81</span><span class="sxs-lookup"><span data-stu-id="5e81d-174">81</span></span>

<span data-ttu-id="5e81d-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-177">82</span><span class="sxs-lookup"><span data-stu-id="5e81d-177">82</span></span>

<span data-ttu-id="5e81d-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="5e81d-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-180">83</span><span class="sxs-lookup"><span data-stu-id="5e81d-180">83</span></span>

<span data-ttu-id="5e81d-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-183">84</span><span class="sxs-lookup"><span data-stu-id="5e81d-183">84</span></span>

<span data-ttu-id="5e81d-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e81d-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-186">85</span><span class="sxs-lookup"><span data-stu-id="5e81d-186">85</span></span>

<span data-ttu-id="5e81d-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e81d-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-189">86</span><span class="sxs-lookup"><span data-stu-id="5e81d-189">86</span></span>

<span data-ttu-id="5e81d-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="5e81d-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="5e81d-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-192">87</span><span class="sxs-lookup"><span data-stu-id="5e81d-192">87</span></span>

<span data-ttu-id="5e81d-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="5e81d-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="5e81d-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-195">88</span><span class="sxs-lookup"><span data-stu-id="5e81d-195">88</span></span>

<span data-ttu-id="5e81d-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="5e81d-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="5e81d-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-198">89</span><span class="sxs-lookup"><span data-stu-id="5e81d-198">89</span></span>

<span data-ttu-id="5e81d-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="5e81d-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="5e81d-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-201">90</span><span class="sxs-lookup"><span data-stu-id="5e81d-201">90</span></span>

<span data-ttu-id="5e81d-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5e81d-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="5e81d-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-204">91</span><span class="sxs-lookup"><span data-stu-id="5e81d-204">91</span></span>

<span data-ttu-id="5e81d-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5e81d-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="5e81d-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-207">92</span><span class="sxs-lookup"><span data-stu-id="5e81d-207">92</span></span>

<span data-ttu-id="5e81d-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5e81d-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-210">93</span><span class="sxs-lookup"><span data-stu-id="5e81d-210">93</span></span>

<span data-ttu-id="5e81d-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-213">94</span><span class="sxs-lookup"><span data-stu-id="5e81d-213">94</span></span>

<span data-ttu-id="5e81d-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-216">95</span><span class="sxs-lookup"><span data-stu-id="5e81d-216">95</span></span>

<span data-ttu-id="5e81d-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-219">96</span><span class="sxs-lookup"><span data-stu-id="5e81d-219">96</span></span>

<span data-ttu-id="5e81d-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="5e81d-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-222">97</span><span class="sxs-lookup"><span data-stu-id="5e81d-222">97</span></span>

<span data-ttu-id="5e81d-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="5e81d-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-225">98</span><span class="sxs-lookup"><span data-stu-id="5e81d-225">98</span></span>

<span data-ttu-id="5e81d-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="5e81d-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5e81d-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-228">100</span><span class="sxs-lookup"><span data-stu-id="5e81d-228">100</span></span>

<span data-ttu-id="5e81d-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e81d-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e81d-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="5e81d-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5e81d-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="5e81d-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e81d-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e81d-232">Remarks</span></span>

<span data-ttu-id="5e81d-233">RFC 1122 und BSD interpretieren den dringenden Zeiger im TCP-Header und die Länge der dringenden Daten unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="5e81d-233">RFC 1122 and BSD interpret the urgent pointer in the TCP header and the length of the urgent data differently.</span></span> <span data-ttu-id="5e81d-234">Sie sind nicht interoperabel.</span><span class="sxs-lookup"><span data-stu-id="5e81d-234">They are not interoperable.</span></span> <span data-ttu-id="5e81d-235">Der Standardwert ist der BSD-Modus.</span><span class="sxs-lookup"><span data-stu-id="5e81d-235">The default is BSD mode.</span></span>

## <a name="examples"></a><span data-ttu-id="5e81d-236">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e81d-236">Examples</span></span>

<span data-ttu-id="5e81d-237">Das Beispiel [Modify Urgent Pointer use for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) VBScript konfiguriert einen Computer so, dass die Spezifikation RFC 1122 für dringende Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e81d-237">The [Modify Urgent Pointer Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) VBScript sample configures a computer to use the RFC 1122 specification for urgent data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e81d-238">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e81d-238">Requirements</span></span>



| <span data-ttu-id="5e81d-239">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e81d-239">Requirement</span></span> | <span data-ttu-id="5e81d-240">Wert</span><span class="sxs-lookup"><span data-stu-id="5e81d-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e81d-241">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e81d-241">Minimum supported client</span></span><br/> | <span data-ttu-id="5e81d-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e81d-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e81d-243">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e81d-243">Minimum supported server</span></span><br/> | <span data-ttu-id="5e81d-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e81d-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e81d-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e81d-245">Namespace</span></span><br/>                | <span data-ttu-id="5e81d-246">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5e81d-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e81d-247">MOF</span><span class="sxs-lookup"><span data-stu-id="5e81d-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e81d-248"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5e81d-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e81d-249">DLL</span><span class="sxs-lookup"><span data-stu-id="5e81d-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e81d-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e81d-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e81d-251">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e81d-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e81d-252">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="5e81d-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5e81d-253">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="5e81d-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="5e81d-254">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="5e81d-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="5e81d-255">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="5e81d-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="5e81d-256">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="5e81d-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

