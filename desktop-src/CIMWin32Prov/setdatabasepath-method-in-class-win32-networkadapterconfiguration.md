---
description: Mit der statischen Methode SetDatabasePath WMI-Klasse wird der Pfad zu den standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke und Protokolle) festgelegt.
ms.assetid: 373fef0f-9cdf-4785-8d73-3f00bbd60ae2
ms.tgt_platform: multiple
title: SetDatabasePath-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDatabasePath
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b66a9979ec97d4ceda16acad6488d3b84d5d3a54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524248"
---
# <a name="setdatabasepath-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="dc820-103">SetDatabasePath-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="dc820-103">SetDatabasePath method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="dc820-104">Mit der statischen Methode **SetDatabasePath** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird der Pfad zu den standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke und Protokolle) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc820-104">The **SetDatabasePath** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span>

<span data-ttu-id="dc820-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc820-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dc820-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dc820-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc820-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc820-107">Syntax</span></span>


```mof
uint32 SetDatabasePath(
  [in] string DatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="dc820-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc820-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc820-109">*DatabasePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc820-109">*DatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc820-110">Gültiger Dateipfad zu standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke und Protokolle), die von der Windows Sockets-Schnittstelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-110">Valid file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS) used by the Windows Sockets interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc820-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc820-111">Return value</span></span>

<span data-ttu-id="dc820-112">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="dc820-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, a different number if there is an error.</span></span> <span data-ttu-id="dc820-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dc820-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dc820-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dc820-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="dc820-115">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="dc820-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-116">0</span><span class="sxs-lookup"><span data-stu-id="dc820-116">0</span></span>

<span data-ttu-id="dc820-117">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc820-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-118">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="dc820-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-119">1</span><span class="sxs-lookup"><span data-stu-id="dc820-119">1</span></span>

<span data-ttu-id="dc820-120">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc820-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-121">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="dc820-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-122">64</span><span class="sxs-lookup"><span data-stu-id="dc820-122">64</span></span>

<span data-ttu-id="dc820-123">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc820-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-124">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="dc820-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-125">65</span><span class="sxs-lookup"><span data-stu-id="dc820-125">65</span></span>

<span data-ttu-id="dc820-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="dc820-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-127">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="dc820-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-128">66</span><span class="sxs-lookup"><span data-stu-id="dc820-128">66</span></span>

<span data-ttu-id="dc820-129">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="dc820-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-130">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="dc820-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-131">67</span><span class="sxs-lookup"><span data-stu-id="dc820-131">67</span></span>

<span data-ttu-id="dc820-132">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="dc820-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-133">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="dc820-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-134">68</span><span class="sxs-lookup"><span data-stu-id="dc820-134">68</span></span>

<span data-ttu-id="dc820-135">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="dc820-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-136">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="dc820-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-137">69</span><span class="sxs-lookup"><span data-stu-id="dc820-137">69</span></span>

<span data-ttu-id="dc820-138">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="dc820-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-139">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="dc820-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-140">70</span><span class="sxs-lookup"><span data-stu-id="dc820-140">70</span></span>

<span data-ttu-id="dc820-141">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="dc820-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-142">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="dc820-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-143">71</span><span class="sxs-lookup"><span data-stu-id="dc820-143">71</span></span>

<span data-ttu-id="dc820-144">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="dc820-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-145">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="dc820-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-146">72</span><span class="sxs-lookup"><span data-stu-id="dc820-146">72</span></span>

<span data-ttu-id="dc820-147">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="dc820-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-148">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="dc820-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-149">73</span><span class="sxs-lookup"><span data-stu-id="dc820-149">73</span></span>

<span data-ttu-id="dc820-150">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="dc820-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-151">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="dc820-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-152">74</span><span class="sxs-lookup"><span data-stu-id="dc820-152">74</span></span>

<span data-ttu-id="dc820-153">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="dc820-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-154">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="dc820-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-155">75</span><span class="sxs-lookup"><span data-stu-id="dc820-155">75</span></span>

<span data-ttu-id="dc820-156">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="dc820-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-157">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="dc820-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-158">76</span><span class="sxs-lookup"><span data-stu-id="dc820-158">76</span></span>

<span data-ttu-id="dc820-159">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="dc820-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-160">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="dc820-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-161">77</span><span class="sxs-lookup"><span data-stu-id="dc820-161">77</span></span>

<span data-ttu-id="dc820-162">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="dc820-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-163">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="dc820-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-164">78</span><span class="sxs-lookup"><span data-stu-id="dc820-164">78</span></span>

<span data-ttu-id="dc820-165">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="dc820-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-166">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="dc820-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-167">79</span><span class="sxs-lookup"><span data-stu-id="dc820-167">79</span></span>

<span data-ttu-id="dc820-168">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="dc820-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-169">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-170">80</span><span class="sxs-lookup"><span data-stu-id="dc820-170">80</span></span>

<span data-ttu-id="dc820-171">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-172">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-173">81</span><span class="sxs-lookup"><span data-stu-id="dc820-173">81</span></span>

<span data-ttu-id="dc820-174">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-175">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-176">82</span><span class="sxs-lookup"><span data-stu-id="dc820-176">82</span></span>

<span data-ttu-id="dc820-177">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-178">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="dc820-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-179">83</span><span class="sxs-lookup"><span data-stu-id="dc820-179">83</span></span>

<span data-ttu-id="dc820-180">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-181">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="dc820-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-182">84</span><span class="sxs-lookup"><span data-stu-id="dc820-182">84</span></span>

<span data-ttu-id="dc820-183">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dc820-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-184">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="dc820-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-185">85</span><span class="sxs-lookup"><span data-stu-id="dc820-185">85</span></span>

<span data-ttu-id="dc820-186">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dc820-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-187">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="dc820-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-188">86</span><span class="sxs-lookup"><span data-stu-id="dc820-188">86</span></span>

<span data-ttu-id="dc820-189">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="dc820-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-190">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="dc820-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-191">87</span><span class="sxs-lookup"><span data-stu-id="dc820-191">87</span></span>

<span data-ttu-id="dc820-192">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="dc820-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-193">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="dc820-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-194">88</span><span class="sxs-lookup"><span data-stu-id="dc820-194">88</span></span>

<span data-ttu-id="dc820-195">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="dc820-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-196">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="dc820-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-197">89</span><span class="sxs-lookup"><span data-stu-id="dc820-197">89</span></span>

<span data-ttu-id="dc820-198">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="dc820-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-199">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="dc820-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-200">90</span><span class="sxs-lookup"><span data-stu-id="dc820-200">90</span></span>

<span data-ttu-id="dc820-201">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="dc820-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-202">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="dc820-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-203">91</span><span class="sxs-lookup"><span data-stu-id="dc820-203">91</span></span>

<span data-ttu-id="dc820-204">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="dc820-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-205">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="dc820-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-206">92</span><span class="sxs-lookup"><span data-stu-id="dc820-206">92</span></span>

<span data-ttu-id="dc820-207">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="dc820-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-208">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-209">93</span><span class="sxs-lookup"><span data-stu-id="dc820-209">93</span></span>

<span data-ttu-id="dc820-210">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="dc820-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-211">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-212">94</span><span class="sxs-lookup"><span data-stu-id="dc820-212">94</span></span>

<span data-ttu-id="dc820-213">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="dc820-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-214">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-215">95</span><span class="sxs-lookup"><span data-stu-id="dc820-215">95</span></span>

<span data-ttu-id="dc820-216">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-217">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-218">96</span><span class="sxs-lookup"><span data-stu-id="dc820-218">96</span></span>

<span data-ttu-id="dc820-219">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-220">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="dc820-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-221">97</span><span class="sxs-lookup"><span data-stu-id="dc820-221">97</span></span>

<span data-ttu-id="dc820-222">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="dc820-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-223">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="dc820-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-224">98</span><span class="sxs-lookup"><span data-stu-id="dc820-224">98</span></span>

<span data-ttu-id="dc820-225">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-226">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="dc820-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-227">100</span><span class="sxs-lookup"><span data-stu-id="dc820-227">100</span></span>

<span data-ttu-id="dc820-228">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dc820-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dc820-229">**Andere**</span><span class="sxs-lookup"><span data-stu-id="dc820-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="dc820-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="dc820-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc820-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc820-231">Remarks</span></span>

<span data-ttu-id="dc820-232">Diese Methode wird von der Windows Sockets-Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc820-232">This method is used by the Windows Sockets interface.</span></span> <span data-ttu-id="dc820-233">Der Standardpfad lautet% systemroot% \\ system32 \\ Drivers \\ .</span><span class="sxs-lookup"><span data-stu-id="dc820-233">The default path is %SystemRoot%\\system32\\drivers\\ .</span></span>

## <a name="examples"></a><span data-ttu-id="dc820-234">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc820-234">Examples</span></span>

<span data-ttu-id="dc820-235">Im Beispiel [Ändern des Daten Bank Pfads für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) VBScript in der TechNet Gallery wird **SetDatabasePath** verwendet, um den Pfad zu den standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke, Protokolle) festzulegen, die von der Windows Sockets-Schnittstelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc820-235">The [Modify the Database Path for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) VBScript sample on TechNet Gallery uses **SetDatabasePath** to set the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, PROTOCOLS) used by the Windows Sockets interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc820-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc820-236">Requirements</span></span>



| <span data-ttu-id="dc820-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc820-237">Requirement</span></span> | <span data-ttu-id="dc820-238">Wert</span><span class="sxs-lookup"><span data-stu-id="dc820-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc820-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc820-239">Minimum supported client</span></span><br/> | <span data-ttu-id="dc820-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc820-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc820-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc820-241">Minimum supported server</span></span><br/> | <span data-ttu-id="dc820-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc820-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc820-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc820-243">Namespace</span></span><br/>                | <span data-ttu-id="dc820-244">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dc820-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc820-245">MOF</span><span class="sxs-lookup"><span data-stu-id="dc820-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc820-246"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc820-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc820-247">DLL</span><span class="sxs-lookup"><span data-stu-id="dc820-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc820-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc820-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc820-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc820-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc820-250">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="dc820-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="dc820-251">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="dc820-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="dc820-252">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="dc820-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="dc820-253">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="dc820-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="dc820-254">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="dc820-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

