---
description: Die statische Methode der setmtu-WMI-Klasse wird verwendet, um die Standard-MTU (Maximum Transmission Unit) für eine Netzwerkschnittstelle festzulegen.
ms.assetid: 262c8bd7-1057-4204-80ab-725c60fc9c52
ms.tgt_platform: multiple
title: Die Methode "stmtu" der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetMTU
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 466c344892f2c4bf4a1e979ac9c1f50cd709325a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748569"
---
# <a name="setmtu-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="59cb6-103">Die Methode "nettmtu" der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="59cb6-103">SetMTU method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="59cb6-104">Die statische Methode der **setmtu** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um die Standard-MTU (Maximum Transmission Unit) für eine Netzwerkschnittstelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="59cb6-104">The **SetMTU** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Maximum Transmission Unit (MTU) for a network interface.</span></span>

<span data-ttu-id="59cb6-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="59cb6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="59cb6-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="59cb6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="59cb6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="59cb6-107">Syntax</span></span>


```mof
uint32 SetMTU(
  [in] uint32 MTU
);
```



## <a name="parameters"></a><span data-ttu-id="59cb6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59cb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59cb6-109">*MTU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59cb6-109">*MTU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-110">Standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="59cb6-110">Default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="59cb6-111">Der Bereich dieses Werts umfasst die minimale Paketgröße (68) für die MTU, die vom zugrunde liegenden Netzwerk unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="59cb6-111">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59cb6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59cb6-112">Return value</span></span>

<span data-ttu-id="59cb6-113">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="59cb6-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="59cb6-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="59cb6-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="59cb6-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="59cb6-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="59cb6-116">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="59cb6-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-117">0</span><span class="sxs-lookup"><span data-stu-id="59cb6-117">0</span></span>

<span data-ttu-id="59cb6-118">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="59cb6-118">Successful completion.</span></span> <span data-ttu-id="59cb6-119">Es ist kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="59cb6-119">No reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-120">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="59cb6-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-121">1</span><span class="sxs-lookup"><span data-stu-id="59cb6-121">1</span></span>

<span data-ttu-id="59cb6-122">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="59cb6-122">Successful completion.</span></span> <span data-ttu-id="59cb6-123">Neustart ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="59cb6-123">Reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-124">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-124">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-125">64</span><span class="sxs-lookup"><span data-stu-id="59cb6-125">64</span></span>

<span data-ttu-id="59cb6-126">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59cb6-126">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-127">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-127">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-128">65</span><span class="sxs-lookup"><span data-stu-id="59cb6-128">65</span></span>

<span data-ttu-id="59cb6-129">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="59cb6-129">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-130">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-130">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-131">66</span><span class="sxs-lookup"><span data-stu-id="59cb6-131">66</span></span>

<span data-ttu-id="59cb6-132">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="59cb6-132">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-133">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-133">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-134">67</span><span class="sxs-lookup"><span data-stu-id="59cb6-134">67</span></span>

<span data-ttu-id="59cb6-135">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="59cb6-135">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-136">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="59cb6-136">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-137">68</span><span class="sxs-lookup"><span data-stu-id="59cb6-137">68</span></span>

<span data-ttu-id="59cb6-138">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="59cb6-138">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-139">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-139">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-140">69</span><span class="sxs-lookup"><span data-stu-id="59cb6-140">69</span></span>

<span data-ttu-id="59cb6-141">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="59cb6-141">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-142">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="59cb6-142">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-143">70</span><span class="sxs-lookup"><span data-stu-id="59cb6-143">70</span></span>

<span data-ttu-id="59cb6-144">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="59cb6-144">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-145">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="59cb6-145">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-146">71</span><span class="sxs-lookup"><span data-stu-id="59cb6-146">71</span></span>

<span data-ttu-id="59cb6-147">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="59cb6-147">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-148">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-148">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-149">72</span><span class="sxs-lookup"><span data-stu-id="59cb6-149">72</span></span>

<span data-ttu-id="59cb6-150">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="59cb6-150">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-151">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="59cb6-151">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-152">73</span><span class="sxs-lookup"><span data-stu-id="59cb6-152">73</span></span>

<span data-ttu-id="59cb6-153">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="59cb6-153">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-154">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="59cb6-154">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-155">74</span><span class="sxs-lookup"><span data-stu-id="59cb6-155">74</span></span>

<span data-ttu-id="59cb6-156">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="59cb6-156">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-157">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-157">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-158">75</span><span class="sxs-lookup"><span data-stu-id="59cb6-158">75</span></span>

<span data-ttu-id="59cb6-159">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="59cb6-159">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-160">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="59cb6-160">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-161">76</span><span class="sxs-lookup"><span data-stu-id="59cb6-161">76</span></span>

<span data-ttu-id="59cb6-162">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="59cb6-162">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-163">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-163">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-164">77</span><span class="sxs-lookup"><span data-stu-id="59cb6-164">77</span></span>

<span data-ttu-id="59cb6-165">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="59cb6-165">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-166">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="59cb6-166">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-167">78</span><span class="sxs-lookup"><span data-stu-id="59cb6-167">78</span></span>

<span data-ttu-id="59cb6-168">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="59cb6-168">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-169">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="59cb6-169">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-170">79</span><span class="sxs-lookup"><span data-stu-id="59cb6-170">79</span></span>

<span data-ttu-id="59cb6-171">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="59cb6-171">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-172">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-172">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-173">80</span><span class="sxs-lookup"><span data-stu-id="59cb6-173">80</span></span>

<span data-ttu-id="59cb6-174">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-174">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-175">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-175">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-176">81</span><span class="sxs-lookup"><span data-stu-id="59cb6-176">81</span></span>

<span data-ttu-id="59cb6-177">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-177">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-178">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-178">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-179">82</span><span class="sxs-lookup"><span data-stu-id="59cb6-179">82</span></span>

<span data-ttu-id="59cb6-180">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-180">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-181">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="59cb6-181">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-182">83</span><span class="sxs-lookup"><span data-stu-id="59cb6-182">83</span></span>

<span data-ttu-id="59cb6-183">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-183">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-184">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-184">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-185">84</span><span class="sxs-lookup"><span data-stu-id="59cb6-185">84</span></span>

<span data-ttu-id="59cb6-186">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="59cb6-186">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-187">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-187">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-188">85</span><span class="sxs-lookup"><span data-stu-id="59cb6-188">85</span></span>

<span data-ttu-id="59cb6-189">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="59cb6-189">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-190">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-190">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-191">86</span><span class="sxs-lookup"><span data-stu-id="59cb6-191">86</span></span>

<span data-ttu-id="59cb6-192">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="59cb6-192">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-193">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="59cb6-193">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-194">87</span><span class="sxs-lookup"><span data-stu-id="59cb6-194">87</span></span>

<span data-ttu-id="59cb6-195">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="59cb6-195">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-196">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="59cb6-196">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-197">88</span><span class="sxs-lookup"><span data-stu-id="59cb6-197">88</span></span>

<span data-ttu-id="59cb6-198">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="59cb6-198">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-199">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="59cb6-199">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-200">89</span><span class="sxs-lookup"><span data-stu-id="59cb6-200">89</span></span>

<span data-ttu-id="59cb6-201">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="59cb6-201">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-202">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="59cb6-202">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-203">90</span><span class="sxs-lookup"><span data-stu-id="59cb6-203">90</span></span>

<span data-ttu-id="59cb6-204">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="59cb6-204">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-205">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="59cb6-205">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-206">91</span><span class="sxs-lookup"><span data-stu-id="59cb6-206">91</span></span>

<span data-ttu-id="59cb6-207">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="59cb6-207">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-208">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="59cb6-208">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-209">92</span><span class="sxs-lookup"><span data-stu-id="59cb6-209">92</span></span>

<span data-ttu-id="59cb6-210">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="59cb6-210">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-211">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-211">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-212">93</span><span class="sxs-lookup"><span data-stu-id="59cb6-212">93</span></span>

<span data-ttu-id="59cb6-213">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-213">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-214">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-214">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-215">94</span><span class="sxs-lookup"><span data-stu-id="59cb6-215">94</span></span>

<span data-ttu-id="59cb6-216">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-216">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-217">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-217">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-218">95</span><span class="sxs-lookup"><span data-stu-id="59cb6-218">95</span></span>

<span data-ttu-id="59cb6-219">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-219">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-220">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-220">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-221">96</span><span class="sxs-lookup"><span data-stu-id="59cb6-221">96</span></span>

<span data-ttu-id="59cb6-222">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-222">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-223">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="59cb6-223">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-224">97</span><span class="sxs-lookup"><span data-stu-id="59cb6-224">97</span></span>

<span data-ttu-id="59cb6-225">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="59cb6-225">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-226">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-226">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-227">98</span><span class="sxs-lookup"><span data-stu-id="59cb6-227">98</span></span>

<span data-ttu-id="59cb6-228">Nicht alle DHCP-Leases können freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="59cb6-228">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-229">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="59cb6-229">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-230">100</span><span class="sxs-lookup"><span data-stu-id="59cb6-230">100</span></span>

<span data-ttu-id="59cb6-231">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="59cb6-231">DHCP is not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="59cb6-232">**Andere**</span><span class="sxs-lookup"><span data-stu-id="59cb6-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="59cb6-233">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="59cb6-233">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59cb6-234">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59cb6-234">Remarks</span></span>

<span data-ttu-id="59cb6-235">Die MTU ist die maximale Paketgröße (in Bytes), die ein Transport über das zugrunde liegende Netzwerk überträgt.</span><span class="sxs-lookup"><span data-stu-id="59cb6-235">The MTU is the maximum packet size (in bytes) that a transport will transmit over the underlying network.</span></span> <span data-ttu-id="59cb6-236">Die Größe schließt den Transport Header ein.</span><span class="sxs-lookup"><span data-stu-id="59cb6-236">The size includes the transport header.</span></span>

<span data-ttu-id="59cb6-237">Beachten Sie, dass ein IP-Datagramm mehrere Pakete umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="59cb6-237">Note that an IP datagram can span multiple packets.</span></span> <span data-ttu-id="59cb6-238">Werte, die größer als der Standardwert für das zugrunde liegende Netzwerk sind, führen zum Transport mit der Standard-MTU des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="59cb6-238">Values larger than the default for the underlying network result in the transport using the network default MTU.</span></span> <span data-ttu-id="59cb6-239">Werte, die kleiner als 68 sind, führen zum Transport mit einer MTU von 68.</span><span class="sxs-lookup"><span data-stu-id="59cb6-239">Values smaller than 68 result in the transport using an MTU of 68.</span></span>

## <a name="examples"></a><span data-ttu-id="59cb6-240">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59cb6-240">Examples</span></span>

<span data-ttu-id="59cb6-241">Im Beispiel [Ändern der MTU für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript wird die maximale Übertragungseinheit für alle in einem Computer installierten Netzwerkadapter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="59cb6-241">The [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript sample configures the maximum transmission unit for all network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="59cb6-242">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59cb6-242">Requirements</span></span>



| <span data-ttu-id="59cb6-243">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59cb6-243">Requirement</span></span> | <span data-ttu-id="59cb6-244">Wert</span><span class="sxs-lookup"><span data-stu-id="59cb6-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59cb6-245">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59cb6-245">Minimum supported client</span></span><br/> | <span data-ttu-id="59cb6-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59cb6-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59cb6-247">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59cb6-247">Minimum supported server</span></span><br/> | <span data-ttu-id="59cb6-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59cb6-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59cb6-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="59cb6-249">Namespace</span></span><br/>                | <span data-ttu-id="59cb6-250">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="59cb6-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59cb6-251">MOF</span><span class="sxs-lookup"><span data-stu-id="59cb6-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59cb6-252"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="59cb6-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59cb6-253">DLL</span><span class="sxs-lookup"><span data-stu-id="59cb6-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59cb6-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59cb6-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59cb6-255">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59cb6-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59cb6-256">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="59cb6-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="59cb6-257">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="59cb6-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="59cb6-258">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="59cb6-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="59cb6-259">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="59cb6-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="59cb6-260">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="59cb6-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

