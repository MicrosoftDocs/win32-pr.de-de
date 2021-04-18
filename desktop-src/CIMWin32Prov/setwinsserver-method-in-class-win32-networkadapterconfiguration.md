---
description: Mithilfe der WMI-Klassenmethode SetWINSServer werden die primären und sekundären Windows Internet Naming Service (WINS)-Server auf diesem TCP/IP-gebundenen Netzwerkadapter festgelegt. Diese Methode wird unabhängig vom Netzwerkadapter angewendet.
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: SetWINSServer-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344940"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3cefd-104">SetWINSServer-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="3cefd-104">SetWINSServer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3cefd-105">Mithilfe der [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetWINSServer** werden die primären und sekundären Windows Internet Naming Service (WINS)-Server auf diesem TCP/IP-gebundenen Netzwerkadapter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3cefd-105">The **SetWINSServer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span> <span data-ttu-id="3cefd-106">Diese Methode wird unabhängig vom Netzwerkadapter angewendet.</span><span class="sxs-lookup"><span data-stu-id="3cefd-106">This method is applied independently of the network adapter.</span></span>

<span data-ttu-id="3cefd-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cefd-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3cefd-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3cefd-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3cefd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cefd-109">Syntax</span></span>


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a><span data-ttu-id="3cefd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cefd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cefd-111">*WINSPrimaryServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cefd-111">*WINSPrimaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-112">Die IP-Adresse des primären WINS-Servers.</span><span class="sxs-lookup"><span data-stu-id="3cefd-112">IP address of the primary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="3cefd-113">Überprüfen Sie immer die Gültigkeit dieser IP-Adresse, wenn Sie von einer unbekannten Quelle oder von einer nicht vertrauenswürdigen Quelle ist.</span><span class="sxs-lookup"><span data-stu-id="3cefd-113">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> <dt>

<span data-ttu-id="3cefd-114">*WINSSecondaryServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cefd-114">*WINSSecondaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-115">IP-Adresse des sekundären WINS-Servers.</span><span class="sxs-lookup"><span data-stu-id="3cefd-115">IP address of the secondary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="3cefd-116">Überprüfen Sie immer die Gültigkeit dieser IP-Adresse, wenn Sie von einer unbekannten Quelle oder von einer nicht vertrauenswürdigen Quelle ist.</span><span class="sxs-lookup"><span data-stu-id="3cefd-116">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cefd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cefd-117">Return value</span></span>

<span data-ttu-id="3cefd-118">Gibt bei erfolgreichem Abschluss einen ganzzahligen Wert von 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="3cefd-118">Returns an integer value of 0 (zero) on successful completion, and any other number to indicate an error.</span></span> <span data-ttu-id="3cefd-119">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3cefd-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3cefd-120">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3cefd-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3cefd-121">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3cefd-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-122">0</span><span class="sxs-lookup"><span data-stu-id="3cefd-122">0</span></span>

<span data-ttu-id="3cefd-123">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cefd-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-124">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3cefd-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-125">1</span><span class="sxs-lookup"><span data-stu-id="3cefd-125">1</span></span>

<span data-ttu-id="3cefd-126">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cefd-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-127">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-128">64</span><span class="sxs-lookup"><span data-stu-id="3cefd-128">64</span></span>

<span data-ttu-id="3cefd-129">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3cefd-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-130">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-131">65</span><span class="sxs-lookup"><span data-stu-id="3cefd-131">65</span></span>

<span data-ttu-id="3cefd-132">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3cefd-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-133">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-134">66</span><span class="sxs-lookup"><span data-stu-id="3cefd-134">66</span></span>

<span data-ttu-id="3cefd-135">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="3cefd-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-136">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-137">67</span><span class="sxs-lookup"><span data-stu-id="3cefd-137">67</span></span>

<span data-ttu-id="3cefd-138">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3cefd-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-139">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="3cefd-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-140">68</span><span class="sxs-lookup"><span data-stu-id="3cefd-140">68</span></span>

<span data-ttu-id="3cefd-141">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="3cefd-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-142">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-143">69</span><span class="sxs-lookup"><span data-stu-id="3cefd-143">69</span></span>

<span data-ttu-id="3cefd-144">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="3cefd-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-145">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="3cefd-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-146">70</span><span class="sxs-lookup"><span data-stu-id="3cefd-146">70</span></span>

<span data-ttu-id="3cefd-147">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3cefd-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-148">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="3cefd-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-149">71</span><span class="sxs-lookup"><span data-stu-id="3cefd-149">71</span></span>

<span data-ttu-id="3cefd-150">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3cefd-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-151">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-152">72</span><span class="sxs-lookup"><span data-stu-id="3cefd-152">72</span></span>

<span data-ttu-id="3cefd-153">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="3cefd-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-154">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="3cefd-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-155">73</span><span class="sxs-lookup"><span data-stu-id="3cefd-155">73</span></span>

<span data-ttu-id="3cefd-156">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="3cefd-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-157">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="3cefd-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-158">74</span><span class="sxs-lookup"><span data-stu-id="3cefd-158">74</span></span>

<span data-ttu-id="3cefd-159">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="3cefd-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-160">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-161">75</span><span class="sxs-lookup"><span data-stu-id="3cefd-161">75</span></span>

<span data-ttu-id="3cefd-162">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="3cefd-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-163">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="3cefd-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-164">76</span><span class="sxs-lookup"><span data-stu-id="3cefd-164">76</span></span>

<span data-ttu-id="3cefd-165">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="3cefd-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-166">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-167">77</span><span class="sxs-lookup"><span data-stu-id="3cefd-167">77</span></span>

<span data-ttu-id="3cefd-168">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="3cefd-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-169">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="3cefd-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-170">78</span><span class="sxs-lookup"><span data-stu-id="3cefd-170">78</span></span>

<span data-ttu-id="3cefd-171">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="3cefd-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-172">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="3cefd-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-173">79</span><span class="sxs-lookup"><span data-stu-id="3cefd-173">79</span></span>

<span data-ttu-id="3cefd-174">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="3cefd-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-175">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-176">80</span><span class="sxs-lookup"><span data-stu-id="3cefd-176">80</span></span>

<span data-ttu-id="3cefd-177">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-178">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-179">81</span><span class="sxs-lookup"><span data-stu-id="3cefd-179">81</span></span>

<span data-ttu-id="3cefd-180">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-180">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-181">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-181">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-182">82</span><span class="sxs-lookup"><span data-stu-id="3cefd-182">82</span></span>

<span data-ttu-id="3cefd-183">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-183">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-184">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="3cefd-184">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-185">83</span><span class="sxs-lookup"><span data-stu-id="3cefd-185">83</span></span>

<span data-ttu-id="3cefd-186">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-186">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-187">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-187">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-188">84</span><span class="sxs-lookup"><span data-stu-id="3cefd-188">84</span></span>

<span data-ttu-id="3cefd-189">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3cefd-189">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-190">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-190">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-191">85</span><span class="sxs-lookup"><span data-stu-id="3cefd-191">85</span></span>

<span data-ttu-id="3cefd-192">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3cefd-192">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-193">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-193">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-194">86</span><span class="sxs-lookup"><span data-stu-id="3cefd-194">86</span></span>

<span data-ttu-id="3cefd-195">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="3cefd-195">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-196">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="3cefd-196">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-197">87</span><span class="sxs-lookup"><span data-stu-id="3cefd-197">87</span></span>

<span data-ttu-id="3cefd-198">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="3cefd-198">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-199">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="3cefd-199">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-200">88</span><span class="sxs-lookup"><span data-stu-id="3cefd-200">88</span></span>

<span data-ttu-id="3cefd-201">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="3cefd-201">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-202">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="3cefd-202">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-203">89</span><span class="sxs-lookup"><span data-stu-id="3cefd-203">89</span></span>

<span data-ttu-id="3cefd-204">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="3cefd-204">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-205">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="3cefd-205">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-206">90</span><span class="sxs-lookup"><span data-stu-id="3cefd-206">90</span></span>

<span data-ttu-id="3cefd-207">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="3cefd-207">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-208">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="3cefd-208">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-209">91</span><span class="sxs-lookup"><span data-stu-id="3cefd-209">91</span></span>

<span data-ttu-id="3cefd-210">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="3cefd-210">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-211">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="3cefd-211">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-212">92</span><span class="sxs-lookup"><span data-stu-id="3cefd-212">92</span></span>

<span data-ttu-id="3cefd-213">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3cefd-213">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-214">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-214">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-215">93</span><span class="sxs-lookup"><span data-stu-id="3cefd-215">93</span></span>

<span data-ttu-id="3cefd-216">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-216">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-217">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-217">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-218">94</span><span class="sxs-lookup"><span data-stu-id="3cefd-218">94</span></span>

<span data-ttu-id="3cefd-219">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-219">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-220">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-220">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-221">95</span><span class="sxs-lookup"><span data-stu-id="3cefd-221">95</span></span>

<span data-ttu-id="3cefd-222">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-222">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-223">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-223">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-224">96</span><span class="sxs-lookup"><span data-stu-id="3cefd-224">96</span></span>

<span data-ttu-id="3cefd-225">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-225">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-226">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="3cefd-226">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-227">97</span><span class="sxs-lookup"><span data-stu-id="3cefd-227">97</span></span>

<span data-ttu-id="3cefd-228">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="3cefd-228">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-229">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-229">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-230">98</span><span class="sxs-lookup"><span data-stu-id="3cefd-230">98</span></span>

<span data-ttu-id="3cefd-231">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="3cefd-231">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-232">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="3cefd-232">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-233">100</span><span class="sxs-lookup"><span data-stu-id="3cefd-233">100</span></span>

<span data-ttu-id="3cefd-234">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3cefd-234">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3cefd-235">**Andere**</span><span class="sxs-lookup"><span data-stu-id="3cefd-235">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3cefd-236">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="3cefd-236">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cefd-237">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cefd-237">Remarks</span></span>

<span data-ttu-id="3cefd-238">Wenn *WINSPrimaryServer* und *WINSSecondaryServer* auf "" festgelegt sind (eine leere Zeichenfolge), werden explizite WINS-Server auf DHCP zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3cefd-238">If both *WINSPrimaryServer* and *WINSSecondaryServer* are set to "" (an empty string), then explicit WINS servers revert back to DHCP.</span></span>

## <a name="examples"></a><span data-ttu-id="3cefd-239">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cefd-239">Examples</span></span>

<span data-ttu-id="3cefd-240">[Zuweisen einer aus einer Datenbank abgerufenen IP-Adresse](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript-Codebeispiel sucht einen Computer in einer-Datenbank und weist diesem Computer die angegebene IP-Adresse zu.</span><span class="sxs-lookup"><span data-stu-id="3cefd-240">[The Assign an IP Address Retrieved from a Database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript code sample looks up a computer in a database and assigns that computer the specified IP address.</span></span>

<span data-ttu-id="3cefd-241">Im folgenden VBScript-Codebeispiel wird der primäre und der sekundäre WINS-Server für einen TCP/IP-gebundenen Netzwerkadapter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3cefd-241">The following VBScript code sample sets the primary and secondary WINS server for a TCP/IP-bound network adapter.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
```



## <a name="requirements"></a><span data-ttu-id="3cefd-242">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cefd-242">Requirements</span></span>



| <span data-ttu-id="3cefd-243">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cefd-243">Requirement</span></span> | <span data-ttu-id="3cefd-244">Wert</span><span class="sxs-lookup"><span data-stu-id="3cefd-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cefd-245">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cefd-245">Minimum supported client</span></span><br/> | <span data-ttu-id="3cefd-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cefd-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cefd-247">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cefd-247">Minimum supported server</span></span><br/> | <span data-ttu-id="3cefd-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cefd-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cefd-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cefd-249">Namespace</span></span><br/>                | <span data-ttu-id="3cefd-250">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3cefd-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3cefd-251">MOF</span><span class="sxs-lookup"><span data-stu-id="3cefd-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cefd-252"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3cefd-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cefd-253">DLL</span><span class="sxs-lookup"><span data-stu-id="3cefd-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cefd-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cefd-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cefd-255">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cefd-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cefd-256">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="3cefd-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3cefd-257">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="3cefd-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3cefd-258">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3cefd-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3cefd-259">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="3cefd-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="3cefd-260">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="3cefd-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

