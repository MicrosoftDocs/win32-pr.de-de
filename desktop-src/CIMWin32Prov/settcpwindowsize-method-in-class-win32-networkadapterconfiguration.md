---
description: Die statische Methode settcpwindowsize WMI-Klasse wird verwendet, um die maximale Größe des TCP-Empfangs Fensters festzulegen, die vom System bereitgestellt wird.
ms.assetid: c108fd9c-6de4-4f3e-9691-b0b5c1a3dc5f
ms.tgt_platform: multiple
title: Settcpwindowsize-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpWindowSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4a77acdc81c06d1f78da8bbc0160bd0d21bcfd8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126853"
---
# <a name="settcpwindowsize-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="58003-103">Settcpwindowsize-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="58003-103">SetTcpWindowSize method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="58003-104">Die statische Methode **settcpwindowsize** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die maximale Größe des TCP-Empfangs Fensters festzulegen, die vom System bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="58003-104">The **SetTcpWindowSize** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum TCP Receive Window size offered by the system.</span></span>

<span data-ttu-id="58003-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="58003-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="58003-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="58003-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="58003-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="58003-107">Syntax</span></span>


```mof
uint32 SetTcpWindowSize(
  [in] uint16 TcpWindowSize
);
```



## <a name="parameters"></a><span data-ttu-id="58003-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="58003-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58003-109">*TcpWindowSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58003-109">*TcpWindowSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58003-110">Maximale TCP-Empfangs Fenstergröße, die vom System bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="58003-110">Maximum TCP receive window size offered by the system.</span></span> <span data-ttu-id="58003-111">Der gültige Wertebereich in Bytes ist 0-65535.</span><span class="sxs-lookup"><span data-stu-id="58003-111">The valid range of values in bytes is 0 - 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58003-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58003-112">Return value</span></span>

<span data-ttu-id="58003-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="58003-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="58003-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="58003-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="58003-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="58003-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="58003-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="58003-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="58003-117">0</span><span class="sxs-lookup"><span data-stu-id="58003-117">0</span></span>

<span data-ttu-id="58003-118">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58003-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="58003-119">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="58003-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="58003-120">1</span><span class="sxs-lookup"><span data-stu-id="58003-120">1</span></span>

<span data-ttu-id="58003-121">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58003-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="58003-122">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="58003-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="58003-123">64</span><span class="sxs-lookup"><span data-stu-id="58003-123">64</span></span>

<span data-ttu-id="58003-124">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58003-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="58003-125">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="58003-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="58003-126">65</span><span class="sxs-lookup"><span data-stu-id="58003-126">65</span></span>

<span data-ttu-id="58003-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="58003-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="58003-128">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="58003-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="58003-129">66</span><span class="sxs-lookup"><span data-stu-id="58003-129">66</span></span>

<span data-ttu-id="58003-130">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="58003-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="58003-131">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="58003-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="58003-132">67</span><span class="sxs-lookup"><span data-stu-id="58003-132">67</span></span>

<span data-ttu-id="58003-133">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="58003-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="58003-134">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="58003-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="58003-135">68</span><span class="sxs-lookup"><span data-stu-id="58003-135">68</span></span>

<span data-ttu-id="58003-136">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="58003-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="58003-137">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="58003-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="58003-138">69</span><span class="sxs-lookup"><span data-stu-id="58003-138">69</span></span>

<span data-ttu-id="58003-139">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="58003-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="58003-140">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="58003-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="58003-141">70</span><span class="sxs-lookup"><span data-stu-id="58003-141">70</span></span>

<span data-ttu-id="58003-142">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="58003-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="58003-143">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="58003-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="58003-144">71</span><span class="sxs-lookup"><span data-stu-id="58003-144">71</span></span>

<span data-ttu-id="58003-145">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="58003-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="58003-146">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="58003-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="58003-147">72</span><span class="sxs-lookup"><span data-stu-id="58003-147">72</span></span>

<span data-ttu-id="58003-148">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="58003-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="58003-149">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="58003-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="58003-150">73</span><span class="sxs-lookup"><span data-stu-id="58003-150">73</span></span>

<span data-ttu-id="58003-151">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="58003-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="58003-152">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="58003-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="58003-153">74</span><span class="sxs-lookup"><span data-stu-id="58003-153">74</span></span>

<span data-ttu-id="58003-154">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="58003-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="58003-155">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="58003-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="58003-156">75</span><span class="sxs-lookup"><span data-stu-id="58003-156">75</span></span>

<span data-ttu-id="58003-157">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="58003-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="58003-158">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="58003-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="58003-159">76</span><span class="sxs-lookup"><span data-stu-id="58003-159">76</span></span>

<span data-ttu-id="58003-160">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="58003-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="58003-161">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="58003-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="58003-162">77</span><span class="sxs-lookup"><span data-stu-id="58003-162">77</span></span>

<span data-ttu-id="58003-163">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="58003-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="58003-164">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="58003-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="58003-165">78</span><span class="sxs-lookup"><span data-stu-id="58003-165">78</span></span>

<span data-ttu-id="58003-166">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="58003-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="58003-167">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="58003-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="58003-168">79</span><span class="sxs-lookup"><span data-stu-id="58003-168">79</span></span>

<span data-ttu-id="58003-169">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="58003-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="58003-170">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="58003-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="58003-171">80</span><span class="sxs-lookup"><span data-stu-id="58003-171">80</span></span>

<span data-ttu-id="58003-172">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="58003-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="58003-173">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="58003-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="58003-174">81</span><span class="sxs-lookup"><span data-stu-id="58003-174">81</span></span>

<span data-ttu-id="58003-175">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="58003-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="58003-176">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="58003-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="58003-177">82</span><span class="sxs-lookup"><span data-stu-id="58003-177">82</span></span>

<span data-ttu-id="58003-178">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="58003-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="58003-179">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="58003-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="58003-180">83</span><span class="sxs-lookup"><span data-stu-id="58003-180">83</span></span>

<span data-ttu-id="58003-181">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="58003-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="58003-182">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="58003-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="58003-183">84</span><span class="sxs-lookup"><span data-stu-id="58003-183">84</span></span>

<span data-ttu-id="58003-184">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58003-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="58003-185">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="58003-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="58003-186">85</span><span class="sxs-lookup"><span data-stu-id="58003-186">85</span></span>

<span data-ttu-id="58003-187">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58003-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="58003-188">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="58003-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="58003-189">86</span><span class="sxs-lookup"><span data-stu-id="58003-189">86</span></span>

<span data-ttu-id="58003-190">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="58003-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="58003-191">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="58003-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="58003-192">87</span><span class="sxs-lookup"><span data-stu-id="58003-192">87</span></span>

<span data-ttu-id="58003-193">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="58003-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="58003-194">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="58003-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="58003-195">88</span><span class="sxs-lookup"><span data-stu-id="58003-195">88</span></span>

<span data-ttu-id="58003-196">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="58003-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="58003-197">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="58003-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="58003-198">89</span><span class="sxs-lookup"><span data-stu-id="58003-198">89</span></span>

<span data-ttu-id="58003-199">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="58003-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="58003-200">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="58003-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="58003-201">90</span><span class="sxs-lookup"><span data-stu-id="58003-201">90</span></span>

<span data-ttu-id="58003-202">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="58003-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="58003-203">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="58003-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="58003-204">91</span><span class="sxs-lookup"><span data-stu-id="58003-204">91</span></span>

<span data-ttu-id="58003-205">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="58003-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="58003-206">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="58003-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="58003-207">92</span><span class="sxs-lookup"><span data-stu-id="58003-207">92</span></span>

<span data-ttu-id="58003-208">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="58003-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="58003-209">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="58003-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="58003-210">93</span><span class="sxs-lookup"><span data-stu-id="58003-210">93</span></span>

<span data-ttu-id="58003-211">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="58003-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="58003-212">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="58003-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="58003-213">94</span><span class="sxs-lookup"><span data-stu-id="58003-213">94</span></span>

<span data-ttu-id="58003-214">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="58003-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="58003-215">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="58003-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="58003-216">95</span><span class="sxs-lookup"><span data-stu-id="58003-216">95</span></span>

<span data-ttu-id="58003-217">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="58003-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="58003-218">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="58003-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="58003-219">96</span><span class="sxs-lookup"><span data-stu-id="58003-219">96</span></span>

<span data-ttu-id="58003-220">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="58003-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="58003-221">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="58003-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="58003-222">97</span><span class="sxs-lookup"><span data-stu-id="58003-222">97</span></span>

<span data-ttu-id="58003-223">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="58003-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="58003-224">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="58003-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="58003-225">98</span><span class="sxs-lookup"><span data-stu-id="58003-225">98</span></span>

<span data-ttu-id="58003-226">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="58003-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="58003-227">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="58003-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="58003-228">100</span><span class="sxs-lookup"><span data-stu-id="58003-228">100</span></span>

<span data-ttu-id="58003-229">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58003-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="58003-230">**Andere**</span><span class="sxs-lookup"><span data-stu-id="58003-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="58003-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="58003-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58003-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58003-232">Remarks</span></span>

<span data-ttu-id="58003-233">Das Empfangsfenster gibt die Anzahl der Bytes an, die von einem Absender übertragen werden können, ohne eine Bestätigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="58003-233">The receive window specifies the number of bytes a sender can transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="58003-234">Im allgemeinen verbessern größere Empfangs Fenster die Leistung bei Netzwerken mit hoher Verzögerung und hoher Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="58003-234">In general, larger receive windows improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="58003-235">Aus Effizienzgründen sollte das Empfangs Fenster ein gleich Vielfaches der maximalen TCP-Segment Größe (MSS) sein.</span><span class="sxs-lookup"><span data-stu-id="58003-235">For efficiency, the receive window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span>

> [!Note]  
> <span data-ttu-id="58003-236">Windows Vista: Diese Methode greift `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` auf den Registrierungs Eintrag zu, der nicht in der aktuellen Implementierung des Betriebssystems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58003-236">Windows Vista: This method accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

## <a name="examples"></a><span data-ttu-id="58003-237">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58003-237">Examples</span></span>

<span data-ttu-id="58003-238">Im Beispiel [Ändern der TCP-Fenstergröße für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript wird die TCP-Fenstergröße für alle Netzwerkadapter auf einem Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="58003-238">The [Modify the TCP Window Size for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript sample sets the TCP window size for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="58003-239">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58003-239">Requirements</span></span>



| <span data-ttu-id="58003-240">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58003-240">Requirement</span></span> | <span data-ttu-id="58003-241">Wert</span><span class="sxs-lookup"><span data-stu-id="58003-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58003-242">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58003-242">Minimum supported client</span></span><br/> | <span data-ttu-id="58003-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58003-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58003-244">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58003-244">Minimum supported server</span></span><br/> | <span data-ttu-id="58003-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58003-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58003-246">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="58003-246">End of client support</span></span><br/>    | <span data-ttu-id="58003-247">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58003-247">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="58003-248">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="58003-248">End of server support</span></span><br/>    | <span data-ttu-id="58003-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58003-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58003-250">Namespace</span><span class="sxs-lookup"><span data-stu-id="58003-250">Namespace</span></span><br/>                | <span data-ttu-id="58003-251">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58003-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58003-252">MOF</span><span class="sxs-lookup"><span data-stu-id="58003-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58003-253"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58003-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58003-254">DLL</span><span class="sxs-lookup"><span data-stu-id="58003-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58003-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58003-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58003-256">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58003-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58003-257">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="58003-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="58003-258">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="58003-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="58003-259">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="58003-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="58003-260">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="58003-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="58003-261">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="58003-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

