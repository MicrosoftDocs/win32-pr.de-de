---
description: Die statische Methode SetTcpNumConnections WMI-Klasse wird verwendet, um die maximale Anzahl von Verbindungen festzulegen, die TCP möglicherweise gleichzeitig geöffnet hat.
ms.assetid: 50458161-1f28-47f9-b395-09586e859d5d
ms.tgt_platform: multiple
title: SetTcpNumConnections-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpNumConnections
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5708c7ce80930c0924b560cc7b84e5af45ad7962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126857"
---
# <a name="settcpnumconnections-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="6498f-103">SetTcpNumConnections-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="6498f-103">SetTcpNumConnections method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="6498f-104">Die statische Methode **SetTcpNumConnections** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die maximale Anzahl von Verbindungen festzulegen, die TCP möglicherweise gleichzeitig geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="6498f-104">The **SetTcpNumConnections** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum number of connections that TCP may have open simultaneously.</span></span>

<span data-ttu-id="6498f-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6498f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6498f-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6498f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6498f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6498f-107">Syntax</span></span>


```mof
uint32 SetTcpNumConnections(
  [in] uint32 TcpNumConnections
);
```



## <a name="parameters"></a><span data-ttu-id="6498f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6498f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6498f-109">*TcpNumConnections* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6498f-109">*TcpNumConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6498f-110">Maximale Anzahl von Verbindungen, die TCP möglicherweise gleichzeitig geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="6498f-110">Maximum number of connections that TCP may have open simultaneously.</span></span> <span data-ttu-id="6498f-111">Der gültige Wertebereich ist 0-0xfffffe.</span><span class="sxs-lookup"><span data-stu-id="6498f-111">The valid range of values is 0 - 0xFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6498f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6498f-112">Return value</span></span>

<span data-ttu-id="6498f-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="6498f-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="6498f-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6498f-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6498f-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6498f-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6498f-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6498f-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-117">0</span><span class="sxs-lookup"><span data-stu-id="6498f-117">0</span></span>

<span data-ttu-id="6498f-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6498f-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6498f-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-120">1</span><span class="sxs-lookup"><span data-stu-id="6498f-120">1</span></span>

<span data-ttu-id="6498f-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6498f-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="6498f-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-123">64</span><span class="sxs-lookup"><span data-stu-id="6498f-123">64</span></span>

<span data-ttu-id="6498f-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6498f-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="6498f-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-126">65</span><span class="sxs-lookup"><span data-stu-id="6498f-126">65</span></span>

<span data-ttu-id="6498f-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6498f-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="6498f-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-129">66</span><span class="sxs-lookup"><span data-stu-id="6498f-129">66</span></span>

<span data-ttu-id="6498f-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="6498f-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="6498f-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-132">67</span><span class="sxs-lookup"><span data-stu-id="6498f-132">67</span></span>

<span data-ttu-id="6498f-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6498f-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="6498f-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-135">68</span><span class="sxs-lookup"><span data-stu-id="6498f-135">68</span></span>

<span data-ttu-id="6498f-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="6498f-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="6498f-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-138">69</span><span class="sxs-lookup"><span data-stu-id="6498f-138">69</span></span>

<span data-ttu-id="6498f-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="6498f-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="6498f-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-141">70</span><span class="sxs-lookup"><span data-stu-id="6498f-141">70</span></span>

<span data-ttu-id="6498f-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6498f-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="6498f-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-144">71</span><span class="sxs-lookup"><span data-stu-id="6498f-144">71</span></span>

<span data-ttu-id="6498f-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6498f-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="6498f-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-147">72</span><span class="sxs-lookup"><span data-stu-id="6498f-147">72</span></span>

<span data-ttu-id="6498f-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="6498f-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="6498f-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-150">73</span><span class="sxs-lookup"><span data-stu-id="6498f-150">73</span></span>

<span data-ttu-id="6498f-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="6498f-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="6498f-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-153">74</span><span class="sxs-lookup"><span data-stu-id="6498f-153">74</span></span>

<span data-ttu-id="6498f-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="6498f-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="6498f-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-156">75</span><span class="sxs-lookup"><span data-stu-id="6498f-156">75</span></span>

<span data-ttu-id="6498f-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="6498f-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="6498f-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-159">76</span><span class="sxs-lookup"><span data-stu-id="6498f-159">76</span></span>

<span data-ttu-id="6498f-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="6498f-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="6498f-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-162">77</span><span class="sxs-lookup"><span data-stu-id="6498f-162">77</span></span>

<span data-ttu-id="6498f-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="6498f-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="6498f-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-165">78</span><span class="sxs-lookup"><span data-stu-id="6498f-165">78</span></span>

<span data-ttu-id="6498f-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="6498f-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="6498f-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-168">79</span><span class="sxs-lookup"><span data-stu-id="6498f-168">79</span></span>

<span data-ttu-id="6498f-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="6498f-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-171">80</span><span class="sxs-lookup"><span data-stu-id="6498f-171">80</span></span>

<span data-ttu-id="6498f-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="6498f-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-174">81</span><span class="sxs-lookup"><span data-stu-id="6498f-174">81</span></span>

<span data-ttu-id="6498f-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="6498f-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-177">82</span><span class="sxs-lookup"><span data-stu-id="6498f-177">82</span></span>

<span data-ttu-id="6498f-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="6498f-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="6498f-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-180">83</span><span class="sxs-lookup"><span data-stu-id="6498f-180">83</span></span>

<span data-ttu-id="6498f-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6498f-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="6498f-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-183">84</span><span class="sxs-lookup"><span data-stu-id="6498f-183">84</span></span>

<span data-ttu-id="6498f-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6498f-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="6498f-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-186">85</span><span class="sxs-lookup"><span data-stu-id="6498f-186">85</span></span>

<span data-ttu-id="6498f-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6498f-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="6498f-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-189">86</span><span class="sxs-lookup"><span data-stu-id="6498f-189">86</span></span>

<span data-ttu-id="6498f-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="6498f-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="6498f-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-192">87</span><span class="sxs-lookup"><span data-stu-id="6498f-192">87</span></span>

<span data-ttu-id="6498f-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="6498f-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="6498f-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-195">88</span><span class="sxs-lookup"><span data-stu-id="6498f-195">88</span></span>

<span data-ttu-id="6498f-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="6498f-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="6498f-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-198">89</span><span class="sxs-lookup"><span data-stu-id="6498f-198">89</span></span>

<span data-ttu-id="6498f-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="6498f-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="6498f-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-201">90</span><span class="sxs-lookup"><span data-stu-id="6498f-201">90</span></span>

<span data-ttu-id="6498f-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="6498f-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="6498f-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-204">91</span><span class="sxs-lookup"><span data-stu-id="6498f-204">91</span></span>

<span data-ttu-id="6498f-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6498f-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="6498f-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-207">92</span><span class="sxs-lookup"><span data-stu-id="6498f-207">92</span></span>

<span data-ttu-id="6498f-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6498f-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-210">93</span><span class="sxs-lookup"><span data-stu-id="6498f-210">93</span></span>

<span data-ttu-id="6498f-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6498f-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-213">94</span><span class="sxs-lookup"><span data-stu-id="6498f-213">94</span></span>

<span data-ttu-id="6498f-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6498f-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-216">95</span><span class="sxs-lookup"><span data-stu-id="6498f-216">95</span></span>

<span data-ttu-id="6498f-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="6498f-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-219">96</span><span class="sxs-lookup"><span data-stu-id="6498f-219">96</span></span>

<span data-ttu-id="6498f-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="6498f-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="6498f-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-222">97</span><span class="sxs-lookup"><span data-stu-id="6498f-222">97</span></span>

<span data-ttu-id="6498f-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="6498f-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="6498f-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-225">98</span><span class="sxs-lookup"><span data-stu-id="6498f-225">98</span></span>

<span data-ttu-id="6498f-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="6498f-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="6498f-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-228">100</span><span class="sxs-lookup"><span data-stu-id="6498f-228">100</span></span>

<span data-ttu-id="6498f-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6498f-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6498f-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="6498f-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="6498f-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="6498f-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="6498f-232">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6498f-232">Examples</span></span>

<span data-ttu-id="6498f-233">Im Beispiel [Ändern der zulässigen Anzahl von TCP-Verbindungen](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript wird die maximal zulässige Anzahl gleichzeitig geöffneter TCP-Verbindungen auf einem Computer auf 10 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6498f-233">The [Modify the Allowed Number of TCP Connections](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript sample sets the maximum allowed number of simultaneously-opened TCP connections on a computer to 10.</span></span>

## <a name="requirements"></a><span data-ttu-id="6498f-234">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6498f-234">Requirements</span></span>



| <span data-ttu-id="6498f-235">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6498f-235">Requirement</span></span> | <span data-ttu-id="6498f-236">Wert</span><span class="sxs-lookup"><span data-stu-id="6498f-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6498f-237">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6498f-237">Minimum supported client</span></span><br/> | <span data-ttu-id="6498f-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6498f-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6498f-239">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6498f-239">Minimum supported server</span></span><br/> | <span data-ttu-id="6498f-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6498f-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6498f-241">Namespace</span><span class="sxs-lookup"><span data-stu-id="6498f-241">Namespace</span></span><br/>                | <span data-ttu-id="6498f-242">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6498f-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6498f-243">MOF</span><span class="sxs-lookup"><span data-stu-id="6498f-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6498f-244"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6498f-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6498f-245">DLL</span><span class="sxs-lookup"><span data-stu-id="6498f-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6498f-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6498f-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6498f-247">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6498f-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6498f-248">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="6498f-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="6498f-249">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="6498f-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="6498f-250">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="6498f-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="6498f-251">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="6498f-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="6498f-252">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="6498f-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

