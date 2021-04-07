---
description: Die statische Methode setnumforwardpacket WMI-Klasse wird verwendet, um die Anzahl der IP-Paket Header festzulegen, die der Routerpaketwarteschlange zugeordnet werden. Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen.
ms.assetid: cadc7565-4cad-4e0f-a1eb-bf99d333bb28
ms.tgt_platform: multiple
title: Setnumforwardpakete-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetNumForwardPackets
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f46ecd62766b5df642dff1e52614171a513a8fca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748568"
---
# <a name="setnumforwardpackets-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b8f49-104">Setnumforwardadapters-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8f49-104">SetNumForwardPackets method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b8f49-105">Die statische Methode **setnumforwardpacket** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Anzahl der IP-Paket Header festzulegen, die der Routerpaketwarteschlange zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-105">The **SetNumForwardPackets** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="b8f49-106">Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="b8f49-106">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span>

<span data-ttu-id="b8f49-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8f49-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b8f49-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b8f49-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f49-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8f49-109">Syntax</span></span>


```mof
uint32 SetNumForwardPackets(
  [in] uint32 NumForwardPackets
);
```



## <a name="parameters"></a><span data-ttu-id="b8f49-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8f49-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f49-111">*Numforwardpakete* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8f49-111">*NumForwardPackets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-112">Anzahl der IP-Paket Header, die der Routerpaketwarteschlange zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="b8f49-112">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="b8f49-113">Dies sollte mindestens so groß wie der Wert der Eigenschaft [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) sein, dividiert durch die maximale IP-Datengröße der mit dem Router verbundenen Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="b8f49-113">This should be at least as large as the value of the [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) property divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="b8f49-114">Er sollte nicht größer sein als der **ForwardBufferMemory** -Wert dividiert durch 256, da für jedes Paket mindestens 256 Bytes an vorwärts Puffer Arbeitsspeicher erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b8f49-114">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are required by each packet.</span></span> <span data-ttu-id="b8f49-115">Die optimale Anzahl von vorwärts Paketen für eine bestimmte **ForwardBufferMemory** -Größe hängt von der Art des Datenverkehrs ab, der im Netzwerk übertragen wird, und liegt zwischen diesen beiden Werten.</span><span class="sxs-lookup"><span data-stu-id="b8f49-115">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic carried on the network, and will be somewhere between these two values.</span></span> <span data-ttu-id="b8f49-116">Wenn der Router deaktiviert ist, wird dieser Parameter ignoriert, und es werden keine Header zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b8f49-116">If the router is disabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="b8f49-117">Gültiger Bereich: 1-0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="b8f49-117">Valid range: 1 - 0xFFFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f49-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8f49-118">Return value</span></span>

<span data-ttu-id="b8f49-119">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="b8f49-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="b8f49-120">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b8f49-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b8f49-121">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b8f49-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b8f49-122">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b8f49-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-123">0</span><span class="sxs-lookup"><span data-stu-id="b8f49-123">0</span></span>

<span data-ttu-id="b8f49-124">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8f49-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-125">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b8f49-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-126">1</span><span class="sxs-lookup"><span data-stu-id="b8f49-126">1</span></span>

<span data-ttu-id="b8f49-127">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8f49-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-128">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-129">64</span><span class="sxs-lookup"><span data-stu-id="b8f49-129">64</span></span>

<span data-ttu-id="b8f49-130">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8f49-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-131">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-132">65</span><span class="sxs-lookup"><span data-stu-id="b8f49-132">65</span></span>

<span data-ttu-id="b8f49-133">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b8f49-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-134">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-135">66</span><span class="sxs-lookup"><span data-stu-id="b8f49-135">66</span></span>

<span data-ttu-id="b8f49-136">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="b8f49-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-137">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-138">67</span><span class="sxs-lookup"><span data-stu-id="b8f49-138">67</span></span>

<span data-ttu-id="b8f49-139">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b8f49-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-140">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="b8f49-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-141">68</span><span class="sxs-lookup"><span data-stu-id="b8f49-141">68</span></span>

<span data-ttu-id="b8f49-142">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="b8f49-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-143">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-144">69</span><span class="sxs-lookup"><span data-stu-id="b8f49-144">69</span></span>

<span data-ttu-id="b8f49-145">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8f49-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-146">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="b8f49-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-147">70</span><span class="sxs-lookup"><span data-stu-id="b8f49-147">70</span></span>

<span data-ttu-id="b8f49-148">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b8f49-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-149">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="b8f49-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-150">71</span><span class="sxs-lookup"><span data-stu-id="b8f49-150">71</span></span>

<span data-ttu-id="b8f49-151">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b8f49-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-152">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-153">72</span><span class="sxs-lookup"><span data-stu-id="b8f49-153">72</span></span>

<span data-ttu-id="b8f49-154">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="b8f49-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-155">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="b8f49-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-156">73</span><span class="sxs-lookup"><span data-stu-id="b8f49-156">73</span></span>

<span data-ttu-id="b8f49-157">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="b8f49-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-158">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="b8f49-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-159">74</span><span class="sxs-lookup"><span data-stu-id="b8f49-159">74</span></span>

<span data-ttu-id="b8f49-160">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="b8f49-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-161">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-162">75</span><span class="sxs-lookup"><span data-stu-id="b8f49-162">75</span></span>

<span data-ttu-id="b8f49-163">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="b8f49-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-164">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="b8f49-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-165">76</span><span class="sxs-lookup"><span data-stu-id="b8f49-165">76</span></span>

<span data-ttu-id="b8f49-166">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="b8f49-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-167">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-168">77</span><span class="sxs-lookup"><span data-stu-id="b8f49-168">77</span></span>

<span data-ttu-id="b8f49-169">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="b8f49-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-170">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="b8f49-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-171">78</span><span class="sxs-lookup"><span data-stu-id="b8f49-171">78</span></span>

<span data-ttu-id="b8f49-172">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="b8f49-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-173">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="b8f49-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-174">79</span><span class="sxs-lookup"><span data-stu-id="b8f49-174">79</span></span>

<span data-ttu-id="b8f49-175">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="b8f49-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-176">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-177">80</span><span class="sxs-lookup"><span data-stu-id="b8f49-177">80</span></span>

<span data-ttu-id="b8f49-178">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-179">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-180">81</span><span class="sxs-lookup"><span data-stu-id="b8f49-180">81</span></span>

<span data-ttu-id="b8f49-181">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-182">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-183">82</span><span class="sxs-lookup"><span data-stu-id="b8f49-183">82</span></span>

<span data-ttu-id="b8f49-184">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-185">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="b8f49-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-186">83</span><span class="sxs-lookup"><span data-stu-id="b8f49-186">83</span></span>

<span data-ttu-id="b8f49-187">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-188">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-189">84</span><span class="sxs-lookup"><span data-stu-id="b8f49-189">84</span></span>

<span data-ttu-id="b8f49-190">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8f49-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-191">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-192">85</span><span class="sxs-lookup"><span data-stu-id="b8f49-192">85</span></span>

<span data-ttu-id="b8f49-193">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8f49-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-194">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-195">86</span><span class="sxs-lookup"><span data-stu-id="b8f49-195">86</span></span>

<span data-ttu-id="b8f49-196">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="b8f49-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-197">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="b8f49-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-198">87</span><span class="sxs-lookup"><span data-stu-id="b8f49-198">87</span></span>

<span data-ttu-id="b8f49-199">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="b8f49-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-200">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="b8f49-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-201">88</span><span class="sxs-lookup"><span data-stu-id="b8f49-201">88</span></span>

<span data-ttu-id="b8f49-202">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="b8f49-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-203">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="b8f49-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-204">89</span><span class="sxs-lookup"><span data-stu-id="b8f49-204">89</span></span>

<span data-ttu-id="b8f49-205">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="b8f49-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-206">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="b8f49-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-207">90</span><span class="sxs-lookup"><span data-stu-id="b8f49-207">90</span></span>

<span data-ttu-id="b8f49-208">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="b8f49-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-209">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="b8f49-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-210">91</span><span class="sxs-lookup"><span data-stu-id="b8f49-210">91</span></span>

<span data-ttu-id="b8f49-211">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b8f49-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-212">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="b8f49-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-213">92</span><span class="sxs-lookup"><span data-stu-id="b8f49-213">92</span></span>

<span data-ttu-id="b8f49-214">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b8f49-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-215">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-216">93</span><span class="sxs-lookup"><span data-stu-id="b8f49-216">93</span></span>

<span data-ttu-id="b8f49-217">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-218">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-219">94</span><span class="sxs-lookup"><span data-stu-id="b8f49-219">94</span></span>

<span data-ttu-id="b8f49-220">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-221">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-222">95</span><span class="sxs-lookup"><span data-stu-id="b8f49-222">95</span></span>

<span data-ttu-id="b8f49-223">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-224">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-225">96</span><span class="sxs-lookup"><span data-stu-id="b8f49-225">96</span></span>

<span data-ttu-id="b8f49-226">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-227">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="b8f49-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-228">97</span><span class="sxs-lookup"><span data-stu-id="b8f49-228">97</span></span>

<span data-ttu-id="b8f49-229">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="b8f49-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-230">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-231">98</span><span class="sxs-lookup"><span data-stu-id="b8f49-231">98</span></span>

<span data-ttu-id="b8f49-232">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="b8f49-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-233">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="b8f49-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-234">100</span><span class="sxs-lookup"><span data-stu-id="b8f49-234">100</span></span>

<span data-ttu-id="b8f49-235">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8f49-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-236">**Andere**</span><span class="sxs-lookup"><span data-stu-id="b8f49-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b8f49-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b8f49-238">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8f49-238">Examples</span></span>

<span data-ttu-id="b8f49-239">Im Beispiel [Modify the number of allowed Forward](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) Pakets VBScript wird die Anzahl von vorwärts Paketen konfiguriert, die der Routerpaketwarteschlange zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b8f49-239">The [Modify the Number of Allowed Forward Packets](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) VBScript sample configures the number of forward packets allocated to the router packet queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f49-240">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8f49-240">Requirements</span></span>



| <span data-ttu-id="b8f49-241">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8f49-241">Requirement</span></span> | <span data-ttu-id="b8f49-242">Wert</span><span class="sxs-lookup"><span data-stu-id="b8f49-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f49-243">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8f49-243">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f49-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8f49-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8f49-245">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8f49-245">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f49-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8f49-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8f49-247">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8f49-247">Namespace</span></span><br/>                | <span data-ttu-id="b8f49-248">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b8f49-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8f49-249">MOF</span><span class="sxs-lookup"><span data-stu-id="b8f49-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8f49-250"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b8f49-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8f49-251">DLL</span><span class="sxs-lookup"><span data-stu-id="b8f49-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8f49-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8f49-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f49-253">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8f49-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f49-254">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="b8f49-254">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b8f49-255">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="b8f49-255">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b8f49-256">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="b8f49-256">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b8f49-257">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="b8f49-257">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b8f49-258">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="b8f49-258">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

