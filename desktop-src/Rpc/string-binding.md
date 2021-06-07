---
title: Zeichenfolgenbindung
description: Die Zeichenfolgenbindung ist eine Zeichenfolge ohne Vorzeichen, die aus Zeichenfolgen besteht, die die Bindungsobjekt-UUID, die RPC-Protokollsequenz, die Netzwerkadresse sowie die Endpunkt- und Endpunktoptionen darstellen.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3f925c03c85be3c47ab174a85f31e72e40d828
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386979"
---
# <a name="string-binding"></a>Zeichenfolgenbindung

Die Zeichenfolgenbindung ist eine Zeichenfolge ohne Vorzeichen, die aus Zeichenfolgen besteht, die die Bindungsobjekt-UUID, die RPC-Protokollsequenz, die Netzwerkadresse sowie die Endpunkt- und Endpunktoptionen darstellen.

*ObjectUUID* @ *ProtocolSequence*:*NetworkAddress-Endpunkt* \[ ,*Option*\]

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

[UUID](/windows/desktop/Midl/uuid) des Objekts, das vom Remoteprozeduraufruf verwendet wird. Auf dem Server ordnet die RPC-Laufzeitbibliothek den Objekttyp einem Manager-Einstiegspunktvektor (einem Array von Funktionszektoren) zu, um die richtige Managerroutine aufrufen. Eine Erörterung der Zuordnung von Objekt-UUIDs zu Manager-Einstiegspunktvektoren finden Sie unter [Registrieren von Schnittstellen.](registering-interfaces.md)

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Zeichenfolge, die eine gültige Kombination aus einem RPC-Protokoll (z. B. ncacn), einem Transportprotokoll (z. B. TCP) und einem Netzwerkprotokoll (z. B. IP) darstellt. Microsoft RPC unterstützt die folgenden Protokolle, die unter [Protokollsequenzkonst constants angegeben sind.](protocol-sequence-constants.md)

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*Networkaddress*
</dt> <dd>

Netzwerkadresse des Systems zum Empfangen von Remoteprozeduraufrufen.

> [!Note]  
> Die folgenden Protokollsequenzen werden ab Windows XP nicht unterstützt:

 

-   [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)

Das Format und der Inhalt der Netzwerkadresse hängen wie folgt von der angegebenen Protokollsequenz ab.



| Protokollsequenz                       | Netzwerkadresse                                                                                                                                  | Beispiele                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Computername                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | Computername                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | Computername                                                                                                                                    | Myserver                                               |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Internetadresse mit vier Oktetten oder Hostname. Wenn der IPv6-Netzwerkstapel installiert ist, wird IPv6 vollständig unterstützt, und eine IPv6-Adresse wird ebenfalls akzeptiert. | 128.10.2.30 anynode.microsoft.com                      |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Servername (führende doppelte schräge Schrägstriche sind optional)                                                                                            | myserver \\ \\ myotherserver                             |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | IPX-Internetadresse oder Servername                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | Bereichs- und Knotensyntax                                                                                                                             | 4.120                                                  |
| [ncacn \_ bei \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Computername, optional gefolgt von @ und dem Namen der AppleTalk-Zone. Der Standardwert ist @ \* , die Zone des Clients, wenn keine Zone angegeben ist.                     | servername@zonename Servername                         |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Name des StreetTalk-Servers des Formulars item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Servername                                                                                                                                      | Myserver                                               |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Internetadresse (entweder Vier-Oktett- oder -Beschriftungsname oder name des lokalen Servers)                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Internetadresse mit vier Oktetten oder Hostname                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | IPX-Internetadresse oder Servername                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Computername                                                                                                                                     | thismachine                                            |



 

Das Feld netzwerkadresse ist optional. Wenn Sie keine Netzwerkadresse angeben, bezieht sich die Zeichenfolgenbindung auf Ihren lokalen Host. Es ist möglich, den Namen des lokalen Computers anzugeben, wenn Sie die **ncalrpc-Protokollsequenz** verwenden. Dies ist jedoch völlig unnötig.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Endpunkt*
</dt> <dd>

Endpunkt oder Adresse des Prozesses zum Empfangen von Remoteprozeduraufrufen. Einem Endpunkt kann das Schlüsselwort **endpoint= vorangehenden werden.** Die Angabe des Endpunkts ist optional, wenn der Server seine Bindungen bei der Endpunktzuordnung registriert hat. Weitere Informationen [**finden Sie unter RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

Das Format und der Inhalt eines Endpunkts hängen von der angegebenen Protokollsequenz ab, wie in der folgenden Endpunkt-/Optionstabelle gezeigt.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Option*
</dt> <dd>

Protokollspezifische Optionen. Das Optionsfeld ist nicht erforderlich. Jede Option wird durch ein {name, value}-Paar angegeben, das den Optionswert *der Syntaxoption* = *Name verwendet.* Optionen werden für jede Protokollsequenz definiert, wie in der folgenden Tabelle Endpunkt/Option gezeigt.



| Protokollsequenz                       | Endpunkt                                                                                           | Beispiele             | Optionsname                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Ganze Zahl zwischen 1 und 254. Viele Werte zwischen 0 und 32 sind von Microsoft reserviert.                 | 100                  | Keine                                                   |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | (wie oben beschrieben)                                                                                         | (wie oben beschrieben)           | Keine                                                   |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | (wie oben beschrieben)                                                                                         | (wie oben beschrieben)           | Keine                                                   |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Internetportnummer.                                                                              | 1025                 | Keine                                                   |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Named Pipe. Name muss mit \\ \\ "pipe" beginnen.                                                       | \\\\pipe \\ \\ pipename | Sicherheit                                               |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | Ganze Zahl zwischen 1 und 65535.                                                                       | 5.000                 | Keine                                                   |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | DECnet Phase IV-Objektnummer (muss dem Zeichen vorangestellt \# werden) oder Objektname.              | mailserver \# 17      | Keine                                                   |
| [ncacn \_ bei \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Eine Zeichenfolge mit einer Länge von bis zu 22 Byte.                                                           | myservicesendpoint   | Keine                                                   |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Vines-SPP-Portnummer zwischen 250 und 511.                                                         | 500                  | Keine                                                   |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Ganze Zahl zwischen 1 und 65535.                                                                       | 5.000                 | Keine                                                   |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Internetportnummer.                                                                              | 2215                 | HTTP- und RPC-Proxyservernamen, Option "HttpConnection" |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Internetportnummer.                                                                              | 1025                 | Keine                                                   |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | Ganze Zahl zwischen 1 und 65535.                                                                       | 5.000                 | Keine                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Zeichenfolge, die den Anwendungs- oder Dienstnamen angibt. Die Zeichenfolge darf keine umgekehrten Schrägstriche enthalten. | Mein \_ Drucker          | Sicherheit                                               |



 

Der Für die ncacn-HTTP-Protokollsequenz unterstützte **HttpConnectionOption-Optionsname** \_ verwendet den folgenden Wert.



| Optionsname       | Wert            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

**HttpConnectionOption** ermöglicht es Ihnen, rpc-Verhalten beim Herstellen von HTTP-Verbindungen zu leiten. Der **UseHttpProxy-Wert** weist RPC an, seinen Datenverkehr jederzeit über den HTTP-Proxy weiterzuleiten. Dies gilt auch, wenn für den Client die Internetoptionen in Internet Explorer proxy server for local addresses (Proxyserver für lokale Adressen umgehen) festgelegt sind.  Diese Option weist den Client an, eine verbindung mit dem RPC-Proxy über den HTTP-Proxy zu erzwingen. Dadurch wird die Zeit zum Herstellen einer Verbindung beschleunigt, da jede Verzögerung bei der Suche nach dem RPC-Server direkt vor der Verwendung des HTTP-Proxys umgangen wird.

Wenn diese **HttpConnectionOption-Option** verwendet wird und Internet Explorer auf dem Client nicht für die Verwendung dieses HTTP-Proxys konfiguriert ist, können Verbindungen mit **RPC S INVALID NETWORK \_ \_ \_ \_ OPTIONS** fehlschlagen.

``` syntax
HttpConnectOption=UseHttpProxy
```

Weitere Informationen zur **HttpConnectionOption** finden Sie unter [Verwenden von HTTP als RPC-Transport.](using-http-as-an-rpc-transport.md)

Der Name der **Sicherheitsoption,** der für die Protokollsequenzen ncalrpc, ncacn \_ np, ncadg \_ ip \_ udp und ncadg ipx unterstützt \_ wird, verwendet die folgenden Optionswerte.



| Optionsname  | Optionswert                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Sicherheit** | {Identification \| Anonymous \| impersonation} {dynamic \| static} {**true** \| **false**} |



 

Wenn der Name der Sicherheitsoption angegeben wird, muss auch ein Eintrag aus jedem der Sicherheitsoptionswerte angegeben werden. Die Optionswerte müssen durch ein einzelnes Leerzeichen getrennt werden. Beispielsweise sind die folgenden *Optionsfelder* gültig:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

Die Werte der Sicherheitsoption haben die folgende Bedeutung.



| Wert der Sicherheitsoption | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anonym             | Der Client ist gegenüber dem Server anonym.                                                                                                                                                                                                                                                                                                                   |
| Dynamisch               | Änderungen an der Clientsicherheitsidentität werden vom Server erkannt, wenn der Server Transportsicherheit verwendet. Dies ist der Standardmodus für die Sicherheit auf LRPC-Transportebene (ncalrpc) und für die Sicherheit auf lokaler Named Pipe-Transportebene (ncacn \_ np).                                                                                                             |
| **False**             | Effective = **FALSE**; Alle Tokenberechtigungseinstellungen, einschließlich der auf OFF festgelegten Einstellungen, sind im Token auf dem Server enthalten und können vom Server aktiviert werden. Berechtigungen sind nur für RPC-Aufrufe desselben Computers relevant.                                                                                                                                     |
| **Identifikation**    | Der Server verfügt über Informationen zum Client, kann aber keine Identität annehmen.                                                                                                                                                                                                                                                                                      |
| **Identitätswechsel**     | Der Server kann im Namen des Clients innerhalb des lokalen Systems agieren (die Sicherheit auf Transportebene unterstützt keine Delegierung).                                                                                                                                                                                                                               |
| **Statisch**            | Änderungen an der Clientsicherheitsidentität werden vom Server nicht erkannt, wenn der Server Transportsicherheit verwendet. Dies ist der einzige Modus, der für die Sicherheit auf Remote-Named Pipe -Transportebene (ncacn np) verfügbar \_ ist. Die Identität des Aufrufers wird während des ersten Remoteprozeduraufrufs für dieses Bindungshandle gespeichert, nicht zum Zeitpunkt der Erstellung des Bindungshandle. |
| **True**              | Effective = **TRUE**; Im Token auf dem Server sind nur einstellungen für Tokenberechtigungen enthalten, die auf ON festgelegt sind. Berechtigungen, die auf OFF festgelegt sind, können vom Server nicht aktiviert werden, wenn diese Option verwendet wird. Berechtigungen sind nur für RPC-Aufrufe desselben Computers relevant.                                                                                                         |



 

Weitere Informationen zu Sicherheitsoptionen, [Sicherheit](security.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Leerzeichen sind in Zeichenfolgenbindungen nur zulässig, wenn *dies* für die Optionssyntax erforderlich ist. Die Standardeinstellungen für die Felder *NetworkAddress,* *Endpoint* und *Option* variieren je nach Wert des *ProtocolSequence-Members.*

Für alle Zeichenfolgenbindungsfelder wird ein einzelner umgekehrter Schrägstrich \\ () als Escapezeichen interpretiert. Um einen einzelnen literalen umgekehrten Schrägstrich anzugeben, müssen Sie zwei umgekehrte Schrägstriche \\ \\ () angeben.

Eine Zeichenfolgenbindung enthält die Zeichendarstellung eines Bindungshandle und gelegentlich Teile eines Bindungshandle. Zeichenfolgenbindungen eignen sich für die Darstellung von Teilen eines Bindungshandle, können jedoch nicht zum Durchführen von Remoteprozeduraufrufen verwendet werden. Sie müssen zuerst in ein Bindungshandle konvertiert werden, indem [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)aufgerufen wird.

Darüber hinaus enthält eine Zeichenfolgenbindung nicht alle Informationen aus einem Bindungshandle. Die Authentifizierungsinformationen, die einem Bindungshandle zugeordnet sind, werden beispielsweise nicht in die Zeichenfolgenbindung übersetzt, die durch Aufrufen von [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)zurückgegeben wird.

Während der Entwicklung einer verteilten Anwendung können Server ihre Bindungsinformationen mithilfe von Zeichenfolgenbindungen an Clients übermitteln, um eine Client-Server-Beziehung herzustellen, ohne die Datenbank endpoint-map oder name-service zu verwenden. Verwenden Sie zum Einrichten einer solchen Beziehung die [**Funktion RpcBindingToStringBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) um einen oder mehrere Bindungshandles aus einem Bindungshandlesvektor in eine Zeichenfolgenbindung zu konvertieren und die Zeichenfolgenbindung für den Client zur Verfügung zu stellen.

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie Beispiele für gültige Zeichenfolgenbindungen. In diesen Beispielen wird *obj-uuid* zur Vereinfachung verwendet, um eine gültige UUID in Zeichenfolgenform zu darstellen. Anstelle der UUID 308FB580-1EB2-11CA-923B-08002B1075A7 zeigen die Beispiele *obj-uuid*.

``` syntax
obj-uuid@ncadg_mq:mymqserver
obj-uuid@ncacn_http:major7.microsoft.com[2225]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80,HttpConnectOption=UseHttpProxy]
obj-uuid@ncacn_ip_tcp:16.20.16.27[2001]
obj-uuid@ncacn_ip_tcp:16.20.16.27[endpoint=2001]
obj-uuid@ncacn_nb_nb:
obj-uuid@ncacn_nb_nb:[100]
obj-uuid@ncacn_np:
obj-uuid@ncacn_np:[\\pipe\\p3,Security=impersonation static true]
obj-uuid@ncacn_np:\\\\marketing[\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\marketing[endpoint=\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\sales
obj-uuid@ncacn_np:\\\\sales[\\pipe\\p1,Security=identification dynamic true]
obj-uuid@ncalrpc:
obj-uuid@ncalrpc:[object1_name_demonstrating_that_these_can_be_lengthy]
obj-uuid@ncalrpc:[object2_name,Security=anonymous static true]
obj-uuid@ncacn_vns_spp:server@group@org[500]
obj-uuid@ncacn_dnet_nsp:took[elf_server]
obj-uuid@ncacn_dnet_nsp:took[endpoint=elf_server]
obj-uuid@ncadg_ip_udp:128.10.2.30
obj-uuid@ncadg_ip_udp:maryos.microsoft.com[1025]
obj-uuid@ncadg_ipx: ~0000000108002B30612C[5000]
obj-uuid@ncadg_ipx:printserver
obj-uuid@ncacn_spx:annaw[4390]
obj-uuid@ncacn_spx:~0000000108002B30612C
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[Verwenden von HTTP als RPC-Transport](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

