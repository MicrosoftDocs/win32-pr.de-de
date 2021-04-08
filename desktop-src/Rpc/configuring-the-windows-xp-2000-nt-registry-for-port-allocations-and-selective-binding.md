---
title: Konfigurieren der Registrierung für Port Belegungen und selektive Bindung
description: Ab Windows 2000 sollte ein Dienstprogramm im Windows Resource Kit namens Rpccfg.exe zum Festlegen von Bindungen verwendet werden. Weitere Informationen finden Sie im Windows Resource Kit, um die entsprechende Betriebssystemversion zu erhalten.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Konfigurieren der Registrierung für Port Belegungen und selektive Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103949192"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a><span data-ttu-id="a84fd-105">Konfigurieren der Registrierung für Port Belegungen und selektive Bindung</span><span class="sxs-lookup"><span data-stu-id="a84fd-105">Configuring the Registry for Port Allocations and Selective Binding</span></span>

<span data-ttu-id="a84fd-106">Ab Windows 2000 sollte ein Dienstprogramm im Windows Resource Kit namens Rpccfg.exe zum Festlegen von Bindungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a84fd-106">Starting with Windows 2000, a utility in the Windows Resource Kit called Rpccfg.exe should be used to set bindings.</span></span> <span data-ttu-id="a84fd-107">Weitere Informationen finden Sie im Windows Resource Kit, um die entsprechende Betriebssystemversion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a84fd-107">For more information, consult the Windows Resource Kit for the appropriate operating system version.</span></span>

<span data-ttu-id="a84fd-108">Bei Windows-Versionen vor Windows 2000 werden in den Registrierungs Schlüsseln in der folgenden Tabelle die System Standardwerte für die dynamische Port Zuweisung und die Bindung an NICs auf mehrfach vernetzten Computern angegeben.</span><span class="sxs-lookup"><span data-stu-id="a84fd-108">For versions of windows prior to Windows 2000, the registry keys in the following table specify the system defaults for dynamic port allocation and for binding to NICs on multihomed computers.</span></span> <span data-ttu-id="a84fd-109">Sie müssen diese Schlüssel zuerst erstellen und dann die entsprechenden Einstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="a84fd-109">You must first create these keys and then specify the appropriate settings.</span></span>

<span data-ttu-id="a84fd-110">Die Verwendung der [**rpcserveruseprotabsqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) -Funktion wirkt sich auf diese Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="a84fd-110">Using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function affects these settings.</span></span> <span data-ttu-id="a84fd-111">Entwickler sollten mit den Registrierungs Einstellungen vertraut sein, die in diesem Abschnitt erläutert werden, und die Funktion **rpcserveruseprotsetqex** beim Verwalten von Port Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="a84fd-111">Developers should be familiar with the registry settings explained in this section and the **RpcServerUseProtseqEx** function when managing port allocations.</span></span> <span data-ttu-id="a84fd-112">Ein Beispiel mit drei hypothetischen Anwendungen folgt der Tabelle unten und veranschaulicht, wie diese Einstellungen und die Funktion **rpcserveruseprotsetqex** zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a84fd-112">An example with three hypothetical applications follows the table below, and illustrates how these settings and the **RpcServerUseProtseqEx** function interoperate.</span></span>

<span data-ttu-id="a84fd-113">Wenn eine Taste fehlt oder wenn Sie einen ungültigen Wert enthält, wird die gesamte Konfiguration als ungültig markiert, und alle **RpcServerUseProtseq \*** -Aufrufe über [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) oder [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) können fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="a84fd-113">If a key is missing or if it contains an invalid value, the entire configuration is marked as invalid, and all **RpcServerUseProtseq\*** calls over [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) or [**ncadg\_ip\_udp**](/windows/desktop/Midl/ncadg-ip-udp) will fail.</span></span>

> [!Note]  
> <span data-ttu-id="a84fd-114">Ports, die einem Prozess zugeordnet sind, bleiben so lange zugewiesen, bis dieser Prozess nicht mehr</span><span class="sxs-lookup"><span data-stu-id="a84fd-114">Ports allocated to a process remain allocated until that process dies.</span></span> <span data-ttu-id="a84fd-115">Wenn alle verfügbaren Ports verwendet werden, gibt die Funktion RPC- \_ S \_ aus den Ressourcen zurück \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a84fd-115">If all available ports are in use, the function returns RPC\_S\_OUT\_OF\_RESOURCES.</span></span>

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a84fd-116">Port Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a84fd-116">Port key</span></span></th>
<th><span data-ttu-id="a84fd-117">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a84fd-117">Data type</span></span></th>
<th><span data-ttu-id="a84fd-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a84fd-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><span data-ttu-id="a84fd-119"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="a84fd-119"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="a84fd-120">Gibt eine Gruppe von IP-Port Bereichen an, die entweder aus allen Ports aus dem Internet oder aus allen Ports bestehen, die über das Internet nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a84fd-120">Specifies a set of IP port ranges consisting of either all the ports available from the Internet or all the ports not available from the Internet.</span></span> <span data-ttu-id="a84fd-121">Jede Zeichenfolge stellt einen einzelnen Port oder einen inklusiven Satz von Ports dar (z. b. 1000-1050, 1984).</span><span class="sxs-lookup"><span data-stu-id="a84fd-121">Each string represents a single port or an inclusive set of ports (for example,1000-1050, 1984).</span></span> <span data-ttu-id="a84fd-122">Wenn Einträge außerhalb des Bereichs 0 bis 65535 liegen, oder wenn eine beliebige Zeichenfolge nicht interpretiert werden kann, wird die gesamte Konfiguration von der RPC-Laufzeit als ungültig behandelt.</span><span class="sxs-lookup"><span data-stu-id="a84fd-122">If any entries are outside the range 0 to 65535, or if any string cannot be interpreted, the RPC run time will treat the entire configuration as invalid.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><span data-ttu-id="a84fd-123"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="a84fd-123"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="a84fd-124">Y oder N (keine Unterscheidung nach Groß-/Kleinschreibung).</span><span class="sxs-lookup"><span data-stu-id="a84fd-124">Y or N (not case-sensitive).</span></span> <span data-ttu-id="a84fd-125">Wenn der Wert Y lautet, sind die Ports, die im Ports-Schlüssel aufgeführt sind, alle Ports, die für das Internet verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="a84fd-125">If Y, the ports listed in the Ports key are all the Internet-available ports on that computer.</span></span> <span data-ttu-id="a84fd-126">Wenn N, sind die im Ports-Schlüssel aufgeführten Ports alle Ports, die nicht Internet verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a84fd-126">If N, the ports listed in the Ports key are all those ports that are not Internet-available.</span></span></td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><span data-ttu-id="a84fd-127"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="a84fd-127"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="a84fd-128">Y oder N (keine Unterscheidung nach Groß-/Kleinschreibung).</span><span class="sxs-lookup"><span data-stu-id="a84fd-128">Y or N (not case-sensitive).</span></span> <span data-ttu-id="a84fd-129">Gibt die Standard Richtlinie des Systems an.</span><span class="sxs-lookup"><span data-stu-id="a84fd-129">Specifies the system default policy.</span></span> <span data-ttu-id="a84fd-130">Wenn Y, werden den Prozessen, die den Standardwert verwenden, die Ports aus dem Satz der mit dem Internet verfügbaren Ports zugewiesen, wie oben definiert.</span><span class="sxs-lookup"><span data-stu-id="a84fd-130">If Y, the processes using the default will be assigned ports from the set of Internet-available ports, as defined above.</span></span> <span data-ttu-id="a84fd-131">Wenn N, werden Prozesse, die den Standardwert verwenden, Ports aus dem Satz von nur intranetports zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a84fd-131">If N, processes using the default will be assigned ports from the set of intranet-only ports.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><span data-ttu-id="a84fd-132"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="a84fd-132"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="a84fd-133">Listet die Gerätenamen aller NICs auf, an die standardmäßig gebunden werden soll (z. b. \device\amdpcn1).</span><span class="sxs-lookup"><span data-stu-id="a84fd-133">Lists the device names of all the NICs on which to bind by default (for example, \Device\AMDPCN1).</span></span> <span data-ttu-id="a84fd-134">Wenn der Schlüssel nicht vorhanden ist, wird der Server an alle NICs gebunden.</span><span class="sxs-lookup"><span data-stu-id="a84fd-134">If the key does not exist, the server will bind to all NICs.</span></span> <span data-ttu-id="a84fd-135">Wenn der Schlüssel vorhanden ist, wird der Server an die im Schlüssel angegebenen NICs gebunden, es sei denn, das Feld nicflags ist auf RPC_C_BIND_TO_ALL_NICS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a84fd-135">If the key does exist, the server will bind to the NICs specified in the key, unless the NICFlags field is set to RPC_C_BIND_TO_ALL_NICS.</span></span> <span data-ttu-id="a84fd-136">Wenn der Schlüssel einen NULL &quot; &quot; -Wert () aufweist, wird die Konfiguration als ungültig markiert, und alle Aufrufe von <strong>RpcServerUseProtseq \*</strong> über <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> oder <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> schlagen fehl.</span><span class="sxs-lookup"><span data-stu-id="a84fd-136">If the key has a null (&quot;&quot;) value, the configuration will be marked as invalid and all calls to <strong>RpcServerUseProtseq\*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> or <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> will fail.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a84fd-137">In der folgenden Tabelle ist dargestellt, wie die drei Beispielanwendungen von den in der vorherigen Tabelle definierten Einstellungen betroffen sind und wie Einstellungen, die mithilfe der Funktion [**rpcserveruseprotabsqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) angewendet werden, ebenfalls betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="a84fd-137">The following table illustrates how three sample applications are affected by the settings defined in the previous table, and how settings applied using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function are also affected.</span></span>

<span data-ttu-id="a84fd-138">In diesem Beispiel werden drei hypothetische Anwendungen berücksichtigt:</span><span class="sxs-lookup"><span data-stu-id="a84fd-138">In this example, three hypothetical applications are considered:</span></span>

-   <span data-ttu-id="a84fd-139">Interverschachteltapp: diese Anwendung ist für das Internet verfügbar und hat \_ \_ \_ \_ im **endpointflags** -Member der [**RPC- \_ Richtlinien**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) Struktur, die an die Funktion [**rpcserveruseprotseqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übergebene RPC-C-Port verwenden, den angegebenen RPC-C-Port verwenden.</span><span class="sxs-lookup"><span data-stu-id="a84fd-139">InternetApp: This application is intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTERNET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="a84fd-140">Localapp: diese Anwendung ist nicht für das Internet verfügbar und hat den RPC-C- \_ \_ use- \_ Intranet- \_ Port im **endpointflags** -Member der [**RPC- \_ Richtlinien**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) Struktur angegeben, die an die Funktion [**rpcserveruseprotseqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a84fd-140">LocalApp: This application is not intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTRANET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="a84fd-141">Defaultapp: diese Anwendung gibt 0 (null) im **endpointflags** -Member der [**RPC- \_ Richtlinien**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) Struktur an, die an die Funktion [**rpcserveruseprotseqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a84fd-141">DefaultApp: This application specifies zero in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>

<span data-ttu-id="a84fd-142">In der folgenden Tabelle werden die Auswirkung dieser Einstellungen auf Grundlage von Werten erläutert, die in den in der vorherigen Tabelle beschriebenen Registrierungs Einträgen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a84fd-142">The following table explains the impact these settings have based on values specified in the registry entries explained in the previous table.</span></span> <span data-ttu-id="a84fd-143">Für Formatierungs Überlegungen werden die folgenden Codes zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="a84fd-143">For formatting considerations, the following codes are assigned:</span></span>

<span data-ttu-id="a84fd-144">Pia = portsinternettavailable-Schlüsselwert</span><span class="sxs-lookup"><span data-stu-id="a84fd-144">PIA = PortsInternetAvailable Key value</span></span>

<span data-ttu-id="a84fd-145">UIP = Wert für den Schlüsselwert von "EIP"</span><span class="sxs-lookup"><span data-stu-id="a84fd-145">UIP = UseInternetPorts Key value</span></span>

<span data-ttu-id="a84fd-146">Der Wert des Ports Key für dieses Beispiel ist 5000-5100 für jeden Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a84fd-146">The value of the Ports key, for sake of this example, is 5000-5100 for each entry.</span></span>



| <span data-ttu-id="a84fd-147">Application</span><span class="sxs-lookup"><span data-stu-id="a84fd-147">Application</span></span> | <span data-ttu-id="a84fd-148">PIA</span><span class="sxs-lookup"><span data-stu-id="a84fd-148">PIA</span></span> | <span data-ttu-id="a84fd-149">UIP</span><span class="sxs-lookup"><span data-stu-id="a84fd-149">UIP</span></span> | <span data-ttu-id="a84fd-150">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a84fd-150">Result</span></span>                                  |
|-------------|-----|-----|-----------------------------------------|
| <span data-ttu-id="a84fd-151">Internetztapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-151">InternetApp</span></span> | <span data-ttu-id="a84fd-152">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-152">Y</span></span>   | <span data-ttu-id="a84fd-153">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-153">Y</span></span>   | <span data-ttu-id="a84fd-154">Verwendet Ports zwischen 5000 und 5100.</span><span class="sxs-lookup"><span data-stu-id="a84fd-154">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="a84fd-155">Localapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-155">LocalApp</span></span>    | <span data-ttu-id="a84fd-156">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-156">Y</span></span>   | <span data-ttu-id="a84fd-157">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-157">Y</span></span>   | <span data-ttu-id="a84fd-158">Verwendet einen Port außerhalb des 5000-5100-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a84fd-158">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="a84fd-159">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="a84fd-159">DefaultApp</span></span>  | <span data-ttu-id="a84fd-160">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-160">Y</span></span>   | <span data-ttu-id="a84fd-161">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-161">Y</span></span>   | <span data-ttu-id="a84fd-162">Verwendet Ports zwischen 5000 und 5100.</span><span class="sxs-lookup"><span data-stu-id="a84fd-162">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="a84fd-163">Internetztapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-163">InternetApp</span></span> | <span data-ttu-id="a84fd-164">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-164">Y</span></span>   | <span data-ttu-id="a84fd-165">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-165">N</span></span>   | <span data-ttu-id="a84fd-166">Verwendet Ports zwischen 5000 und 5100.</span><span class="sxs-lookup"><span data-stu-id="a84fd-166">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="a84fd-167">Localapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-167">LocalApp</span></span>    | <span data-ttu-id="a84fd-168">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-168">Y</span></span>   | <span data-ttu-id="a84fd-169">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-169">N</span></span>   | <span data-ttu-id="a84fd-170">Verwendet einen Port außerhalb des 5000-5100-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a84fd-170">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="a84fd-171">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="a84fd-171">DefaultApp</span></span>  | <span data-ttu-id="a84fd-172">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-172">Y</span></span>   | <span data-ttu-id="a84fd-173">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-173">N</span></span>   | <span data-ttu-id="a84fd-174">Verwendet einen Port außerhalb des 5000-5100-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a84fd-174">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="a84fd-175">Internetztapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-175">InternetApp</span></span> | <span data-ttu-id="a84fd-176">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-176">N</span></span>   | <span data-ttu-id="a84fd-177">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-177">Y</span></span>   | <span data-ttu-id="a84fd-178">Verwendet einen Port außerhalb des 5000-5100-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a84fd-178">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="a84fd-179">Localapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-179">LocalApp</span></span>    | <span data-ttu-id="a84fd-180">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-180">N</span></span>   | <span data-ttu-id="a84fd-181">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-181">Y</span></span>   | <span data-ttu-id="a84fd-182">Verwendet Ports zwischen 5000 und 5100.</span><span class="sxs-lookup"><span data-stu-id="a84fd-182">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="a84fd-183">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="a84fd-183">DefaultApp</span></span>  | <span data-ttu-id="a84fd-184">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-184">N</span></span>   | <span data-ttu-id="a84fd-185">J</span><span class="sxs-lookup"><span data-stu-id="a84fd-185">Y</span></span>   | <span data-ttu-id="a84fd-186">Verwendet einen Port außerhalb des 5000-5100-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a84fd-186">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="a84fd-187">Internetztapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-187">InternetApp</span></span> | <span data-ttu-id="a84fd-188">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-188">N</span></span>   | <span data-ttu-id="a84fd-189">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-189">N</span></span>   | <span data-ttu-id="a84fd-190">Verwendet einen Port außerhalb des 5000-5100-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a84fd-190">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="a84fd-191">Localapp</span><span class="sxs-lookup"><span data-stu-id="a84fd-191">LocalApp</span></span>    | <span data-ttu-id="a84fd-192">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-192">N</span></span>   | <span data-ttu-id="a84fd-193">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-193">N</span></span>   | <span data-ttu-id="a84fd-194">Verwendet Ports zwischen 5000 und 5100.</span><span class="sxs-lookup"><span data-stu-id="a84fd-194">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="a84fd-195">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="a84fd-195">DefaultApp</span></span>  | <span data-ttu-id="a84fd-196">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-196">N</span></span>   | <span data-ttu-id="a84fd-197">N</span><span class="sxs-lookup"><span data-stu-id="a84fd-197">N</span></span>   | <span data-ttu-id="a84fd-198">Verwendet Ports zwischen 5000 und 5100.</span><span class="sxs-lookup"><span data-stu-id="a84fd-198">Uses ports between 5000 and 5100</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a84fd-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a84fd-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a84fd-200">**RPC- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a84fd-200">**RPC\_POLICY**</span></span>](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[<span data-ttu-id="a84fd-201">**Rpcserveruseallprotabqsex**</span><span class="sxs-lookup"><span data-stu-id="a84fd-201">**RpcServerUseAllProtseqsEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[<span data-ttu-id="a84fd-202">**Rpcserveruseallprotabqsifex**</span><span class="sxs-lookup"><span data-stu-id="a84fd-202">**RpcServerUseAllProtseqsIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[<span data-ttu-id="a84fd-203">**Rpcserveruseprotabqex**</span><span class="sxs-lookup"><span data-stu-id="a84fd-203">**RpcServerUseProtseqEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[<span data-ttu-id="a84fd-204">**Rpcserveruseprotabqepex**</span><span class="sxs-lookup"><span data-stu-id="a84fd-204">**RpcServerUseProtseqEpEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[<span data-ttu-id="a84fd-205">**Rpcserveruseprotabqifex**</span><span class="sxs-lookup"><span data-stu-id="a84fd-205">**RpcServerUseProtseqIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[<span data-ttu-id="a84fd-206">**ncacn \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="a84fd-206">**ncacn\_ip\_tcp**</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[<span data-ttu-id="a84fd-207">**ncadg \_ -IP- \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="a84fd-207">**ncadg\_ip\_udp**</span></span>](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 