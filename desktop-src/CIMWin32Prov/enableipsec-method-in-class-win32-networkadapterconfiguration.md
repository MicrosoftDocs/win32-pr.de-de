---
description: Die EnableIPSec-&\# 8194; Die WMI-Klassenmethode aktiviert die Internet Protokoll Sicherheit (Internet Protocol Security, IPSec) auf einem TCP/IP-fähigen Netzwerkadapter.
ms.assetid: 0a45d864-606d-4adb-9b51-62d46a0d68b1
ms.tgt_platform: multiple
title: EnableIPSec-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988d68f9939752e3c8c2c9ace063b895a2d3720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860956"
---
# <a name="enableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="a2fc6-103">EnableIPSec-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="a2fc6-103">EnableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="a2fc6-104">Die Methode " **EnableIPSec** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " ermöglicht die Internet Protokoll Sicherheit (Internet Protocol Security, IPSec) auf einem TCP/IP-fähigen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-104">The **EnableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables Internet Protocol security (IPsec) on a TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="a2fc6-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a2fc6-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fc6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2fc6-107">Syntax</span></span>


```mof
uint32 EnableIPSec(
  [in] string IPSecPermitTCPPorts[],
  [in] string IPSecPermitUDPPorts[],
  [in] string IPSecPermitIPProtocols[]
);
```



## <a name="parameters"></a><span data-ttu-id="a2fc6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2fc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2fc6-109">*IPSecPermitTCPPorts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2fc6-109">*IPSecPermitTCPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-110">Liste der Ports, denen die Zugriffsberechtigung für TCP erteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-110">List of ports to be granted access permission for TCP.</span></span> <span data-ttu-id="a2fc6-111">Ein numerischer Wert von 0 (null) gibt an, dass für alle Ports die Zugriffsberechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-111">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="a2fc6-112">Ein leeres Array gibt an, dass keinen Ports die Zugriffsberechtigung erteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-112">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-113">*IPSecPermitUDPPorts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2fc6-113">*IPSecPermitUDPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-114">Liste der Ports, denen die Zugriffsberechtigung für UDP erteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-114">List of ports to be granted access permission for UDP.</span></span> <span data-ttu-id="a2fc6-115">Ein numerischer Wert von 0 (null) gibt an, dass für alle Ports die Zugriffsberechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-115">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="a2fc6-116">Ein leeres Array gibt an, dass keinen Ports die Zugriffsberechtigung erteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-116">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-117">*Ipsecperentschärpprotokolle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2fc6-117">*IPSecPermitIPProtocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-118">Liste der Protokolle, die über die IP-Adresse ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-118">List of protocols permitted to run over the IP.</span></span> <span data-ttu-id="a2fc6-119">Ein numerischer Wert von 0 (null) gibt an, dass für alle Protokolle die Zugriffsberechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-119">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="a2fc6-120">Ein leeres Array gibt an, dass keinen Protokollen Zugriffsberechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-120">An empty array indicates that no protocols are granted access permission.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2fc6-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2fc6-121">Return value</span></span>

<span data-ttu-id="a2fc6-122">Gibt einen Wert von 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und jede andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="a2fc6-123">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a2fc6-124">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a2fc6-125">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-126">0</span><span class="sxs-lookup"><span data-stu-id="a2fc6-126">0</span></span>

<span data-ttu-id="a2fc6-127">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-128">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-129">1</span><span class="sxs-lookup"><span data-stu-id="a2fc6-129">1</span></span>

<span data-ttu-id="a2fc6-130">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-131">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-132">64</span><span class="sxs-lookup"><span data-stu-id="a2fc6-132">64</span></span>

<span data-ttu-id="a2fc6-133">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-134">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-135">65</span><span class="sxs-lookup"><span data-stu-id="a2fc6-135">65</span></span>

<span data-ttu-id="a2fc6-136">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-137">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-138">66</span><span class="sxs-lookup"><span data-stu-id="a2fc6-138">66</span></span>

<span data-ttu-id="a2fc6-139">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-140">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-141">67</span><span class="sxs-lookup"><span data-stu-id="a2fc6-141">67</span></span>

<span data-ttu-id="a2fc6-142">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-143">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-144">68</span><span class="sxs-lookup"><span data-stu-id="a2fc6-144">68</span></span>

<span data-ttu-id="a2fc6-145">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-146">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-147">69</span><span class="sxs-lookup"><span data-stu-id="a2fc6-147">69</span></span>

<span data-ttu-id="a2fc6-148">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-149">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-150">70</span><span class="sxs-lookup"><span data-stu-id="a2fc6-150">70</span></span>

<span data-ttu-id="a2fc6-151">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-152">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-153">71</span><span class="sxs-lookup"><span data-stu-id="a2fc6-153">71</span></span>

<span data-ttu-id="a2fc6-154">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-155">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-156">72</span><span class="sxs-lookup"><span data-stu-id="a2fc6-156">72</span></span>

<span data-ttu-id="a2fc6-157">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-158">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-159">73</span><span class="sxs-lookup"><span data-stu-id="a2fc6-159">73</span></span>

<span data-ttu-id="a2fc6-160">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-161">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-162">74</span><span class="sxs-lookup"><span data-stu-id="a2fc6-162">74</span></span>

<span data-ttu-id="a2fc6-163">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-164">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-165">75</span><span class="sxs-lookup"><span data-stu-id="a2fc6-165">75</span></span>

<span data-ttu-id="a2fc6-166">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="a2fc6-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-167">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-168">76</span><span class="sxs-lookup"><span data-stu-id="a2fc6-168">76</span></span>

<span data-ttu-id="a2fc6-169">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-170">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-171">77</span><span class="sxs-lookup"><span data-stu-id="a2fc6-171">77</span></span>

<span data-ttu-id="a2fc6-172">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-173">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-174">78</span><span class="sxs-lookup"><span data-stu-id="a2fc6-174">78</span></span>

<span data-ttu-id="a2fc6-175">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-176">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-177">79</span><span class="sxs-lookup"><span data-stu-id="a2fc6-177">79</span></span>

<span data-ttu-id="a2fc6-178">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-179">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-180">80</span><span class="sxs-lookup"><span data-stu-id="a2fc6-180">80</span></span>

<span data-ttu-id="a2fc6-181">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-182">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-183">81</span><span class="sxs-lookup"><span data-stu-id="a2fc6-183">81</span></span>

<span data-ttu-id="a2fc6-184">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-185">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-186">82</span><span class="sxs-lookup"><span data-stu-id="a2fc6-186">82</span></span>

<span data-ttu-id="a2fc6-187">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-188">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-189">83</span><span class="sxs-lookup"><span data-stu-id="a2fc6-189">83</span></span>

<span data-ttu-id="a2fc6-190">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-191">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-192">84</span><span class="sxs-lookup"><span data-stu-id="a2fc6-192">84</span></span>

<span data-ttu-id="a2fc6-193">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-194">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-195">85</span><span class="sxs-lookup"><span data-stu-id="a2fc6-195">85</span></span>

<span data-ttu-id="a2fc6-196">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-197">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-198">86</span><span class="sxs-lookup"><span data-stu-id="a2fc6-198">86</span></span>

<span data-ttu-id="a2fc6-199">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-200">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-201">87</span><span class="sxs-lookup"><span data-stu-id="a2fc6-201">87</span></span>

<span data-ttu-id="a2fc6-202">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-203">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-204">88</span><span class="sxs-lookup"><span data-stu-id="a2fc6-204">88</span></span>

<span data-ttu-id="a2fc6-205">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-206">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-207">89</span><span class="sxs-lookup"><span data-stu-id="a2fc6-207">89</span></span>

<span data-ttu-id="a2fc6-208">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-209">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-210">90</span><span class="sxs-lookup"><span data-stu-id="a2fc6-210">90</span></span>

<span data-ttu-id="a2fc6-211">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-212">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-213">91</span><span class="sxs-lookup"><span data-stu-id="a2fc6-213">91</span></span>

<span data-ttu-id="a2fc6-214">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-215">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-216">92</span><span class="sxs-lookup"><span data-stu-id="a2fc6-216">92</span></span>

<span data-ttu-id="a2fc6-217">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-218">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-219">93</span><span class="sxs-lookup"><span data-stu-id="a2fc6-219">93</span></span>

<span data-ttu-id="a2fc6-220">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-221">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-222">94</span><span class="sxs-lookup"><span data-stu-id="a2fc6-222">94</span></span>

<span data-ttu-id="a2fc6-223">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-224">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-225">95</span><span class="sxs-lookup"><span data-stu-id="a2fc6-225">95</span></span>

<span data-ttu-id="a2fc6-226">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-227">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-228">96</span><span class="sxs-lookup"><span data-stu-id="a2fc6-228">96</span></span>

<span data-ttu-id="a2fc6-229">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-230">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-231">97</span><span class="sxs-lookup"><span data-stu-id="a2fc6-231">97</span></span>

<span data-ttu-id="a2fc6-232">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-233">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-234">98</span><span class="sxs-lookup"><span data-stu-id="a2fc6-234">98</span></span>

<span data-ttu-id="a2fc6-235">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-235">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-236">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-237">100</span><span class="sxs-lookup"><span data-stu-id="a2fc6-237">100</span></span>

<span data-ttu-id="a2fc6-238">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-238">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc6-239">**Andere**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a2fc6-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="a2fc6-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2fc6-241">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2fc6-241">Remarks</span></span>

<span data-ttu-id="a2fc6-242">Ports werden nur gesichert, wenn die **ipfiltersecurityaktivierte** Eigenschaft in [**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md) den Wert " **true**" hat.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-242">Ports are secured only when the **IPFilterSecurityEnabled** property in [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) is **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="a2fc6-243">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2fc6-243">Examples</span></span>

<span data-ttu-id="a2fc6-244">Das Beispiel " [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript" in der TechNet Gallery verwendet **EnableIPSec** , um die IP-Sicherheit für einen Netzwerkadapter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-244">The [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript sample, on TechNet Gallery, uses **EnableIPSec** to enable IP security for a network adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2fc6-245">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2fc6-245">Requirements</span></span>



| <span data-ttu-id="a2fc6-246">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2fc6-246">Requirement</span></span> | <span data-ttu-id="a2fc6-247">Wert</span><span class="sxs-lookup"><span data-stu-id="a2fc6-247">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fc6-248">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-248">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fc6-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2fc6-249">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2fc6-250">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-250">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fc6-251">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2fc6-251">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2fc6-252">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2fc6-252">Namespace</span></span><br/>                | <span data-ttu-id="a2fc6-253">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2fc6-253">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2fc6-254">MOF</span><span class="sxs-lookup"><span data-stu-id="a2fc6-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2fc6-255"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a2fc6-255"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2fc6-256">DLL</span><span class="sxs-lookup"><span data-stu-id="a2fc6-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2fc6-257"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2fc6-257"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2fc6-258">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2fc6-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fc6-259">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a2fc6-259">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a2fc6-260">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="a2fc6-260">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="a2fc6-261">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="a2fc6-261">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="a2fc6-262">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="a2fc6-262">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="a2fc6-263">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="a2fc6-263">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

