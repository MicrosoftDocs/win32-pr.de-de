---
description: Die statische Methode setigmplevel WMI-Klasse wird verwendet, um das Ausmaß festzulegen, in dem das System IP-Multicasting unterstützt und am Internet Group Management-Protokoll teilnimmt.
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Setigmplevel-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97ead4df1d45b110c3d0a91976dc8eca6ffd72c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523787"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="cb94b-103">Setigmplevel-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="cb94b-103">SetIGMPLevel method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="cb94b-104">Die statische Methode **setigmplevel** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um das Ausmaß festzulegen, in dem das System IP-Multicasting unterstützt und am Internet Group Management-Protokoll teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="cb94b-104">The **SetIGMPLevel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span>

<span data-ttu-id="cb94b-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb94b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cb94b-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cb94b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb94b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb94b-107">Syntax</span></span>


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a><span data-ttu-id="cb94b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb94b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb94b-109">*IGMPLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb94b-109">*IGMPLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-110">Datentyp: **Integer**</span><span class="sxs-lookup"><span data-stu-id="cb94b-110">Data type: **Integer**</span></span>

<span data-ttu-id="cb94b-111">Legt die Ebene fest, bei der das System IP-Multicast unterstützt und am Internet Group Management-Protokoll teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="cb94b-111">Sets the level at which the system supports IP multicast and participates in the Internet Group Management Protocol.</span></span> <span data-ttu-id="cb94b-112">Auf Ebene 0 bietet das System keine Multicast Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="cb94b-112">At level 0, the system provides no multicast support.</span></span> <span data-ttu-id="cb94b-113">Auf Ebene 1 kann das System nur IP-Multicast Pakete senden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-113">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="cb94b-114">Auf Ebene 2 kann das System IP-Multicast Pakete senden und für den Empfang von Multicast Paketen vollständig an IGMP teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="cb94b-114">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="cb94b-115">**Kein Multicast** (0)</span><span class="sxs-lookup"><span data-stu-id="cb94b-115">**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="cb94b-116">**IP-Multicast** (1)</span><span class="sxs-lookup"><span data-stu-id="cb94b-116">**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="cb94b-117">**IP-& IGMP-Multicast** (2)</span><span class="sxs-lookup"><span data-stu-id="cb94b-117">**IP & IGMP multicast** (2)</span></span>


<span data-ttu-id="cb94b-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cb94b-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="cb94b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb94b-119">Return value</span></span>

<span data-ttu-id="cb94b-120">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="cb94b-120">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="cb94b-121">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cb94b-121">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cb94b-122">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cb94b-122">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cb94b-123">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="cb94b-123">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-124">0</span><span class="sxs-lookup"><span data-stu-id="cb94b-124">0</span></span>

<span data-ttu-id="cb94b-125">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb94b-125">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-126">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="cb94b-126">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-127">1</span><span class="sxs-lookup"><span data-stu-id="cb94b-127">1</span></span>

<span data-ttu-id="cb94b-128">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb94b-128">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-129">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-130">64</span><span class="sxs-lookup"><span data-stu-id="cb94b-130">64</span></span>

<span data-ttu-id="cb94b-131">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb94b-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-132">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-133">65</span><span class="sxs-lookup"><span data-stu-id="cb94b-133">65</span></span>

<span data-ttu-id="cb94b-134">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cb94b-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-135">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-136">66</span><span class="sxs-lookup"><span data-stu-id="cb94b-136">66</span></span>

<span data-ttu-id="cb94b-137">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="cb94b-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-138">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-139">67</span><span class="sxs-lookup"><span data-stu-id="cb94b-139">67</span></span>

<span data-ttu-id="cb94b-140">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cb94b-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-141">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="cb94b-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-142">68</span><span class="sxs-lookup"><span data-stu-id="cb94b-142">68</span></span>

<span data-ttu-id="cb94b-143">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="cb94b-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-144">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-145">69</span><span class="sxs-lookup"><span data-stu-id="cb94b-145">69</span></span>

<span data-ttu-id="cb94b-146">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="cb94b-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-147">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="cb94b-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-148">70</span><span class="sxs-lookup"><span data-stu-id="cb94b-148">70</span></span>

<span data-ttu-id="cb94b-149">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="cb94b-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-150">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="cb94b-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-151">71</span><span class="sxs-lookup"><span data-stu-id="cb94b-151">71</span></span>

<span data-ttu-id="cb94b-152">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="cb94b-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-153">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-154">72</span><span class="sxs-lookup"><span data-stu-id="cb94b-154">72</span></span>

<span data-ttu-id="cb94b-155">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="cb94b-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-156">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="cb94b-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-157">73</span><span class="sxs-lookup"><span data-stu-id="cb94b-157">73</span></span>

<span data-ttu-id="cb94b-158">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="cb94b-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-159">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="cb94b-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-160">74</span><span class="sxs-lookup"><span data-stu-id="cb94b-160">74</span></span>

<span data-ttu-id="cb94b-161">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="cb94b-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-162">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-163">75</span><span class="sxs-lookup"><span data-stu-id="cb94b-163">75</span></span>

<span data-ttu-id="cb94b-164">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="cb94b-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-165">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="cb94b-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-166">76</span><span class="sxs-lookup"><span data-stu-id="cb94b-166">76</span></span>

<span data-ttu-id="cb94b-167">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="cb94b-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-168">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-169">77</span><span class="sxs-lookup"><span data-stu-id="cb94b-169">77</span></span>

<span data-ttu-id="cb94b-170">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="cb94b-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-171">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="cb94b-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-172">78</span><span class="sxs-lookup"><span data-stu-id="cb94b-172">78</span></span>

<span data-ttu-id="cb94b-173">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="cb94b-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-174">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="cb94b-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-175">79</span><span class="sxs-lookup"><span data-stu-id="cb94b-175">79</span></span>

<span data-ttu-id="cb94b-176">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="cb94b-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-177">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-178">80</span><span class="sxs-lookup"><span data-stu-id="cb94b-178">80</span></span>

<span data-ttu-id="cb94b-179">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-180">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-181">81</span><span class="sxs-lookup"><span data-stu-id="cb94b-181">81</span></span>

<span data-ttu-id="cb94b-182">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-183">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-184">82</span><span class="sxs-lookup"><span data-stu-id="cb94b-184">82</span></span>

<span data-ttu-id="cb94b-185">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-186">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="cb94b-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-187">83</span><span class="sxs-lookup"><span data-stu-id="cb94b-187">83</span></span>

<span data-ttu-id="cb94b-188">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-189">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-190">84</span><span class="sxs-lookup"><span data-stu-id="cb94b-190">84</span></span>

<span data-ttu-id="cb94b-191">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb94b-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-192">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-193">85</span><span class="sxs-lookup"><span data-stu-id="cb94b-193">85</span></span>

<span data-ttu-id="cb94b-194">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb94b-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-195">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-196">86</span><span class="sxs-lookup"><span data-stu-id="cb94b-196">86</span></span>

<span data-ttu-id="cb94b-197">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="cb94b-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-198">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="cb94b-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-199">87</span><span class="sxs-lookup"><span data-stu-id="cb94b-199">87</span></span>

<span data-ttu-id="cb94b-200">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="cb94b-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-201">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="cb94b-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-202">88</span><span class="sxs-lookup"><span data-stu-id="cb94b-202">88</span></span>

<span data-ttu-id="cb94b-203">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="cb94b-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-204">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="cb94b-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-205">89</span><span class="sxs-lookup"><span data-stu-id="cb94b-205">89</span></span>

<span data-ttu-id="cb94b-206">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="cb94b-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-207">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="cb94b-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-208">90</span><span class="sxs-lookup"><span data-stu-id="cb94b-208">90</span></span>

<span data-ttu-id="cb94b-209">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="cb94b-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-210">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="cb94b-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-211">91</span><span class="sxs-lookup"><span data-stu-id="cb94b-211">91</span></span>

<span data-ttu-id="cb94b-212">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="cb94b-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-213">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="cb94b-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-214">92</span><span class="sxs-lookup"><span data-stu-id="cb94b-214">92</span></span>

<span data-ttu-id="cb94b-215">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cb94b-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-216">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-217">93</span><span class="sxs-lookup"><span data-stu-id="cb94b-217">93</span></span>

<span data-ttu-id="cb94b-218">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-219">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-220">94</span><span class="sxs-lookup"><span data-stu-id="cb94b-220">94</span></span>

<span data-ttu-id="cb94b-221">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-222">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-223">95</span><span class="sxs-lookup"><span data-stu-id="cb94b-223">95</span></span>

<span data-ttu-id="cb94b-224">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-225">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-226">96</span><span class="sxs-lookup"><span data-stu-id="cb94b-226">96</span></span>

<span data-ttu-id="cb94b-227">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-228">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="cb94b-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-229">97</span><span class="sxs-lookup"><span data-stu-id="cb94b-229">97</span></span>

<span data-ttu-id="cb94b-230">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="cb94b-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-231">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-232">98</span><span class="sxs-lookup"><span data-stu-id="cb94b-232">98</span></span>

<span data-ttu-id="cb94b-233">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="cb94b-233">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-234">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="cb94b-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-235">100</span><span class="sxs-lookup"><span data-stu-id="cb94b-235">100</span></span>

<span data-ttu-id="cb94b-236">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb94b-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cb94b-237">**Andere**</span><span class="sxs-lookup"><span data-stu-id="cb94b-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="cb94b-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="cb94b-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cb94b-239">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb94b-239">Examples</span></span>

<span data-ttu-id="cb94b-240">Das Beispiel [Ändern des IGMP-Levels für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript deaktiviert IGMP-Multicasting auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="cb94b-240">The [Modify the IGMP Level for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript sample disables IGMP multicasting on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb94b-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb94b-241">Requirements</span></span>



| <span data-ttu-id="cb94b-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb94b-242">Requirement</span></span> | <span data-ttu-id="cb94b-243">Wert</span><span class="sxs-lookup"><span data-stu-id="cb94b-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb94b-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb94b-244">Minimum supported client</span></span><br/> | <span data-ttu-id="cb94b-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb94b-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb94b-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb94b-246">Minimum supported server</span></span><br/> | <span data-ttu-id="cb94b-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb94b-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb94b-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb94b-248">Namespace</span></span><br/>                | <span data-ttu-id="cb94b-249">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cb94b-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb94b-250">MOF</span><span class="sxs-lookup"><span data-stu-id="cb94b-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb94b-251"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cb94b-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb94b-252">DLL</span><span class="sxs-lookup"><span data-stu-id="cb94b-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb94b-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb94b-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb94b-254">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb94b-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb94b-255">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="cb94b-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cb94b-256">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="cb94b-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="cb94b-257">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="cb94b-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="cb94b-258">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="cb94b-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="cb94b-259">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="cb94b-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

