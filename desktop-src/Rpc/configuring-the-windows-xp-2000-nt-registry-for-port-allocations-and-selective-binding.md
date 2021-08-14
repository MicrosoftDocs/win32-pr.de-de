---
title: Konfigurieren der Registrierung für Portzuordnungen und selektive Bindung
description: Ab Windows 2000 sollte ein Hilfsprogramm im Windows Resource Kit mit dem Namen Rpccfg.exe verwendet werden, um Bindungen festzulegen. Weitere Informationen finden Sie im Windows Resource Kit für die entsprechende Betriebssystemversion.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Remoteprozeduraufruf RPC , Tasks, Konfigurieren der Registrierung für Portzuordnungen und selektive Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8166e9cb4d6706e8eafb016fba309eb64a4c4910b5727bcf88c2e071a7077d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931247"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Konfigurieren der Registrierung für Portzuordnungen und selektive Bindung

Ab Windows 2000 sollte ein Hilfsprogramm im Windows Resource Kit mit dem Namen Rpccfg.exe verwendet werden, um Bindungen festzulegen. Weitere Informationen finden Sie im Windows Resource Kit für die entsprechende Betriebssystemversion.

Für Windows-Versionen vor Windows 2000 geben die Registrierungsschlüssel in der folgenden Tabelle die Systemstandardeinstellungen für die dynamische Portzuordnung und die Bindung an NICs auf mehr vernetzten Computern an. Sie müssen diese Schlüssel zunächst erstellen und dann die entsprechenden Einstellungen angeben.

Die Verwendung der [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) wirkt sich auf diese Einstellungen aus. Entwickler sollten mit den in diesem Abschnitt erläuterten Registrierungseinstellungen und der **RpcServerUseProtseqEx-Funktion** vertraut sein, wenn sie Portzuordnungen verwalten. Ein Beispiel mit drei hypothetischen Anwendungen folgt der folgenden Tabelle und veranschaulicht, wie diese Einstellungen und die **RpcServerUseProtseqEx-Funktion** zusammenarbeiten.

Wenn ein Schlüssel fehlt oder einen ungültigen Wert enthält, wird die gesamte Konfiguration als ungültig markiert, und alle **RpcServerUseProtseq \** _-Aufrufe über [_ *ncacn \_ ip \_ tcp* *](/windows/desktop/Midl/ncacn-ip-tcp) oder [**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp) schlagen fehl.

> [!Note]  
> Ports, die einem Prozess zugeordnet sind, bleiben so lange zugeordnet, bis dieser Prozess abendet. Wenn alle verfügbaren Ports verwendet werden, gibt die Funktion RPC \_ S OUT OF RESOURCES \_ \_ \_ zurück.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Portschlüssel</th>
<th>Datentyp</th>
<th>BESCHREIBUNG</th>
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
<td><strong>REG_MULTI_SZ</strong></td>
<td>Gibt einen Satz von IP-Portbereichen an, die entweder aus allen ports bestehen, die über das Internet verfügbar sind, oder aus allen Ports, die nicht über das Internet verfügbar sind. Jede Zeichenfolge stellt einen einzelnen Port oder einen inklusiven Satz von Ports dar (z.B. 1000-1050, 1984). Wenn Einträge außerhalb des Bereichs von 0 bis 65535 liegen oder keine Zeichenfolge interpretiert werden kann, behandelt die RPC-Laufzeit die gesamte Konfiguration als ungültig.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y oder N (groß-/kleinschreibung wird nicht beachtet). Bei Y handelt es sich bei den im Schlüssel Ports aufgeführten Ports um die ports, die auf diesem Computer über das Internet verfügbar sind. Bei N handelt es sich bei den im Schlüssel Ports aufgeführten Ports um alle Ports, die nicht über das Internet verfügbar sind.</td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y oder N (groß-/kleinschreibung wird nicht beachtet). Gibt die Systemstandardrichtlinie an. Bei Y werden den Prozessen, die den Standardwert verwenden, Ports aus der Gruppe der ports zugewiesen, die über das Internet verfügbar sind, wie oben definiert. Wenn N, werden Prozessen, die den Standard verwenden, Ports aus dem Satz von reinen Intranetports zugewiesen.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Listet die Gerätenamen aller NICs auf, an die standardmäßig gebunden werden soll (z. B. \Device\AMDPCN1). Wenn der Schlüssel nicht vorhanden ist, wird der Server an alle NICs gebunden. Wenn der Schlüssel vorhanden ist, wird der Server an die im Schlüssel angegebenen NICs gebunden, es sei denn, das Feld NICFlags ist auf RPC_C_BIND_TO_ALL_NICS festgelegt. Wenn der Schlüssel über einen &quot; &quot; NULL-Wert () verfügt, wird die Konfiguration als ungültig markiert, und alle Aufrufe von <strong>RpcServerUseProtseq*</strong> über <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> oder <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> schlagen fehl.</td>
</tr>
</tbody>
</table>



 

Die folgende Tabelle veranschaulicht, wie sich die in der vorherigen Tabelle definierten Einstellungen auf drei Beispielanwendungen auswirken und wie einstellungen, die mit der [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) angewendet werden, ebenfalls betroffen sind.

In diesem Beispiel werden drei hypothetische Anwendungen berücksichtigt:

-   InternetApp: Diese Anwendung ist für die Internetverbindung vorgesehen und hat RPC \_ C USE INTERNET PORT im \_ \_ \_ **EndpointFlags-Member** der [**RPC \_ POLICY-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) angegeben, die an die [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übergeben wird.
-   LocalApp: Diese Anwendung ist nicht für die Internetverbindung vorgesehen und hat den RPC \_ C USE INTRANET PORT im \_ \_ \_ **EndpointFlags-Member** der [**RPC \_ POLICY-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) angegeben, die an die [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übergeben wird.
-   DefaultApp: Diese Anwendung gibt 0 (null) im **EndpointFlags-Member** der [**RPC \_ POLICY-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) an, die an die [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übergeben wird.

In der folgenden Tabelle werden die Auswirkungen dieser Einstellungen anhand der werte erläutert, die in den in der vorherigen Tabelle erläuterten Registrierungseinträgen angegeben sind. Für Formatierungsüberlegungen werden die folgenden Codes zugewiesen:

PIA = PortsInternetAvailable-Schlüsselwert

UIP = UseInternetPorts-Schlüsselwert

Der Wert des Ports-Schlüssels für dieses Beispiel ist für jeden Eintrag 5000-5100.



| Application | PIA | Uip | Ergebnis                                  |
|-------------|-----|-----|-----------------------------------------|
| InternetApp | J   | J   | Verwendet Ports zwischen 5000 und 5100.        |
| LocalApp    | J   | J   | Verwendet einen Port außerhalb des Bereichs 5000-5100. |
| DefaultApp  | J   | J   | Verwendet Ports zwischen 5000 und 5100.        |
| InternetApp | J   | N   | Verwendet Ports zwischen 5000 und 5100.        |
| LocalApp    | J   | N   | Verwendet einen Port außerhalb des Bereichs 5000-5100. |
| DefaultApp  | J   | N   | Verwendet einen Port außerhalb des Bereichs 5000-5100. |
| InternetApp | N   | J   | Verwendet einen Port außerhalb des Bereichs 5000-5100. |
| LocalApp    | N   | J   | Verwendet Ports zwischen 5000 und 5100.        |
| DefaultApp  | N   | J   | Verwendet einen Port außerhalb des Bereichs 5000-5100. |
| InternetApp | N   | N   | Verwendet einen Port außerhalb des Bereichs 5000-5100. |
| LocalApp    | N   | N   | Verwendet Ports zwischen 5000 und 5100.        |
| DefaultApp  | N   | N   | Verwendet Ports zwischen 5000 und 5100.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_RPC-RICHTLINIE**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[**RpcServerUseProtseqIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 