---
description: Die statische Methode setkeepaliveinterval WMI-Klasse wird verwendet, um das Intervall für das Trennen von Keep-Alive-reübertragungen festzulegen, bis eine Antwort empfangen wird.
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Setkeepaliveingeterval-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ce6a1491fd9e414f503d0165216794c67db0e97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127060"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f6345-103">Setkeepaliveingeterval-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6345-103">SetKeepAliveInterval method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f6345-104">Die statische Methode **setkeepaliveinterval** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um das Intervall für das Trennen von Keep-Alive-reübertragungen festzulegen, bis eine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f6345-104">The **SetKeepAliveInterval** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the interval separating Keep Alive Retransmissions until a response is received.</span></span>

<span data-ttu-id="f6345-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6345-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f6345-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f6345-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6345-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6345-107">Syntax</span></span>


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a><span data-ttu-id="f6345-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6345-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6345-109">*Keepaliveingeterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6345-109">*KeepAliveInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6345-110">Wert in Millisekunden für das Intervall, bei dem Keep-Alive-Neuübertragungen getrennt werden, bis eine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f6345-110">Value, in milliseconds, for the interval separating Keep Alive Retransmissions until a response is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6345-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6345-111">Return value</span></span>

<span data-ttu-id="f6345-112">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f6345-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f6345-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f6345-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f6345-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f6345-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f6345-115">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f6345-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-116">0</span><span class="sxs-lookup"><span data-stu-id="f6345-116">0</span></span>

<span data-ttu-id="f6345-117">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6345-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-118">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f6345-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-119">1</span><span class="sxs-lookup"><span data-stu-id="f6345-119">1</span></span>

<span data-ttu-id="f6345-120">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6345-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-121">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="f6345-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-122">64</span><span class="sxs-lookup"><span data-stu-id="f6345-122">64</span></span>

<span data-ttu-id="f6345-123">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6345-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-124">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="f6345-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-125">65</span><span class="sxs-lookup"><span data-stu-id="f6345-125">65</span></span>

<span data-ttu-id="f6345-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="f6345-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-127">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="f6345-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-128">66</span><span class="sxs-lookup"><span data-stu-id="f6345-128">66</span></span>

<span data-ttu-id="f6345-129">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="f6345-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="f6345-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-131">67</span><span class="sxs-lookup"><span data-stu-id="f6345-131">67</span></span>

<span data-ttu-id="f6345-132">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f6345-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-133">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="f6345-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-134">68</span><span class="sxs-lookup"><span data-stu-id="f6345-134">68</span></span>

<span data-ttu-id="f6345-135">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="f6345-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-136">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="f6345-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-137">69</span><span class="sxs-lookup"><span data-stu-id="f6345-137">69</span></span>

<span data-ttu-id="f6345-138">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="f6345-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-139">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="f6345-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-140">70</span><span class="sxs-lookup"><span data-stu-id="f6345-140">70</span></span>

<span data-ttu-id="f6345-141">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f6345-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-142">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="f6345-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-143">71</span><span class="sxs-lookup"><span data-stu-id="f6345-143">71</span></span>

<span data-ttu-id="f6345-144">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f6345-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-145">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="f6345-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-146">72</span><span class="sxs-lookup"><span data-stu-id="f6345-146">72</span></span>

<span data-ttu-id="f6345-147">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="f6345-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-148">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="f6345-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-149">73</span><span class="sxs-lookup"><span data-stu-id="f6345-149">73</span></span>

<span data-ttu-id="f6345-150">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="f6345-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-151">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="f6345-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-152">74</span><span class="sxs-lookup"><span data-stu-id="f6345-152">74</span></span>

<span data-ttu-id="f6345-153">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="f6345-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-154">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="f6345-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-155">75</span><span class="sxs-lookup"><span data-stu-id="f6345-155">75</span></span>

<span data-ttu-id="f6345-156">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="f6345-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-157">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="f6345-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-158">76</span><span class="sxs-lookup"><span data-stu-id="f6345-158">76</span></span>

<span data-ttu-id="f6345-159">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="f6345-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-160">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="f6345-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-161">77</span><span class="sxs-lookup"><span data-stu-id="f6345-161">77</span></span>

<span data-ttu-id="f6345-162">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="f6345-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-163">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="f6345-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-164">78</span><span class="sxs-lookup"><span data-stu-id="f6345-164">78</span></span>

<span data-ttu-id="f6345-165">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="f6345-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-166">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="f6345-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-167">79</span><span class="sxs-lookup"><span data-stu-id="f6345-167">79</span></span>

<span data-ttu-id="f6345-168">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="f6345-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-169">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-170">80</span><span class="sxs-lookup"><span data-stu-id="f6345-170">80</span></span>

<span data-ttu-id="f6345-171">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f6345-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-172">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-173">81</span><span class="sxs-lookup"><span data-stu-id="f6345-173">81</span></span>

<span data-ttu-id="f6345-174">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f6345-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-175">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-176">82</span><span class="sxs-lookup"><span data-stu-id="f6345-176">82</span></span>

<span data-ttu-id="f6345-177">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="f6345-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-178">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="f6345-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-179">83</span><span class="sxs-lookup"><span data-stu-id="f6345-179">83</span></span>

<span data-ttu-id="f6345-180">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6345-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-181">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f6345-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-182">84</span><span class="sxs-lookup"><span data-stu-id="f6345-182">84</span></span>

<span data-ttu-id="f6345-183">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6345-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-184">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f6345-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-185">85</span><span class="sxs-lookup"><span data-stu-id="f6345-185">85</span></span>

<span data-ttu-id="f6345-186">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6345-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-187">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="f6345-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-188">86</span><span class="sxs-lookup"><span data-stu-id="f6345-188">86</span></span>

<span data-ttu-id="f6345-189">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="f6345-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-190">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="f6345-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-191">87</span><span class="sxs-lookup"><span data-stu-id="f6345-191">87</span></span>

<span data-ttu-id="f6345-192">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="f6345-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-193">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="f6345-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-194">88</span><span class="sxs-lookup"><span data-stu-id="f6345-194">88</span></span>

<span data-ttu-id="f6345-195">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="f6345-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-196">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="f6345-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-197">89</span><span class="sxs-lookup"><span data-stu-id="f6345-197">89</span></span>

<span data-ttu-id="f6345-198">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="f6345-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-199">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="f6345-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-200">90</span><span class="sxs-lookup"><span data-stu-id="f6345-200">90</span></span>

<span data-ttu-id="f6345-201">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="f6345-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-202">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="f6345-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-203">91</span><span class="sxs-lookup"><span data-stu-id="f6345-203">91</span></span>

<span data-ttu-id="f6345-204">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f6345-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-205">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="f6345-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-206">92</span><span class="sxs-lookup"><span data-stu-id="f6345-206">92</span></span>

<span data-ttu-id="f6345-207">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f6345-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-208">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-209">93</span><span class="sxs-lookup"><span data-stu-id="f6345-209">93</span></span>

<span data-ttu-id="f6345-210">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f6345-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-211">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-212">94</span><span class="sxs-lookup"><span data-stu-id="f6345-212">94</span></span>

<span data-ttu-id="f6345-213">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f6345-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-214">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-215">95</span><span class="sxs-lookup"><span data-stu-id="f6345-215">95</span></span>

<span data-ttu-id="f6345-216">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f6345-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-217">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-218">96</span><span class="sxs-lookup"><span data-stu-id="f6345-218">96</span></span>

<span data-ttu-id="f6345-219">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f6345-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-220">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="f6345-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-221">97</span><span class="sxs-lookup"><span data-stu-id="f6345-221">97</span></span>

<span data-ttu-id="f6345-222">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="f6345-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-223">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6345-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-224">98</span><span class="sxs-lookup"><span data-stu-id="f6345-224">98</span></span>

<span data-ttu-id="f6345-225">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="f6345-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-226">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f6345-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-227">100</span><span class="sxs-lookup"><span data-stu-id="f6345-227">100</span></span>

<span data-ttu-id="f6345-228">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6345-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6345-229">**Andere**</span><span class="sxs-lookup"><span data-stu-id="f6345-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f6345-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f6345-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6345-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6345-231">Remarks</span></span>

<span data-ttu-id="f6345-232">Nachdem eine Antwort empfangen wurde, wird die Verzögerung bis zur nächsten Keep-Alive-Übertragung wieder durch den Wert der [**KeepAliveTime**](win32-networkadapterconfiguration.md) -Eigenschaft gesteuert.</span><span class="sxs-lookup"><span data-stu-id="f6345-232">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of the [**KeepAliveTime**](win32-networkadapterconfiguration.md) property.</span></span> <span data-ttu-id="f6345-233">Die Verbindung wird beendet, nachdem die Anzahl der von der **TcpMaxDataRetransmissions** -Eigenschaft angegebenen erneuten Übertragungen nicht beantwortet wurde.</span><span class="sxs-lookup"><span data-stu-id="f6345-233">The connection is terminated after the number of retransmissions specified by the **TcpMaxDataRetransmissions** property have gone unanswered</span></span>

## <a name="examples"></a><span data-ttu-id="f6345-234">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6345-234">Examples</span></span>

<span data-ttu-id="f6345-235">Im Beispiel [Ändern des Keep-Alive-Intervalls für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) in VBScript wird das Keep-Alive-Intervall für alle Netzwerkadapter auf einem Computer auf 300, 00 Millisekunden (5 Minuten) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f6345-235">The [Modify the Keep Alive Interval for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript sample configures the keep alive interval for all network adapters on a computer to 300,00 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6345-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6345-236">Requirements</span></span>



| <span data-ttu-id="f6345-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6345-237">Requirement</span></span> | <span data-ttu-id="f6345-238">Wert</span><span class="sxs-lookup"><span data-stu-id="f6345-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6345-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6345-239">Minimum supported client</span></span><br/> | <span data-ttu-id="f6345-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6345-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6345-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6345-241">Minimum supported server</span></span><br/> | <span data-ttu-id="f6345-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6345-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6345-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6345-243">Namespace</span></span><br/>                | <span data-ttu-id="f6345-244">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f6345-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6345-245">MOF</span><span class="sxs-lookup"><span data-stu-id="f6345-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6345-246"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6345-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6345-247">DLL</span><span class="sxs-lookup"><span data-stu-id="f6345-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6345-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6345-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6345-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6345-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6345-250">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="f6345-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f6345-251">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="f6345-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f6345-252">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f6345-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f6345-253">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="f6345-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f6345-254">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="f6345-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

