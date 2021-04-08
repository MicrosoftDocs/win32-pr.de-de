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
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Konfigurieren der Registrierung für Port Belegungen und selektive Bindung

Ab Windows 2000 sollte ein Dienstprogramm im Windows Resource Kit namens Rpccfg.exe zum Festlegen von Bindungen verwendet werden. Weitere Informationen finden Sie im Windows Resource Kit, um die entsprechende Betriebssystemversion zu erhalten.

Bei Windows-Versionen vor Windows 2000 werden in den Registrierungs Schlüsseln in der folgenden Tabelle die System Standardwerte für die dynamische Port Zuweisung und die Bindung an NICs auf mehrfach vernetzten Computern angegeben. Sie müssen diese Schlüssel zuerst erstellen und dann die entsprechenden Einstellungen angeben.

Die Verwendung der [**rpcserveruseprotabsqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) -Funktion wirkt sich auf diese Einstellungen aus. Entwickler sollten mit den Registrierungs Einstellungen vertraut sein, die in diesem Abschnitt erläutert werden, und die Funktion **rpcserveruseprotsetqex** beim Verwalten von Port Zuweisungen. Ein Beispiel mit drei hypothetischen Anwendungen folgt der Tabelle unten und veranschaulicht, wie diese Einstellungen und die Funktion **rpcserveruseprotsetqex** zusammenarbeiten.

Wenn eine Taste fehlt oder wenn Sie einen ungültigen Wert enthält, wird die gesamte Konfiguration als ungültig markiert, und alle **RpcServerUseProtseq \*** -Aufrufe über [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) oder [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) können fehlschlagen.

> [!Note]  
> Ports, die einem Prozess zugeordnet sind, bleiben so lange zugewiesen, bis dieser Prozess nicht mehr Wenn alle verfügbaren Ports verwendet werden, gibt die Funktion RPC- \_ S \_ aus den Ressourcen zurück \_ \_ .

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Port Schlüssel</th>
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
<td>Gibt eine Gruppe von IP-Port Bereichen an, die entweder aus allen Ports aus dem Internet oder aus allen Ports bestehen, die über das Internet nicht verfügbar sind. Jede Zeichenfolge stellt einen einzelnen Port oder einen inklusiven Satz von Ports dar (z. b. 1000-1050, 1984). Wenn Einträge außerhalb des Bereichs 0 bis 65535 liegen, oder wenn eine beliebige Zeichenfolge nicht interpretiert werden kann, wird die gesamte Konfiguration von der RPC-Laufzeit als ungültig behandelt.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y oder N (keine Unterscheidung nach Groß-/Kleinschreibung). Wenn der Wert Y lautet, sind die Ports, die im Ports-Schlüssel aufgeführt sind, alle Ports, die für das Internet verfügbar sind Wenn N, sind die im Ports-Schlüssel aufgeführten Ports alle Ports, die nicht Internet verfügbar sind.</td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y oder N (keine Unterscheidung nach Groß-/Kleinschreibung). Gibt die Standard Richtlinie des Systems an. Wenn Y, werden den Prozessen, die den Standardwert verwenden, die Ports aus dem Satz der mit dem Internet verfügbaren Ports zugewiesen, wie oben definiert. Wenn N, werden Prozesse, die den Standardwert verwenden, Ports aus dem Satz von nur intranetports zugewiesen.</td>
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
<td>Listet die Gerätenamen aller NICs auf, an die standardmäßig gebunden werden soll (z. b. \device\amdpcn1). Wenn der Schlüssel nicht vorhanden ist, wird der Server an alle NICs gebunden. Wenn der Schlüssel vorhanden ist, wird der Server an die im Schlüssel angegebenen NICs gebunden, es sei denn, das Feld nicflags ist auf RPC_C_BIND_TO_ALL_NICS festgelegt. Wenn der Schlüssel einen NULL &quot; &quot; -Wert () aufweist, wird die Konfiguration als ungültig markiert, und alle Aufrufe von <strong>RpcServerUseProtseq *</strong> über <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> oder <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> schlagen fehl.</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle ist dargestellt, wie die drei Beispielanwendungen von den in der vorherigen Tabelle definierten Einstellungen betroffen sind und wie Einstellungen, die mithilfe der Funktion [**rpcserveruseprotabsqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) angewendet werden, ebenfalls betroffen sind.

In diesem Beispiel werden drei hypothetische Anwendungen berücksichtigt:

-   Interverschachteltapp: diese Anwendung ist für das Internet verfügbar und hat \_ \_ \_ \_ im **endpointflags** -Member der [**RPC- \_ Richtlinien**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) Struktur, die an die Funktion [**rpcserveruseprotseqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übergebene RPC-C-Port verwenden, den angegebenen RPC-C-Port verwenden.
-   Localapp: diese Anwendung ist nicht für das Internet verfügbar und hat den RPC-C- \_ \_ use- \_ Intranet- \_ Port im **endpointflags** -Member der [**RPC- \_ Richtlinien**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) Struktur angegeben, die an die Funktion [**rpcserveruseprotseqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übermittelt wurde.
-   Defaultapp: diese Anwendung gibt 0 (null) im **endpointflags** -Member der [**RPC- \_ Richtlinien**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) Struktur an, die an die Funktion [**rpcserveruseprotseqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übermittelt wurde.

In der folgenden Tabelle werden die Auswirkung dieser Einstellungen auf Grundlage von Werten erläutert, die in den in der vorherigen Tabelle beschriebenen Registrierungs Einträgen angegeben sind. Für Formatierungs Überlegungen werden die folgenden Codes zugewiesen:

Pia = portsinternettavailable-Schlüsselwert

UIP = Wert für den Schlüsselwert von "EIP"

Der Wert des Ports Key für dieses Beispiel ist 5000-5100 für jeden Eintrag.



| Application | PIA | UIP | Ergebnis                                  |
|-------------|-----|-----|-----------------------------------------|
| Internetztapp | J   | J   | Verwendet Ports zwischen 5000 und 5100.        |
| Localapp    | J   | J   | Verwendet einen Port außerhalb des 5000-5100-Bereichs. |
| DefaultApp  | J   | J   | Verwendet Ports zwischen 5000 und 5100.        |
| Internetztapp | J   | N   | Verwendet Ports zwischen 5000 und 5100.        |
| Localapp    | J   | N   | Verwendet einen Port außerhalb des 5000-5100-Bereichs. |
| DefaultApp  | J   | N   | Verwendet einen Port außerhalb des 5000-5100-Bereichs. |
| Internetztapp | N   | J   | Verwendet einen Port außerhalb des 5000-5100-Bereichs. |
| Localapp    | N   | J   | Verwendet Ports zwischen 5000 und 5100.        |
| DefaultApp  | N   | J   | Verwendet einen Port außerhalb des 5000-5100-Bereichs. |
| Internetztapp | N   | N   | Verwendet einen Port außerhalb des 5000-5100-Bereichs. |
| Localapp    | N   | N   | Verwendet Ports zwischen 5000 und 5100.        |
| DefaultApp  | N   | N   | Verwendet Ports zwischen 5000 und 5100.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**RPC- \_ Richtlinie**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[**Rpcserveruseallprotabqsex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[**Rpcserveruseallprotabqsifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[**Rpcserveruseprotabqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[**Rpcserveruseprotabqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[**Rpcserveruseprotabqifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**ncadg \_ -IP- \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 