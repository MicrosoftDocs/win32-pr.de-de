---
title: Konfigurieren der Registrierung für Portzuordnungen und selektive Bindung
description: Ab Windows 2000 sollte ein Hilfsprogramm im Windows Resource Kit namens Rpccfg.exe zum Festlegen von Bindungen verwendet werden. Weitere Informationen finden Sie im Windows Resource Kit für die entsprechende Betriebssystemversion.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- REMOTE PROCEDURE Call RPC , Tasks, Konfigurieren der Registrierung für Portzuordnungen und selektive Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b220e0e3415b7906c847c0f1196fbc815521dee0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465477"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Konfigurieren der Registrierung für Portzuordnungen und selektive Bindung

Ab Windows 2000 sollte ein Hilfsprogramm im Windows Resource Kit namens Rpccfg.exe zum Festlegen von Bindungen verwendet werden. Weitere Informationen finden Sie im Windows Resource Kit für die entsprechende Betriebssystemversion.

Für Windows-Versionen vor Windows 2000 geben die Registrierungsschlüssel in der folgenden Tabelle die Systemeinstellungen für die dynamische Portzuordnung und die Bindung an NICs auf mehrfach vernetzten Computern an. Sie müssen zuerst diese Schlüssel erstellen und dann die entsprechenden Einstellungen angeben.

Die Verwendung [**der RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) wirkt sich auf diese Einstellungen aus. Entwickler sollten mit den registrierungseinstellungen vertraut sein, die in diesem Abschnitt erläutert werden, und mit der **RpcServerUseProtseqEx-Funktion** beim Verwalten von Portzuordnungen. Ein Beispiel mit drei hypothetischen Anwendungen folgt der folgenden Tabelle und veranschaulicht, wie diese Einstellungen und die **RpcServerUseProtseqEx-Funktion** zusammenarbeiten.

Wenn ein Schlüssel fehlt oder einen ungültigen Wert enthält, wird die gesamte Konfiguration als ungültig markiert, und alle **RpcServerUseProtseq \** _-Aufrufe über [_ *ncacn \_ ip \_ tcp* *](/windows/desktop/Midl/ncacn-ip-tcp) oder [**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp) führen zu einem Fehler.

> [!Note]  
> Ports, die einem Prozess zugeordnet sind, bleiben zugeordnet, bis dieser Prozess abfing. Wenn alle verfügbaren Ports verwendet werden, gibt die Funktion RPC \_ S OUT OF RESOURCES \_ \_ \_ zurück.

 




| Portschlüssel | Datentyp | BESCHREIBUNG | 
|----------|-----------|-------------|
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               Ports</code></pre> | <strong>REG_MULTI_SZ</strong> | Gibt eine Gruppe von IP-Portbereichen an, die entweder aus allen ports bestehen, die über das Internet verfügbar sind, oder aus allen Ports, die nicht über das Internet verfügbar sind. Jede Zeichenfolge stellt einen einzelnen Port oder einen inklusiven Portsatz dar (z.B. 1000-1050, 1984). Wenn Einträge außerhalb des Bereichs von 0 bis 65535 liegen oder eine Zeichenfolge nicht interpretiert werden kann, behandelt die RPC-Laufzeit die gesamte Konfiguration als ungültig. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               PortsInternetAvailable</code></pre> | <strong>REG_SZ</strong> | Y oder N (ohne Sensitivität bei der Schreibung). Bei Y handelt es sich bei den im Schlüssel Ports aufgeführten Ports um alle ports, die für das Internet auf diesem Computer verfügbar sind. Bei N handelt es sich bei den Ports, die im Schlüssel Ports aufgeführt sind, um alle Ports, die nicht über das Internet verfügbar sind. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               UseInternetPorts</code></pre> | <strong>REG_SZ</strong> | Y oder N (ohne Sensitivität bei der Schreibung). Gibt die Standardrichtlinie des Systems an. Wenn Y festgelegt ist, werden den Prozessen, die den Standardwert verwenden, Ports aus dem Satz von Internet-verfügbaren Ports zugewiesen, wie oben definiert. Bei N werden Prozessen, die den Standardwert verwenden, Ports aus der Gruppe der nur im Intranet verfügbaren Ports zugewiesen. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   System      CurrentControlSet         Services            Rpc               Linkage                  Bind</code></pre> | <strong>REG_MULTI_SZ</strong> | Listet die Gerätenamen aller NICs auf, an die standardmäßig gebunden werden soll (z. B. \Device\AMDPCN1). Wenn der Schlüssel nicht vorhanden ist, wird der Server an alle NICs gebunden. Wenn der Schlüssel vorhanden ist, wird der Server an die im Schlüssel angegebenen NICs gebunden, es sei denn, das Feld NICFlags ist auf RPC_C_BIND_TO_ALL_NICS. Wenn der Schlüssel über einen NULL-Wert ("") verfügt, wird die Konfiguration als ungültig <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong></strong></a> markiert, und <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong></strong></a> alle Aufrufe von <strong>RpcServerUseProtseq*</strong> über ncacn_ip_tcp oder ncadg_ip_udp fehlschlagen. | 




 

In der folgenden Tabelle wird veranschaulicht, wie sich die in der vorherigen Tabelle definierten Einstellungen auf drei Beispielanwendungen und auf die Einstellungen, die mit der [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) angewendet werden, ebenfalls beeinflusst werden.

In diesem Beispiel werden drei hypothetische Anwendungen berücksichtigt:

-   InternetApp: Diese Anwendung ist für die Internetverbindung vorgesehen und hat RPC C USE INTERNET PORT im EndpointFlags-Member der RPC POLICY-Struktur angegeben, die an die \_ \_ \_ \_ [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)  [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übergeben wird.
-   LocalApp: Diese Anwendung ist nicht für die Internetverbindung vorgesehen und hat RPC C USE INTRANET PORT im EndpointFlags-Member der RPC POLICY-Struktur angegeben, die an die \_ \_ \_ \_ [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)  [**RpcServerUseProtseqEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) übergeben wird.
-   DefaultApp: Diese Anwendung gibt null im **EndpointFlags-Member** der [**RPC \_ POLICY-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) an, die an die [**RpcServerUseProtseqEx-Funktion übergeben**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) wird.

In der folgenden Tabelle werden die Auswirkungen erläutert, die diese Einstellungen haben, basierend auf Werten, die in den in der vorherigen Tabelle erläuterten Registrierungseinträgen angegeben sind. Aus Gründen der Formatierung werden die folgenden Codes zugewiesen:

PIA = PortsInternetAvailable-Schlüsselwert

UIP = UseInternetPorts-Schlüsselwert

Der Wert des Ports-Schlüssels ist für dieses Beispiel 5000-5100 für jeden Eintrag.



| Application | PIA | UIP | Ergebnis                                  |
|-------------|-----|-----|-----------------------------------------|
| InternetApp | J   | J   | Verwendet Ports zwischen 5000 und 5100        |
| LocalApp    | J   | J   | Verwendet einen Port außerhalb des Bereichs von 5000 bis 5100. |
| DefaultApp  | J   | J   | Verwendet Ports zwischen 5000 und 5100        |
| InternetApp | J   | N   | Verwendet Ports zwischen 5000 und 5100        |
| LocalApp    | J   | N   | Verwendet einen Port außerhalb des Bereichs von 5000 bis 5100. |
| DefaultApp  | J   | N   | Verwendet einen Port außerhalb des Bereichs von 5000 bis 5100. |
| InternetApp | N   | J   | Verwendet einen Port außerhalb des Bereichs von 5000 bis 5100. |
| LocalApp    | N   | J   | Verwendet Ports zwischen 5000 und 5100        |
| DefaultApp  | N   | J   | Verwendet einen Port außerhalb des Bereichs von 5000 bis 5100. |
| InternetApp | N   | N   | Verwendet einen Port außerhalb des Bereichs von 5000 bis 5100. |
| LocalApp    | N   | N   | Verwendet Ports zwischen 5000 und 5100        |
| DefaultApp  | N   | N   | Verwendet Ports zwischen 5000 und 5100        |



 

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

 

 
