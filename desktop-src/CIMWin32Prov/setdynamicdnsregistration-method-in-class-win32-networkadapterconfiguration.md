---
description: Die SetDynamicDNSRegistration-Methode gibt die dynamische DNS-Registrierung von IP-Adressen für diesen IP-gebundenen Adapter an.
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: SetDynamicDNSRegistration-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861380"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f1768-103">SetDynamicDNSRegistration-Methode der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="f1768-103">SetDynamicDNSRegistration method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f1768-104">Die **SetDynamicDNSRegistration** -Methode gibt die dynamische DNS-Registrierung von IP-Adressen für diesen IP-gebundenen Adapter an.</span><span class="sxs-lookup"><span data-stu-id="f1768-104">The **SetDynamicDNSRegistration** method indicates the dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span>

<span data-ttu-id="f1768-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1768-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f1768-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f1768-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1768-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1768-107">Syntax</span></span>


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f1768-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1768-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1768-109">*Fulldnsregistrationaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1768-109">*FullDNSRegistrationEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1768-110">**True** gibt an, dass die IP-Adressen für diese Verbindung in DNS unter dem vollständigen DNS-Namen des Computers registriert sind.</span><span class="sxs-lookup"><span data-stu-id="f1768-110">If **true**, the IP addresses for this connection is registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="f1768-111">Der vollständige DNS-Name des Computers wird in der Systemsteuerung auf der Registerkarte **Netzwerk Identifizierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1768-111">The full DNS name of the computer is displayed on the **Network Identification** tab of the system Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-112">*Domaindnsregistrationaktiviert* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f1768-112">*DomainDNSRegistrationEnabled* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1768-113">Wenn der Wert **true** ist, werden die IP-Adressen für diese Verbindung unter dem Domänen Namen dieser Verbindung registriert, zusätzlich zur Registrierung unter dem vollständigen DNS-Namen des Computers.</span><span class="sxs-lookup"><span data-stu-id="f1768-113">If **true**, the IP addresses for this connection are registered under the domain name of this connection, in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="f1768-114">Der Domänen Name dieser Verbindung wird entweder mithilfe der [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) -Methode festgelegt oder von DHCP zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f1768-114">The domain name of this connection is either set using the method [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) or assigned by DHCP.</span></span> <span data-ttu-id="f1768-115">Der registrierte Name ist der Hostname des Computers, dem der Domänen Name angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f1768-115">The registered name is the host name of the computer with the domain name appended.</span></span> <span data-ttu-id="f1768-116">Dieser Parameter ist nur von Bedeutung, wenn *fulldnsregistrationaktivierte* aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f1768-116">This parameter has meaning only when *FullDNSRegistrationEnabled* is enabled.</span></span> <span data-ttu-id="f1768-117">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="f1768-117">The default value is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1768-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1768-118">Return value</span></span>

<span data-ttu-id="f1768-119">Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f1768-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f1768-120">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f1768-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f1768-121">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f1768-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f1768-122">**Erfolgreicher Abschluss, kein Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f1768-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-123">0</span><span class="sxs-lookup"><span data-stu-id="f1768-123">0</span></span>

<span data-ttu-id="f1768-124">Erfolgreicher Abschluss, kein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f1768-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-125">**Erfolgreicher Abschluss, Neustart erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f1768-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-126">1</span><span class="sxs-lookup"><span data-stu-id="f1768-126">1</span></span>

<span data-ttu-id="f1768-127">Erfolgreicher Abschluss, Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f1768-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-128">**Methode wird auf dieser Plattform nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="f1768-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-129">64</span><span class="sxs-lookup"><span data-stu-id="f1768-129">64</span></span>

<span data-ttu-id="f1768-130">Die Methode wird auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1768-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-131">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="f1768-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-132">65</span><span class="sxs-lookup"><span data-stu-id="f1768-132">65</span></span>

<span data-ttu-id="f1768-133">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="f1768-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-134">**Ungültige Subnetzmaske.**</span><span class="sxs-lookup"><span data-stu-id="f1768-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-135">66</span><span class="sxs-lookup"><span data-stu-id="f1768-135">66</span></span>

<span data-ttu-id="f1768-136">Ungültige Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="f1768-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-137">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**</span><span class="sxs-lookup"><span data-stu-id="f1768-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-138">67</span><span class="sxs-lookup"><span data-stu-id="f1768-138">67</span></span>

<span data-ttu-id="f1768-139">Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f1768-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-140">**Ungültiger Eingabeparameter**</span><span class="sxs-lookup"><span data-stu-id="f1768-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-141">68</span><span class="sxs-lookup"><span data-stu-id="f1768-141">68</span></span>

<span data-ttu-id="f1768-142">Ungültiger Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="f1768-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-143">**Es wurden mehr als 5 Gateways angegeben.**</span><span class="sxs-lookup"><span data-stu-id="f1768-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-144">69</span><span class="sxs-lookup"><span data-stu-id="f1768-144">69</span></span>

<span data-ttu-id="f1768-145">Es wurden mehr als fünf Gateways angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1768-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-146">**Ungültige IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="f1768-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-147">70</span><span class="sxs-lookup"><span data-stu-id="f1768-147">70</span></span>

<span data-ttu-id="f1768-148">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f1768-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-149">**Ungültige Gateway-IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="f1768-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-150">71</span><span class="sxs-lookup"><span data-stu-id="f1768-150">71</span></span>

<span data-ttu-id="f1768-151">Ungültige Gateway-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f1768-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-152">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**</span><span class="sxs-lookup"><span data-stu-id="f1768-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-153">72</span><span class="sxs-lookup"><span data-stu-id="f1768-153">72</span></span>

<span data-ttu-id="f1768-154">Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="f1768-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-155">**Ungültiger Domänen Name**</span><span class="sxs-lookup"><span data-stu-id="f1768-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-156">73</span><span class="sxs-lookup"><span data-stu-id="f1768-156">73</span></span>

<span data-ttu-id="f1768-157">Ungültiger Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="f1768-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-158">**Ungültiger Hostname**</span><span class="sxs-lookup"><span data-stu-id="f1768-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-159">74</span><span class="sxs-lookup"><span data-stu-id="f1768-159">74</span></span>

<span data-ttu-id="f1768-160">Ungültiger Hostname.</span><span class="sxs-lookup"><span data-stu-id="f1768-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-161">**Kein primärer/sekundärer WINS-Server definiert.**</span><span class="sxs-lookup"><span data-stu-id="f1768-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-162">75</span><span class="sxs-lookup"><span data-stu-id="f1768-162">75</span></span>

<span data-ttu-id="f1768-163">Es wurde kein primärer oder sekundärer WINS-Server</span><span class="sxs-lookup"><span data-stu-id="f1768-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-164">**Ungültige Datei**</span><span class="sxs-lookup"><span data-stu-id="f1768-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-165">76</span><span class="sxs-lookup"><span data-stu-id="f1768-165">76</span></span>

<span data-ttu-id="f1768-166">Ungültige Datei.</span><span class="sxs-lookup"><span data-stu-id="f1768-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-167">**Ungültiger Systempfad.**</span><span class="sxs-lookup"><span data-stu-id="f1768-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-168">77</span><span class="sxs-lookup"><span data-stu-id="f1768-168">77</span></span>

<span data-ttu-id="f1768-169">Ungültiger Systempfad.</span><span class="sxs-lookup"><span data-stu-id="f1768-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-170">**Fehler beim Kopieren der Datei**</span><span class="sxs-lookup"><span data-stu-id="f1768-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-171">78</span><span class="sxs-lookup"><span data-stu-id="f1768-171">78</span></span>

<span data-ttu-id="f1768-172">Fehler beim Kopieren der Datei.</span><span class="sxs-lookup"><span data-stu-id="f1768-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-173">**Ungültiger Sicherheitsparameter**</span><span class="sxs-lookup"><span data-stu-id="f1768-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-174">79</span><span class="sxs-lookup"><span data-stu-id="f1768-174">79</span></span>

<span data-ttu-id="f1768-175">Ungültiger Sicherheitsparameter.</span><span class="sxs-lookup"><span data-stu-id="f1768-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-176">**Der TCP/IP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-177">80</span><span class="sxs-lookup"><span data-stu-id="f1768-177">80</span></span>

<span data-ttu-id="f1768-178">Der TCP/IP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f1768-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-179">**DHCP-Dienst kann nicht konfiguriert werden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-180">81</span><span class="sxs-lookup"><span data-stu-id="f1768-180">81</span></span>

<span data-ttu-id="f1768-181">Der DHCP-Dienst kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f1768-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-182">**DHCP-Lease kann nicht erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-183">82</span><span class="sxs-lookup"><span data-stu-id="f1768-183">82</span></span>

<span data-ttu-id="f1768-184">Die DHCP-Lease kann nicht erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="f1768-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-185">**DHCP-Lease kann nicht freigegeben werden**</span><span class="sxs-lookup"><span data-stu-id="f1768-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-186">83</span><span class="sxs-lookup"><span data-stu-id="f1768-186">83</span></span>

<span data-ttu-id="f1768-187">DHCP-Lease kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1768-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-188">**IP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f1768-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-189">84</span><span class="sxs-lookup"><span data-stu-id="f1768-189">84</span></span>

<span data-ttu-id="f1768-190">Die IP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1768-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-191">**IPX ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f1768-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-192">85</span><span class="sxs-lookup"><span data-stu-id="f1768-192">85</span></span>

<span data-ttu-id="f1768-193">IPX ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1768-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-194">**Fehler bei Frame/Netzwerk Nummer.**</span><span class="sxs-lookup"><span data-stu-id="f1768-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-195">86</span><span class="sxs-lookup"><span data-stu-id="f1768-195">86</span></span>

<span data-ttu-id="f1768-196">Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="f1768-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-197">**Ungültiger Frame-Typ**</span><span class="sxs-lookup"><span data-stu-id="f1768-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-198">87</span><span class="sxs-lookup"><span data-stu-id="f1768-198">87</span></span>

<span data-ttu-id="f1768-199">Ungültiger Rahmentyp.</span><span class="sxs-lookup"><span data-stu-id="f1768-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-200">**Ungültige Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="f1768-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-201">88</span><span class="sxs-lookup"><span data-stu-id="f1768-201">88</span></span>

<span data-ttu-id="f1768-202">Ungültige Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="f1768-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-203">**Doppelte Netzwerk Nummer**</span><span class="sxs-lookup"><span data-stu-id="f1768-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-204">89</span><span class="sxs-lookup"><span data-stu-id="f1768-204">89</span></span>

<span data-ttu-id="f1768-205">Doppelte Netzwerk Nummer.</span><span class="sxs-lookup"><span data-stu-id="f1768-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-206">**Parameter außerhalb des gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="f1768-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-207">90</span><span class="sxs-lookup"><span data-stu-id="f1768-207">90</span></span>

<span data-ttu-id="f1768-208">Der Parameter liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="f1768-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-209">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="f1768-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-210">91</span><span class="sxs-lookup"><span data-stu-id="f1768-210">91</span></span>

<span data-ttu-id="f1768-211">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f1768-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-212">**Nicht genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="f1768-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-213">92</span><span class="sxs-lookup"><span data-stu-id="f1768-213">92</span></span>

<span data-ttu-id="f1768-214">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f1768-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-215">**Ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-216">93</span><span class="sxs-lookup"><span data-stu-id="f1768-216">93</span></span>

<span data-ttu-id="f1768-217">Ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f1768-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-218">**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-219">94</span><span class="sxs-lookup"><span data-stu-id="f1768-219">94</span></span>

<span data-ttu-id="f1768-220">Der Pfad, die Datei oder das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f1768-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-221">**Der Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-222">95</span><span class="sxs-lookup"><span data-stu-id="f1768-222">95</span></span>

<span data-ttu-id="f1768-223">Der Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f1768-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-224">**DNS-Dienst kann nicht benachrichtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-225">96</span><span class="sxs-lookup"><span data-stu-id="f1768-225">96</span></span>

<span data-ttu-id="f1768-226">Der DNS-Dienst kann nicht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f1768-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-227">**Schnittstelle nicht konfigurierbar**</span><span class="sxs-lookup"><span data-stu-id="f1768-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-228">97</span><span class="sxs-lookup"><span data-stu-id="f1768-228">97</span></span>

<span data-ttu-id="f1768-229">Schnittstelle nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="f1768-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-230">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**</span><span class="sxs-lookup"><span data-stu-id="f1768-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-231">98</span><span class="sxs-lookup"><span data-stu-id="f1768-231">98</span></span>

<span data-ttu-id="f1768-232">Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="f1768-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-233">**DHCP ist auf dem Adapter nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f1768-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-234">100</span><span class="sxs-lookup"><span data-stu-id="f1768-234">100</span></span>

<span data-ttu-id="f1768-235">DHCP ist auf dem Adapter nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1768-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-236">**Andere**</span><span class="sxs-lookup"><span data-stu-id="f1768-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f1768-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f1768-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f1768-238">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1768-238">Examples</span></span>

<span data-ttu-id="f1768-239">Im Beispiel [Ändern der dynamischen DNS-Registrierung für ein Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript wird die dynamische DNS-Registrierung für einen Netzwerkadapter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f1768-239">The [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript sample configures dynamic DNS registration for a network adapter.</span></span>

<span data-ttu-id="f1768-240">Das [PowerShell-Beispiel Konfigurieren von iSCSI-Netzwerkkarten gemäß Microsoft Best Practices](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatisiert die Konfigurationseinstellungen für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f1768-240">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1768-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1768-241">Requirements</span></span>



| <span data-ttu-id="f1768-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1768-242">Requirement</span></span> | <span data-ttu-id="f1768-243">Wert</span><span class="sxs-lookup"><span data-stu-id="f1768-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1768-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1768-244">Minimum supported client</span></span><br/> | <span data-ttu-id="f1768-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1768-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1768-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1768-246">Minimum supported server</span></span><br/> | <span data-ttu-id="f1768-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1768-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1768-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1768-248">Namespace</span></span><br/>                | <span data-ttu-id="f1768-249">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1768-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1768-250">MOF</span><span class="sxs-lookup"><span data-stu-id="f1768-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1768-251"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f1768-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1768-252">DLL</span><span class="sxs-lookup"><span data-stu-id="f1768-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1768-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1768-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1768-254">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1768-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1768-255">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="f1768-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f1768-256">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="f1768-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f1768-257">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f1768-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f1768-258">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="f1768-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f1768-259">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="f1768-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

