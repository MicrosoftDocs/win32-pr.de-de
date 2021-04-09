---
description: Die SetTcpipNetbios-Methode wird verwendet, um den Standard Vorgang von NetBIOS über TCP/IP festzulegen.
ms.assetid: 2c639595-da13-400d-b4d0-432b39460554
ms.tgt_platform: multiple
title: SetTcpipNetbios-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpipNetbios
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ecab5918d00dc5f189464becc0252f2a8c0569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861727"
---
# <a name="settcpipnetbios-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="bf26f-103">SetTcpipNetbios-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="bf26f-103">SetTcpipNetbios method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="bf26f-104">Die **SetTcpipNetbios** -Methode wird verwendet, um den Standard Vorgang von NetBIOS über TCP/IP festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bf26f-104">The **SetTcpipNetbios** method is used to set the default operation of NetBIOS over TCP/IP.</span></span>

<span data-ttu-id="bf26f-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf26f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bf26f-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bf26f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf26f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf26f-107">Syntax</span></span>


```mof
uint32 SetTcpipNetbios(
  [in] uint32 TcpipNetbiosOptions
);
```



## <a name="parameters"></a><span data-ttu-id="bf26f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf26f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf26f-109">*TcpipNetbiosOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf26f-109">*TcpipNetbiosOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-110">-Wert, der die möglichen Einstellungen im Zusammenhang mit NetBIOS über TCP/IP angibt.</span><span class="sxs-lookup"><span data-stu-id="bf26f-110">Value that specifies the possible settings related to NetBIOS over TCP/IP.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="bf26f-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**Enablenetbiosviadhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="bf26f-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf26f-112">Aktivieren von NetBIOS über DHCP</span><span class="sxs-lookup"><span data-stu-id="bf26f-112">Enable Netbios via DHCP</span></span>

</dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="bf26f-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**Enablenetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="bf26f-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf26f-114">Aktivieren von NetBIOS</span><span class="sxs-lookup"><span data-stu-id="bf26f-114">Enable Netbios</span></span>

</dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="bf26f-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="bf26f-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bf26f-116">Deaktivieren von NetBIOS</span><span class="sxs-lookup"><span data-stu-id="bf26f-116">Disable Netbios</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf26f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf26f-117">Return value</span></span>

<span data-ttu-id="bf26f-118">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="bf26f-118">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="bf26f-119">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bf26f-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bf26f-120">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bf26f-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bf26f-121">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bf26f-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-122">0</span><span class="sxs-lookup"><span data-stu-id="bf26f-122">0</span></span>

<span data-ttu-id="bf26f-123">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="bf26f-123">Successful completion.</span></span> <span data-ttu-id="bf26f-124">Es ist kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf26f-124">No reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-125">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bf26f-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-126">1</span><span class="sxs-lookup"><span data-stu-id="bf26f-126">1</span></span>

<span data-ttu-id="bf26f-127">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="bf26f-127">Successful completion.</span></span> <span data-ttu-id="bf26f-128">Es ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf26f-128">Reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-129">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-130">64</span><span class="sxs-lookup"><span data-stu-id="bf26f-130">64</span></span>

<span data-ttu-id="bf26f-131">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf26f-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-132">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-133">65</span><span class="sxs-lookup"><span data-stu-id="bf26f-133">65</span></span>

<span data-ttu-id="bf26f-134">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bf26f-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-135">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-136">66</span><span class="sxs-lookup"><span data-stu-id="bf26f-136">66</span></span>

<span data-ttu-id="bf26f-137">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="bf26f-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-138">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-139">67</span><span class="sxs-lookup"><span data-stu-id="bf26f-139">67</span></span>

<span data-ttu-id="bf26f-140">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="bf26f-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-141">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="bf26f-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-142">68</span><span class="sxs-lookup"><span data-stu-id="bf26f-142">68</span></span>

<span data-ttu-id="bf26f-143">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="bf26f-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-144">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-145">69</span><span class="sxs-lookup"><span data-stu-id="bf26f-145">69</span></span>

<span data-ttu-id="bf26f-146">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="bf26f-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-147">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="bf26f-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-148">70</span><span class="sxs-lookup"><span data-stu-id="bf26f-148">70</span></span>

<span data-ttu-id="bf26f-149">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="bf26f-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-150">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="bf26f-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-151">71</span><span class="sxs-lookup"><span data-stu-id="bf26f-151">71</span></span>

<span data-ttu-id="bf26f-152">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="bf26f-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-153">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-154">72</span><span class="sxs-lookup"><span data-stu-id="bf26f-154">72</span></span>

<span data-ttu-id="bf26f-155">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="bf26f-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-156">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="bf26f-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-157">73</span><span class="sxs-lookup"><span data-stu-id="bf26f-157">73</span></span>

<span data-ttu-id="bf26f-158">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="bf26f-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-159">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="bf26f-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-160">74</span><span class="sxs-lookup"><span data-stu-id="bf26f-160">74</span></span>

<span data-ttu-id="bf26f-161">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="bf26f-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-162">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-163">75</span><span class="sxs-lookup"><span data-stu-id="bf26f-163">75</span></span>

<span data-ttu-id="bf26f-164">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="bf26f-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-165">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="bf26f-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-166">76</span><span class="sxs-lookup"><span data-stu-id="bf26f-166">76</span></span>

<span data-ttu-id="bf26f-167">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="bf26f-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-168">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-169">77</span><span class="sxs-lookup"><span data-stu-id="bf26f-169">77</span></span>

<span data-ttu-id="bf26f-170">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="bf26f-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-171">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="bf26f-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-172">78</span><span class="sxs-lookup"><span data-stu-id="bf26f-172">78</span></span>

<span data-ttu-id="bf26f-173">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="bf26f-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-174">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="bf26f-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-175">79</span><span class="sxs-lookup"><span data-stu-id="bf26f-175">79</span></span>

<span data-ttu-id="bf26f-176">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="bf26f-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-177">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-178">80</span><span class="sxs-lookup"><span data-stu-id="bf26f-178">80</span></span>

<span data-ttu-id="bf26f-179">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-180">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-181">81</span><span class="sxs-lookup"><span data-stu-id="bf26f-181">81</span></span>

<span data-ttu-id="bf26f-182">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-183">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-184">82</span><span class="sxs-lookup"><span data-stu-id="bf26f-184">82</span></span>

<span data-ttu-id="bf26f-185">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-186">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="bf26f-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-187">83</span><span class="sxs-lookup"><span data-stu-id="bf26f-187">83</span></span>

<span data-ttu-id="bf26f-188">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-189">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-190">84</span><span class="sxs-lookup"><span data-stu-id="bf26f-190">84</span></span>

<span data-ttu-id="bf26f-191">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf26f-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-192">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-193">85</span><span class="sxs-lookup"><span data-stu-id="bf26f-193">85</span></span>

<span data-ttu-id="bf26f-194">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf26f-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-195">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-196">86</span><span class="sxs-lookup"><span data-stu-id="bf26f-196">86</span></span>

<span data-ttu-id="bf26f-197">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="bf26f-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-198">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="bf26f-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-199">87</span><span class="sxs-lookup"><span data-stu-id="bf26f-199">87</span></span>

<span data-ttu-id="bf26f-200">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="bf26f-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-201">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="bf26f-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-202">88</span><span class="sxs-lookup"><span data-stu-id="bf26f-202">88</span></span>

<span data-ttu-id="bf26f-203">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="bf26f-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-204">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="bf26f-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-205">89</span><span class="sxs-lookup"><span data-stu-id="bf26f-205">89</span></span>

<span data-ttu-id="bf26f-206">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="bf26f-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-207">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="bf26f-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-208">90</span><span class="sxs-lookup"><span data-stu-id="bf26f-208">90</span></span>

<span data-ttu-id="bf26f-209">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="bf26f-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-210">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="bf26f-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-211">91</span><span class="sxs-lookup"><span data-stu-id="bf26f-211">91</span></span>

<span data-ttu-id="bf26f-212">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="bf26f-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-213">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="bf26f-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-214">92</span><span class="sxs-lookup"><span data-stu-id="bf26f-214">92</span></span>

<span data-ttu-id="bf26f-215">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bf26f-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-216">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-217">93</span><span class="sxs-lookup"><span data-stu-id="bf26f-217">93</span></span>

<span data-ttu-id="bf26f-218">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-219">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-220">94</span><span class="sxs-lookup"><span data-stu-id="bf26f-220">94</span></span>

<span data-ttu-id="bf26f-221">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-222">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-223">95</span><span class="sxs-lookup"><span data-stu-id="bf26f-223">95</span></span>

<span data-ttu-id="bf26f-224">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-225">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-226">96</span><span class="sxs-lookup"><span data-stu-id="bf26f-226">96</span></span>

<span data-ttu-id="bf26f-227">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-228">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="bf26f-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-229">97</span><span class="sxs-lookup"><span data-stu-id="bf26f-229">97</span></span>

<span data-ttu-id="bf26f-230">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="bf26f-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-231">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-232">98</span><span class="sxs-lookup"><span data-stu-id="bf26f-232">98</span></span>

<span data-ttu-id="bf26f-233">Nicht alle DHCP-Leases können freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="bf26f-233">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-234">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="bf26f-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-235">100</span><span class="sxs-lookup"><span data-stu-id="bf26f-235">100</span></span>

<span data-ttu-id="bf26f-236">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf26f-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="bf26f-237">**Andere**</span><span class="sxs-lookup"><span data-stu-id="bf26f-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="bf26f-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="bf26f-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bf26f-239">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf26f-239">Examples</span></span>

<span data-ttu-id="bf26f-240">Das Beispiel [NetBIOS-Verwendung auf einem Netzwerkadapter anpassen](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript aktiviert NetBIOS für einen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="bf26f-240">The [Modify NetBIOS Use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript sample enables NetBIOS for a network adapter.</span></span>

<span data-ttu-id="bf26f-241">Das [PowerShell-Beispiel Konfigurieren von iSCSI-Netzwerkkarten gemäß Microsoft Best Practices](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatisiert die Konfigurationseinstellungen für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="bf26f-241">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf26f-242">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf26f-242">Requirements</span></span>



| <span data-ttu-id="bf26f-243">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf26f-243">Requirement</span></span> | <span data-ttu-id="bf26f-244">Wert</span><span class="sxs-lookup"><span data-stu-id="bf26f-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf26f-245">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf26f-245">Minimum supported client</span></span><br/> | <span data-ttu-id="bf26f-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf26f-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf26f-247">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf26f-247">Minimum supported server</span></span><br/> | <span data-ttu-id="bf26f-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf26f-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf26f-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf26f-249">Namespace</span></span><br/>                | <span data-ttu-id="bf26f-250">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bf26f-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf26f-251">MOF</span><span class="sxs-lookup"><span data-stu-id="bf26f-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf26f-252"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bf26f-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf26f-253">DLL</span><span class="sxs-lookup"><span data-stu-id="bf26f-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf26f-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf26f-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf26f-255">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf26f-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf26f-256">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="bf26f-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="bf26f-257">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="bf26f-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="bf26f-258">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="bf26f-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="bf26f-259">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="bf26f-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="bf26f-260">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="bf26f-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

