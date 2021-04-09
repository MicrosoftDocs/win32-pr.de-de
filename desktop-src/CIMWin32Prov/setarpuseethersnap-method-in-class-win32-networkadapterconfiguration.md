---
description: Die statische Methode SetArpUseEtherSNAP WMI-Klasse wird verwendet, um Ethernet-Paketen die Verwendung der 802,3-Snap-Codierung zu ermöglichen.
ms.assetid: 437954c0-ea6b-4559-a4cb-1f66630e70fe
ms.tgt_platform: multiple
title: SetArpUseEtherSNAP-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpUseEtherSNAP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52e3ce42948d5c40bbde3329b37ee3fa506c47ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861668"
---
# <a name="setarpuseethersnap-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="e9ea6-103">SetArpUseEtherSNAP-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="e9ea6-103">SetArpUseEtherSNAP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="e9ea6-104">Die statische Methode **SetArpUseEtherSNAP** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um Ethernet-Paketen die Verwendung der 802,3-Snap-Codierung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-104">The **SetArpUseEtherSNAP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable ethernet packets to use 802.3 SNAP encoding.</span></span>

<span data-ttu-id="e9ea6-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e9ea6-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e9ea6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ea6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9ea6-107">Syntax</span></span>


```mof
uint32 SetArpUseEtherSNAP(
  [in] boolean ArpUseEtherSNAP
);
```



## <a name="parameters"></a><span data-ttu-id="e9ea6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9ea6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ea6-109">*ArpUseEtherSNAP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9ea6-109">*ArpUseEtherSNAP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-110">Wenn der Wert **true** ist, wird TCP/IP für die Übertragung von Ethernet-Paketen mithilfe der 802,3-</span><span class="sxs-lookup"><span data-stu-id="e9ea6-110">If **true** enables TCP/IP to transmit Ethernet packets using 802.3 SNAP encoding.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ea6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9ea6-111">Return value</span></span>

<span data-ttu-id="e9ea6-112">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="e9ea6-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e9ea6-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e9ea6-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e9ea6-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e9ea6-115">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-116">0</span><span class="sxs-lookup"><span data-stu-id="e9ea6-116">0</span></span>

<span data-ttu-id="e9ea6-117">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-118">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-119">1</span><span class="sxs-lookup"><span data-stu-id="e9ea6-119">1</span></span>

<span data-ttu-id="e9ea6-120">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-121">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-122">64</span><span class="sxs-lookup"><span data-stu-id="e9ea6-122">64</span></span>

<span data-ttu-id="e9ea6-123">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-124">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-125">65</span><span class="sxs-lookup"><span data-stu-id="e9ea6-125">65</span></span>

<span data-ttu-id="e9ea6-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-127">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-128">66</span><span class="sxs-lookup"><span data-stu-id="e9ea6-128">66</span></span>

<span data-ttu-id="e9ea6-129">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-131">67</span><span class="sxs-lookup"><span data-stu-id="e9ea6-131">67</span></span>

<span data-ttu-id="e9ea6-132">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-133">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-134">68</span><span class="sxs-lookup"><span data-stu-id="e9ea6-134">68</span></span>

<span data-ttu-id="e9ea6-135">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-136">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-137">69</span><span class="sxs-lookup"><span data-stu-id="e9ea6-137">69</span></span>

<span data-ttu-id="e9ea6-138">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-139">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-140">70</span><span class="sxs-lookup"><span data-stu-id="e9ea6-140">70</span></span>

<span data-ttu-id="e9ea6-141">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-142">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-143">71</span><span class="sxs-lookup"><span data-stu-id="e9ea6-143">71</span></span>

<span data-ttu-id="e9ea6-144">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-145">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-146">72</span><span class="sxs-lookup"><span data-stu-id="e9ea6-146">72</span></span>

<span data-ttu-id="e9ea6-147">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-148">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-149">73</span><span class="sxs-lookup"><span data-stu-id="e9ea6-149">73</span></span>

<span data-ttu-id="e9ea6-150">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-151">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-152">74</span><span class="sxs-lookup"><span data-stu-id="e9ea6-152">74</span></span>

<span data-ttu-id="e9ea6-153">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-154">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-155">75</span><span class="sxs-lookup"><span data-stu-id="e9ea6-155">75</span></span>

<span data-ttu-id="e9ea6-156">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="e9ea6-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-157">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-158">76</span><span class="sxs-lookup"><span data-stu-id="e9ea6-158">76</span></span>

<span data-ttu-id="e9ea6-159">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-160">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-161">77</span><span class="sxs-lookup"><span data-stu-id="e9ea6-161">77</span></span>

<span data-ttu-id="e9ea6-162">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-163">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-164">78</span><span class="sxs-lookup"><span data-stu-id="e9ea6-164">78</span></span>

<span data-ttu-id="e9ea6-165">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-166">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-167">79</span><span class="sxs-lookup"><span data-stu-id="e9ea6-167">79</span></span>

<span data-ttu-id="e9ea6-168">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-169">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-170">80</span><span class="sxs-lookup"><span data-stu-id="e9ea6-170">80</span></span>

<span data-ttu-id="e9ea6-171">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-172">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-173">81</span><span class="sxs-lookup"><span data-stu-id="e9ea6-173">81</span></span>

<span data-ttu-id="e9ea6-174">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-175">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-176">82</span><span class="sxs-lookup"><span data-stu-id="e9ea6-176">82</span></span>

<span data-ttu-id="e9ea6-177">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-178">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-179">83</span><span class="sxs-lookup"><span data-stu-id="e9ea6-179">83</span></span>

<span data-ttu-id="e9ea6-180">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-181">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-182">84</span><span class="sxs-lookup"><span data-stu-id="e9ea6-182">84</span></span>

<span data-ttu-id="e9ea6-183">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-184">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-185">85</span><span class="sxs-lookup"><span data-stu-id="e9ea6-185">85</span></span>

<span data-ttu-id="e9ea6-186">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-187">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-188">86</span><span class="sxs-lookup"><span data-stu-id="e9ea6-188">86</span></span>

<span data-ttu-id="e9ea6-189">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-190">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-191">87</span><span class="sxs-lookup"><span data-stu-id="e9ea6-191">87</span></span>

<span data-ttu-id="e9ea6-192">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-193">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-194">88</span><span class="sxs-lookup"><span data-stu-id="e9ea6-194">88</span></span>

<span data-ttu-id="e9ea6-195">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-196">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-197">89</span><span class="sxs-lookup"><span data-stu-id="e9ea6-197">89</span></span>

<span data-ttu-id="e9ea6-198">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-199">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-200">90</span><span class="sxs-lookup"><span data-stu-id="e9ea6-200">90</span></span>

<span data-ttu-id="e9ea6-201">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-202">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-203">91</span><span class="sxs-lookup"><span data-stu-id="e9ea6-203">91</span></span>

<span data-ttu-id="e9ea6-204">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-205">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-206">92</span><span class="sxs-lookup"><span data-stu-id="e9ea6-206">92</span></span>

<span data-ttu-id="e9ea6-207">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-208">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-209">93</span><span class="sxs-lookup"><span data-stu-id="e9ea6-209">93</span></span>

<span data-ttu-id="e9ea6-210">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-211">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-212">94</span><span class="sxs-lookup"><span data-stu-id="e9ea6-212">94</span></span>

<span data-ttu-id="e9ea6-213">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-214">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-215">95</span><span class="sxs-lookup"><span data-stu-id="e9ea6-215">95</span></span>

<span data-ttu-id="e9ea6-216">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-217">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-218">96</span><span class="sxs-lookup"><span data-stu-id="e9ea6-218">96</span></span>

<span data-ttu-id="e9ea6-219">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-220">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-221">97</span><span class="sxs-lookup"><span data-stu-id="e9ea6-221">97</span></span>

<span data-ttu-id="e9ea6-222">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-223">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-224">98</span><span class="sxs-lookup"><span data-stu-id="e9ea6-224">98</span></span>

<span data-ttu-id="e9ea6-225">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-226">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-227">100</span><span class="sxs-lookup"><span data-stu-id="e9ea6-227">100</span></span>

<span data-ttu-id="e9ea6-228">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-229">**Andere**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="e9ea6-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ea6-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9ea6-231">Remarks</span></span>

<span data-ttu-id="e9ea6-232">Standardmäßig überträgt der Stapel Pakete im Digital, Intel, Xerox (Dix) Ethernet-Format.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-232">By default, the stack transmits packets in Digital, Intel, Xerox (DIX) Ethernet format.</span></span> <span data-ttu-id="e9ea6-233">Beide Formate werden immer empfangen.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-233">It always receives both formats.</span></span>

## <a name="examples"></a><span data-ttu-id="e9ea6-234">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9ea6-234">Examples</span></span>

<span data-ttu-id="e9ea6-235">Das Codebeispiel zum [Ändern von ARP-Abfragen zur Verwendung von ethersnap](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript in der TechNet Gallery verwendet **SetArpUseEtherSNAP** zum Konfigurieren der Netzwerkadapter auf einem Computer für die Verwendung der 802,3-Snap-Codierung für Ethernet-Pakete.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-235">The [Modify ARP Queries to Use EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript code sample on TechNet Gallery uses **SetArpUseEtherSNAP** to configure the network adapters on a computer to use 802.3 SNAP encoding for Ethernet packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ea6-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9ea6-236">Requirements</span></span>



| <span data-ttu-id="e9ea6-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9ea6-237">Requirement</span></span> | <span data-ttu-id="e9ea6-238">Wert</span><span class="sxs-lookup"><span data-stu-id="e9ea6-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ea6-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9ea6-239">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ea6-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9ea6-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9ea6-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9ea6-241">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ea6-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9ea6-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9ea6-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9ea6-243">Namespace</span></span><br/>                | <span data-ttu-id="e9ea6-244">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e9ea6-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9ea6-245">MOF</span><span class="sxs-lookup"><span data-stu-id="e9ea6-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9ea6-246"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e9ea6-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9ea6-247">DLL</span><span class="sxs-lookup"><span data-stu-id="e9ea6-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9ea6-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9ea6-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ea6-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9ea6-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ea6-250">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="e9ea6-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e9ea6-251">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="e9ea6-252">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e9ea6-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="e9ea6-253">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="e9ea6-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="e9ea6-254">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="e9ea6-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

