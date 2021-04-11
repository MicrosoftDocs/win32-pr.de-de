---
description: Die statische Methode settcpmaxconnectretransmissions WMI-Klasse wird verwendet, um die Anzahl von Versuchen festzulegen, die TCP vor dem Abbruch erneut eine Verbindungsanforderung überträgt.
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Settcpmaxconnectretransmissions-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160d84c2a466bff34070a6dec4a34804d5a3a7fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127732"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="95882-103">Settcpmaxconnectretransmissions-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="95882-103">SetTcpMaxConnectRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="95882-104">Die statische Methode **settcpmaxconnectretransmissions** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Anzahl von Versuchen festzulegen, die TCP vor dem Abbruch erneut eine Verbindungsanforderung überträgt.</span><span class="sxs-lookup"><span data-stu-id="95882-104">The **SetTcpMaxConnectRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of attempts TCP will retransmit a connect request before aborting.</span></span>

<span data-ttu-id="95882-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="95882-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="95882-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="95882-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="95882-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95882-107">Syntax</span></span>


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="95882-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95882-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95882-109">*Tcpmaxconnectretransmissions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95882-109">*TcpMaxConnectRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95882-110">Anzahl der Versuche, die von TCP vor dem Abbruch erneut eine Verbindungsanforderung übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="95882-110">Number of attempts TCP will retransmit a connect request before aborting.</span></span> <span data-ttu-id="95882-111">Der gültige Wertebereich liegt zwischen 0 und 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="95882-111">The valid range for values is 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95882-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95882-112">Return value</span></span>

<span data-ttu-id="95882-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="95882-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="95882-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="95882-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="95882-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="95882-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="95882-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="95882-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="95882-117">0</span><span class="sxs-lookup"><span data-stu-id="95882-117">0</span></span>

<span data-ttu-id="95882-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95882-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="95882-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="95882-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="95882-120">1</span><span class="sxs-lookup"><span data-stu-id="95882-120">1</span></span>

<span data-ttu-id="95882-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95882-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="95882-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="95882-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="95882-123">64</span><span class="sxs-lookup"><span data-stu-id="95882-123">64</span></span>

<span data-ttu-id="95882-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95882-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="95882-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="95882-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="95882-126">65</span><span class="sxs-lookup"><span data-stu-id="95882-126">65</span></span>

<span data-ttu-id="95882-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="95882-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="95882-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="95882-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="95882-129">66</span><span class="sxs-lookup"><span data-stu-id="95882-129">66</span></span>

<span data-ttu-id="95882-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="95882-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="95882-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="95882-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="95882-132">67</span><span class="sxs-lookup"><span data-stu-id="95882-132">67</span></span>

<span data-ttu-id="95882-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="95882-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="95882-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="95882-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="95882-135">68</span><span class="sxs-lookup"><span data-stu-id="95882-135">68</span></span>

<span data-ttu-id="95882-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="95882-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="95882-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="95882-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="95882-138">69</span><span class="sxs-lookup"><span data-stu-id="95882-138">69</span></span>

<span data-ttu-id="95882-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="95882-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="95882-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="95882-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="95882-141">70</span><span class="sxs-lookup"><span data-stu-id="95882-141">70</span></span>

<span data-ttu-id="95882-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="95882-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="95882-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="95882-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="95882-144">71</span><span class="sxs-lookup"><span data-stu-id="95882-144">71</span></span>

<span data-ttu-id="95882-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="95882-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="95882-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="95882-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="95882-147">72</span><span class="sxs-lookup"><span data-stu-id="95882-147">72</span></span>

<span data-ttu-id="95882-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="95882-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="95882-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="95882-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="95882-150">73</span><span class="sxs-lookup"><span data-stu-id="95882-150">73</span></span>

<span data-ttu-id="95882-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="95882-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="95882-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="95882-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="95882-153">74</span><span class="sxs-lookup"><span data-stu-id="95882-153">74</span></span>

<span data-ttu-id="95882-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="95882-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="95882-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="95882-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="95882-156">75</span><span class="sxs-lookup"><span data-stu-id="95882-156">75</span></span>

<span data-ttu-id="95882-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="95882-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="95882-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="95882-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="95882-159">76</span><span class="sxs-lookup"><span data-stu-id="95882-159">76</span></span>

<span data-ttu-id="95882-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="95882-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="95882-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="95882-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="95882-162">77</span><span class="sxs-lookup"><span data-stu-id="95882-162">77</span></span>

<span data-ttu-id="95882-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="95882-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="95882-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="95882-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="95882-165">78</span><span class="sxs-lookup"><span data-stu-id="95882-165">78</span></span>

<span data-ttu-id="95882-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="95882-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="95882-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="95882-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="95882-168">79</span><span class="sxs-lookup"><span data-stu-id="95882-168">79</span></span>

<span data-ttu-id="95882-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="95882-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="95882-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="95882-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="95882-171">80</span><span class="sxs-lookup"><span data-stu-id="95882-171">80</span></span>

<span data-ttu-id="95882-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="95882-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="95882-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="95882-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="95882-174">81</span><span class="sxs-lookup"><span data-stu-id="95882-174">81</span></span>

<span data-ttu-id="95882-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="95882-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="95882-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="95882-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="95882-177">82</span><span class="sxs-lookup"><span data-stu-id="95882-177">82</span></span>

<span data-ttu-id="95882-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="95882-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="95882-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="95882-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="95882-180">83</span><span class="sxs-lookup"><span data-stu-id="95882-180">83</span></span>

<span data-ttu-id="95882-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="95882-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="95882-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="95882-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95882-183">84</span><span class="sxs-lookup"><span data-stu-id="95882-183">84</span></span>

<span data-ttu-id="95882-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="95882-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95882-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="95882-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95882-186">85</span><span class="sxs-lookup"><span data-stu-id="95882-186">85</span></span>

<span data-ttu-id="95882-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="95882-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95882-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="95882-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="95882-189">86</span><span class="sxs-lookup"><span data-stu-id="95882-189">86</span></span>

<span data-ttu-id="95882-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="95882-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="95882-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="95882-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="95882-192">87</span><span class="sxs-lookup"><span data-stu-id="95882-192">87</span></span>

<span data-ttu-id="95882-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="95882-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="95882-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="95882-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="95882-195">88</span><span class="sxs-lookup"><span data-stu-id="95882-195">88</span></span>

<span data-ttu-id="95882-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="95882-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="95882-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="95882-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="95882-198">89</span><span class="sxs-lookup"><span data-stu-id="95882-198">89</span></span>

<span data-ttu-id="95882-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="95882-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="95882-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="95882-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="95882-201">90</span><span class="sxs-lookup"><span data-stu-id="95882-201">90</span></span>

<span data-ttu-id="95882-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="95882-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="95882-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="95882-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="95882-204">91</span><span class="sxs-lookup"><span data-stu-id="95882-204">91</span></span>

<span data-ttu-id="95882-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="95882-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="95882-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="95882-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="95882-207">92</span><span class="sxs-lookup"><span data-stu-id="95882-207">92</span></span>

<span data-ttu-id="95882-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="95882-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="95882-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="95882-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="95882-210">93</span><span class="sxs-lookup"><span data-stu-id="95882-210">93</span></span>

<span data-ttu-id="95882-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="95882-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="95882-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95882-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="95882-213">94</span><span class="sxs-lookup"><span data-stu-id="95882-213">94</span></span>

<span data-ttu-id="95882-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="95882-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="95882-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="95882-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="95882-216">95</span><span class="sxs-lookup"><span data-stu-id="95882-216">95</span></span>

<span data-ttu-id="95882-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="95882-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="95882-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="95882-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="95882-219">96</span><span class="sxs-lookup"><span data-stu-id="95882-219">96</span></span>

<span data-ttu-id="95882-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="95882-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="95882-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="95882-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="95882-222">97</span><span class="sxs-lookup"><span data-stu-id="95882-222">97</span></span>

<span data-ttu-id="95882-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="95882-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="95882-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="95882-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="95882-225">98</span><span class="sxs-lookup"><span data-stu-id="95882-225">98</span></span>

<span data-ttu-id="95882-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="95882-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="95882-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="95882-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95882-228">100</span><span class="sxs-lookup"><span data-stu-id="95882-228">100</span></span>

<span data-ttu-id="95882-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="95882-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95882-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="95882-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="95882-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="95882-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95882-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95882-232">Remarks</span></span>

<span data-ttu-id="95882-233">Der anfängliche Neuübertragungs Timeout beträgt drei Sekunden und verdoppelt sich für jeden aufeinander folgenden Versuch.</span><span class="sxs-lookup"><span data-stu-id="95882-233">The initial retransmission timeout is three seconds, and doubles for each successive attempt.</span></span>

## <a name="examples"></a><span data-ttu-id="95882-234">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95882-234">Examples</span></span>

<span data-ttu-id="95882-235">Das Beispiel zum [Ändern der maximal zulässigen TCP-Verbindung reüberträgt](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript konfiguriert, wie oft TCP einen Verbindungsversuch erneut überträgt, bevor der Aufwand abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="95882-235">The [Modify the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript sample configures the number of times TCP will retransmit a connection attempt before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="95882-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95882-236">Requirements</span></span>



| <span data-ttu-id="95882-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95882-237">Requirement</span></span> | <span data-ttu-id="95882-238">Wert</span><span class="sxs-lookup"><span data-stu-id="95882-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95882-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95882-239">Minimum supported client</span></span><br/> | <span data-ttu-id="95882-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95882-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="95882-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95882-241">Minimum supported server</span></span><br/> | <span data-ttu-id="95882-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95882-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="95882-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="95882-243">Namespace</span></span><br/>                | <span data-ttu-id="95882-244">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="95882-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95882-245">MOF</span><span class="sxs-lookup"><span data-stu-id="95882-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95882-246"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="95882-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95882-247">DLL</span><span class="sxs-lookup"><span data-stu-id="95882-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95882-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95882-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95882-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95882-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95882-250">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="95882-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="95882-251">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="95882-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="95882-252">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="95882-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="95882-253">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="95882-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="95882-254">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="95882-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

