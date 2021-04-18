---
description: Die statische Methode setkeepalivetime WMI-Klasse wird verwendet, um festzulegen, wie oft TCP versucht, zu überprüfen, ob eine Leerlaufverbindung weiterhin verfügbar ist, indem ein Keep-Alive-Paket gesendet wird.
ms.assetid: 8640b109-928b-46fc-8dce-9ee5dcbd94e3
ms.tgt_platform: multiple
title: Setkeepalivetime-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dc2674f3c09626749b4c7ac6151349401670e27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341144"
---
# <a name="setkeepalivetime-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="37dd4-103">Setkeepalivetime-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="37dd4-103">SetKeepAliveTime method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="37dd4-104">Die statische Methode **setkeepalivetime** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um festzulegen, wie oft TCP versucht, zu überprüfen, ob eine Leerlaufverbindung weiterhin verfügbar ist, indem ein Keep-Alive-Paket gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="37dd4-104">The **SetKeepAliveTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span>

<span data-ttu-id="37dd4-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="37dd4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="37dd4-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="37dd4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="37dd4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37dd4-107">Syntax</span></span>


```mof
uint32 SetKeepAliveTime(
  [in] uint32 KeepAliveTime
);
```



## <a name="parameters"></a><span data-ttu-id="37dd4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37dd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37dd4-109">*KeepAliveTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37dd4-109">*KeepAliveTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-110">Intervall (in Millisekunden): das TCP wartet darauf, zu überprüfen, ob eine Verbindung im Leerlauf noch verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37dd4-110">Interval, in milliseconds, the TCP waits to check that an idle connection is still available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37dd4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37dd4-111">Return value</span></span>

<span data-ttu-id="37dd4-112">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="37dd4-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="37dd4-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="37dd4-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="37dd4-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="37dd4-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="37dd4-115">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="37dd4-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-116">0</span><span class="sxs-lookup"><span data-stu-id="37dd4-116">0</span></span>

<span data-ttu-id="37dd4-117">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37dd4-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-118">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="37dd4-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-119">1</span><span class="sxs-lookup"><span data-stu-id="37dd4-119">1</span></span>

<span data-ttu-id="37dd4-120">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37dd4-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-121">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-122">64</span><span class="sxs-lookup"><span data-stu-id="37dd4-122">64</span></span>

<span data-ttu-id="37dd4-123">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37dd4-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-124">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-125">65</span><span class="sxs-lookup"><span data-stu-id="37dd4-125">65</span></span>

<span data-ttu-id="37dd4-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="37dd4-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-127">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-128">66</span><span class="sxs-lookup"><span data-stu-id="37dd4-128">66</span></span>

<span data-ttu-id="37dd4-129">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="37dd4-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-131">67</span><span class="sxs-lookup"><span data-stu-id="37dd4-131">67</span></span>

<span data-ttu-id="37dd4-132">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="37dd4-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-133">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="37dd4-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-134">68</span><span class="sxs-lookup"><span data-stu-id="37dd4-134">68</span></span>

<span data-ttu-id="37dd4-135">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="37dd4-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-136">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-137">69</span><span class="sxs-lookup"><span data-stu-id="37dd4-137">69</span></span>

<span data-ttu-id="37dd4-138">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="37dd4-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-139">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="37dd4-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-140">70</span><span class="sxs-lookup"><span data-stu-id="37dd4-140">70</span></span>

<span data-ttu-id="37dd4-141">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="37dd4-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-142">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="37dd4-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-143">71</span><span class="sxs-lookup"><span data-stu-id="37dd4-143">71</span></span>

<span data-ttu-id="37dd4-144">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="37dd4-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-145">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-146">72</span><span class="sxs-lookup"><span data-stu-id="37dd4-146">72</span></span>

<span data-ttu-id="37dd4-147">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="37dd4-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-148">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="37dd4-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-149">73</span><span class="sxs-lookup"><span data-stu-id="37dd4-149">73</span></span>

<span data-ttu-id="37dd4-150">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="37dd4-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-151">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="37dd4-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-152">74</span><span class="sxs-lookup"><span data-stu-id="37dd4-152">74</span></span>

<span data-ttu-id="37dd4-153">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="37dd4-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-154">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-155">75</span><span class="sxs-lookup"><span data-stu-id="37dd4-155">75</span></span>

<span data-ttu-id="37dd4-156">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="37dd4-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-157">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="37dd4-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-158">76</span><span class="sxs-lookup"><span data-stu-id="37dd4-158">76</span></span>

<span data-ttu-id="37dd4-159">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="37dd4-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-160">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-161">77</span><span class="sxs-lookup"><span data-stu-id="37dd4-161">77</span></span>

<span data-ttu-id="37dd4-162">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="37dd4-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-163">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="37dd4-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-164">78</span><span class="sxs-lookup"><span data-stu-id="37dd4-164">78</span></span>

<span data-ttu-id="37dd4-165">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="37dd4-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-166">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="37dd4-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-167">79</span><span class="sxs-lookup"><span data-stu-id="37dd4-167">79</span></span>

<span data-ttu-id="37dd4-168">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="37dd4-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-169">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-170">80</span><span class="sxs-lookup"><span data-stu-id="37dd4-170">80</span></span>

<span data-ttu-id="37dd4-171">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-172">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-173">81</span><span class="sxs-lookup"><span data-stu-id="37dd4-173">81</span></span>

<span data-ttu-id="37dd4-174">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-175">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-176">82</span><span class="sxs-lookup"><span data-stu-id="37dd4-176">82</span></span>

<span data-ttu-id="37dd4-177">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-178">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="37dd4-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-179">83</span><span class="sxs-lookup"><span data-stu-id="37dd4-179">83</span></span>

<span data-ttu-id="37dd4-180">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-181">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-182">84</span><span class="sxs-lookup"><span data-stu-id="37dd4-182">84</span></span>

<span data-ttu-id="37dd4-183">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37dd4-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-184">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-185">85</span><span class="sxs-lookup"><span data-stu-id="37dd4-185">85</span></span>

<span data-ttu-id="37dd4-186">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37dd4-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-187">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-188">86</span><span class="sxs-lookup"><span data-stu-id="37dd4-188">86</span></span>

<span data-ttu-id="37dd4-189">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="37dd4-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-190">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="37dd4-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-191">87</span><span class="sxs-lookup"><span data-stu-id="37dd4-191">87</span></span>

<span data-ttu-id="37dd4-192">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="37dd4-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-193">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="37dd4-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-194">88</span><span class="sxs-lookup"><span data-stu-id="37dd4-194">88</span></span>

<span data-ttu-id="37dd4-195">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="37dd4-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-196">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="37dd4-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-197">89</span><span class="sxs-lookup"><span data-stu-id="37dd4-197">89</span></span>

<span data-ttu-id="37dd4-198">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="37dd4-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-199">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="37dd4-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-200">90</span><span class="sxs-lookup"><span data-stu-id="37dd4-200">90</span></span>

<span data-ttu-id="37dd4-201">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="37dd4-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-202">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="37dd4-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-203">91</span><span class="sxs-lookup"><span data-stu-id="37dd4-203">91</span></span>

<span data-ttu-id="37dd4-204">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="37dd4-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-205">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="37dd4-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-206">92</span><span class="sxs-lookup"><span data-stu-id="37dd4-206">92</span></span>

<span data-ttu-id="37dd4-207">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37dd4-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-208">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-209">93</span><span class="sxs-lookup"><span data-stu-id="37dd4-209">93</span></span>

<span data-ttu-id="37dd4-210">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-211">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-212">94</span><span class="sxs-lookup"><span data-stu-id="37dd4-212">94</span></span>

<span data-ttu-id="37dd4-213">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-214">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-215">95</span><span class="sxs-lookup"><span data-stu-id="37dd4-215">95</span></span>

<span data-ttu-id="37dd4-216">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-217">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-218">96</span><span class="sxs-lookup"><span data-stu-id="37dd4-218">96</span></span>

<span data-ttu-id="37dd4-219">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-220">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="37dd4-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-221">97</span><span class="sxs-lookup"><span data-stu-id="37dd4-221">97</span></span>

<span data-ttu-id="37dd4-222">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="37dd4-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-223">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-224">98</span><span class="sxs-lookup"><span data-stu-id="37dd4-224">98</span></span>

<span data-ttu-id="37dd4-225">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-226">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="37dd4-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-227">100</span><span class="sxs-lookup"><span data-stu-id="37dd4-227">100</span></span>

<span data-ttu-id="37dd4-228">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37dd4-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="37dd4-229">**Andere**</span><span class="sxs-lookup"><span data-stu-id="37dd4-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="37dd4-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="37dd4-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37dd4-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37dd4-231">Remarks</span></span>

<span data-ttu-id="37dd4-232">Wenn das Remote System immer noch erreichbar ist und funktionsfähig ist, wird die Keep-Alive-Übertragung anerkannt.</span><span class="sxs-lookup"><span data-stu-id="37dd4-232">If the remote system is still reachable and functioning, it will acknowledge the Keep Alive transmission.</span></span> <span data-ttu-id="37dd4-233">Keep-Alive-Pakete werden standardmäßig nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="37dd4-233">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="37dd4-234">Diese Funktion kann in einer Verbindung von einer Anwendung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="37dd4-234">This feature may be enabled in a connection by an application.</span></span>

## <a name="examples"></a><span data-ttu-id="37dd4-235">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37dd4-235">Examples</span></span>

<span data-ttu-id="37dd4-236">Im Beispiel zum [Ändern der Keep-Alive-Zeit für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) mit VBScript wird die Keep-Alive-Zeit für alle Netzwerkadapter auf einem Computer auf 300.000 Millisekunden (5 Minuten) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="37dd4-236">The [Modify Keep Alive Time for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) VBScript sample configures the keep alive time for all network adapters on a computer to 300,000 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="37dd4-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37dd4-237">Requirements</span></span>



| <span data-ttu-id="37dd4-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37dd4-238">Requirement</span></span> | <span data-ttu-id="37dd4-239">Wert</span><span class="sxs-lookup"><span data-stu-id="37dd4-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37dd4-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37dd4-240">Minimum supported client</span></span><br/> | <span data-ttu-id="37dd4-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37dd4-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37dd4-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37dd4-242">Minimum supported server</span></span><br/> | <span data-ttu-id="37dd4-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37dd4-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37dd4-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="37dd4-244">Namespace</span></span><br/>                | <span data-ttu-id="37dd4-245">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="37dd4-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37dd4-246">MOF</span><span class="sxs-lookup"><span data-stu-id="37dd4-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37dd4-247"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37dd4-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37dd4-248">DLL</span><span class="sxs-lookup"><span data-stu-id="37dd4-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37dd4-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37dd4-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37dd4-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37dd4-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37dd4-251">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="37dd4-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="37dd4-252">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="37dd4-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="37dd4-253">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="37dd4-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="37dd4-254">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="37dd4-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="37dd4-255">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="37dd4-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

