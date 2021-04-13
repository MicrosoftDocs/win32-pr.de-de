---
title: Zeichen folgen Bindung
description: Die Zeichen folgen Bindung ist eine Zeichenfolge ohne Vorzeichen, die aus Zeichen folgen besteht, die das Bindungs Objekt UUID, die RPC-Protokoll Sequenz, die Netzwerkadresse und die Endpunkt-und Endpunkt Optionen darstellen.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d804fe614185b054b8041e13069e900501342a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390799"
---
# <a name="string-binding"></a>Zeichen folgen Bindung

Die Zeichen folgen Bindung ist eine Zeichenfolge ohne Vorzeichen, die aus Zeichen folgen besteht, die das Bindungs Objekt UUID, die RPC-Protokoll Sequenz, die Netzwerkadresse und die Endpunkt-und Endpunkt Optionen darstellen.

*Objectuuid* @ *Protocolsequence*:*networkaddress*- \[ *Endpunkt*,*Option*\]

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*Objectuuid*
</dt> <dd>

[UUID](/windows/desktop/Midl/uuid) des Objekts, das vom Remote Prozedur aufrufsvorgang verarbeitet wird. Auf dem Server ordnet die RPC-Lauf Zeit Bibliothek den Objekttyp einem Manager-Einstiegspunkt Vektor (ein Array von Funktions Zeigern) zu, um die korrekte Manager-Routine aufzurufen. Eine Erläuterung zum Zuordnen von Objekt-UUIDs zu Manager-Einstiegspunkt Vektoren finden Sie unter [Registrieren von Schnittstellen](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*Protocolsequence*
</dt> <dd>

Zeichenfolge, die eine gültige Kombination eines RPC-Protokolls (z. b. ncacn), eines Transport Protokolls (z. b. TCP) und eines Netzwerk Protokolls (z. b. IP) darstellt. Microsoft RPC unterstützt die folgenden Protokolle, die in den [Protokoll Sequenz Konstanten](protocol-sequence-constants.md)angegeben sind.

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*
</dt> <dd>

Netzwerkadresse des Systems, um Remote Prozedur Aufrufe zu empfangen.

> [!Note]  
> Die folgenden Protokoll Sequenzen werden ab Windows XP nicht unterstützt:

 

-   [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ VNS- \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)

Das Format und der Inhalt der Netzwerkadresse sind wie folgt von der angegebenen Protokoll Sequenz abhängig.



| Protokoll Sequenz                       | Netzwerkadresse                                                                                                                                  | Beispiele                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Computername                                                                                                                                    | MyServer                                               |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | Computername                                                                                                                                    | MyServer                                               |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | Computername                                                                                                                                    | MyServer                                               |
| [ncacn \_ IP \_ TCP](/windows/desktop/Midl/ncacn-ip-tcp)     | Vier Oktett-Internet Adresse oder Hostname. Wenn der IPv6-Netzwerk Stapel installiert ist, wird IPv6 vollständig unterstützt, und eine IPv6-Adresse wird ebenfalls akzeptiert. | 128.10.2.30 anynode.Microsoft.com                      |
| [ncacn \_ NP](/windows/desktop/Midl/ncacn-np)              | Server Name (führende doppelte umgekehrte Schrägstriche sind optional)                                                                                            | MyServer \\ \\ myotherserver                             |
| [ncacn- \_ SPX](/windows/desktop/Midl/ncacn-spx)            | IPX-Internet Adresse oder Servername                                                                                                             | ~ 0000000108002b30612c MyServer                         |
| [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | Bereichs-und Knoten Syntax                                                                                                                             | 4,120                                                  |
| [ncacn \_ bei \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Computer Name, optional gefolgt von @ und dem Namen der AppleTalk-Zone. Der Standardwert \* ist @, der Client Zone, wenn keine Zone bereitgestellt wird.                     | servername@zonename Servername                         |
| [ncacn \_ VNS- \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | StreetTalk-Servername der Form item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Servername                                                                                                                                      | MyServer                                               |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Internet Adresse (entweder vier Oktett oder Anzeige Name oder Name des lokalen Servers)                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [ncadg \_ -IP- \_ UDP](/windows/desktop/Midl/ncadg-ip-udp)     | Vier Oktett-Internet Adresse oder Hostname                                                                                                        | 128.10.2.30 anynode.Microsoft.com                      |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | IPX-Internet Adresse oder Servername                                                                                                             | ~ 0000000108002b30612c MyServer                         |
| [Ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Computername                                                                                                                                     | thismachine                                            |



 

Das Feld für die Netzwerkadresse ist optional. Wenn Sie keine Netzwerkadresse angeben, verweist die Zeichen folgen Bindung auf den lokalen Host. Es ist möglich, den Namen des lokalen Computers anzugeben, wenn Sie die **Ncalrpc** -Protokoll Sequenz verwenden. Dies ist jedoch völlig unnötig.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Dreher*
</dt> <dd>

Der Endpunkt oder die Adresse des Prozesses, der Remote Prozedur Aufrufe empfangen soll. Einem Endpunkt kann das Schlüsselwort **EndPoint =** vorangestellt werden. Das Angeben des Endpunkts ist optional, wenn der Server seine Bindungen mit der Endpunkt Zuordnung registriert hat. Weitere Informationen finden Sie unter [**rpcepregiester**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

Das Format und der Inhalt eines Endpunkts sind von der angegebenen Protokoll Sequenz abhängig, wie in der folgenden Endpunkt-/Option-Tabelle gezeigt.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Andere*
</dt> <dd>

Protokoll spezifische Optionen. Das Optionsfeld ist nicht erforderlich. Jede Option wird durch ein {Name, Value}-Paar angegeben, das den  = *Optionswert* der Syntax Option Name verwendet. Optionen werden für jede Protokoll Sequenz definiert, wie in der folgenden Endpunkt-/Options-Tabelle gezeigt.



| Protokoll Sequenz                       | Endpunkt                                                                                           | Beispiele             | Optionsname                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Ganzzahl zwischen 1 und 254. Viele Werte zwischen 0 und 32 sind von Microsoft reserviert.                 | 100                  | Keine                                                   |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | (wie oben)                                                                                         | (wie oben)           | Keine                                                   |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | (wie oben)                                                                                         | (wie oben)           | Keine                                                   |
| [ncacn \_ IP \_ TCP](/windows/desktop/Midl/ncacn-ip-tcp)     | Internet Portnummer.                                                                              | 1025                 | Keine                                                   |
| [ncacn \_ NP](/windows/desktop/Midl/ncacn-np)              | Named Pipe. Der Name muss mit " \\ \\ Pipe" beginnen.                                                       | \\\\\\ \\ Pipename der Pipe | Sicherheit                                               |
| [ncacn- \_ SPX](/windows/desktop/Midl/ncacn-spx)            | Ganzzahl zwischen 1 und 65535.                                                                       | 5.000                 | Keine                                                   |
| [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | Der DECnet-Phase IV-Objekt Nummer (muss das \# Zeichen vorangestellt sein) oder Objektname.              | Mailserver \# 17      | Keine                                                   |
| [ncacn \_ bei \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Eine Zeichenfolge mit einer Länge von bis zu 22 bytes.                                                           | myservicesendpoint   | Keine                                                   |
| [ncacn \_ VNS- \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | SPP-Portnummer der Reben zwischen 250 und 511.                                                         | 500                  | Keine                                                   |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Ganzzahl zwischen 1 und 65535.                                                                       | 5.000                 | Keine                                                   |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Internet Portnummer.                                                                              | 2215                 | HTTP-und RPC-Proxy Servernamen, httpconnection-Option |
| [ncadg \_ -IP- \_ UDP](/windows/desktop/Midl/ncadg-ip-udp)     | Internet Portnummer.                                                                              | 1025                 | Keine                                                   |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | Ganzzahl zwischen 1 und 65535.                                                                       | 5.000                 | Keine                                                   |
| [Ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Zeichenfolge, die den Anwendungs-oder Dienstnamen angibt. Die Zeichenfolge darf keine umgekehrten Schrägstriche enthalten. | mein \_ Drucker          | Sicherheit                                               |



 

Der **httpconnectionoption** -Options Name, der für die ncacn http-Protokoll Sequenz unterstützt wird \_ , hat den folgenden Wert.



| Optionsname       | Wert            |
|-------------------|------------------|
| Httpconnectoption | **Usehttpproxy** |



 

Mit der **httpconnectionoption** können Sie das RPC-e-Verhalten beim Herstellen von http-Verbindungen weiterleiten. Der **usehttpproxy** -Wert weist RPC an, den Datenverkehr jederzeit über den HTTP-Proxy weiterzuleiten. Dies umfasst auch, wenn der Client die Internetoptionen in Internet Explorer festgelegt hat, um den Proxy Server bei lokalen Adressen zu umgehen.  Mit dieser Option wird der Client angewiesen, eine zwangsweise über den HTTP-Proxy eine Verbindung zum RPC-Proxy herzustellen. Dies beschleunigt die Zeit, um eine Verbindung herzustellen, da die Verzögerung bei der Suche nach dem RPC-Server unmittelbar vor der Verwendung des HTTP-Proxys umgangen wird.

Wenn diese **httpconnectionoption** -Option verwendet wird und Internet Explorer auf dem Client nicht für die Verwendung dieses HTTP-Proxys konfiguriert ist, können Verbindungen mit **\_ ungültigen RPC S- \_ \_ Netzwerk \_ Optionen** fehlschlagen.

``` syntax
HttpConnectOption=UseHttpProxy
```

Weitere Informationen zu **httpconnectionoption** finden [Sie unter Verwenden von http als RPC-Transport](using-http-as-an-rpc-transport.md).

Der Name der **Sicherheits** Option, der für die Protokoll Sequenzen Ncalrpc, ncacn \_ NP, ncadg \_ IP \_ UDP und ncadg IPX unterstützt wird \_ , übernimmt die folgenden Optionswerte.



| Optionsname  | Optionswert                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Security** | {Identifizierungs- \| Anonymer Identitätswechsel \| } {Dynamic \| static} {**true** \| **false**} |



 

Wenn der Name der Sicherheitsoption angegeben ist, muss auch ein Eintrag aus den einzelnen Gruppen von Sicherheits Options Werten angegeben werden. Die Optionswerte müssen durch ein einzelnes Leerzeichen voneinander getrennt werden. Die folgenden *options* Felder sind z. b. gültig:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

Die Werte der Sicherheitsoptionen haben folgende Bedeutungen.



| Wert der Sicherheitsoption | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anonym             | Der Client ist gegenüber dem Server anonym.                                                                                                                                                                                                                                                                                                                   |
| Dynamisch               | Änderungen an der Client Sicherheitsidentität werden vom Server erkannt, wenn der Server die Transportsicherheit verwendet. Dies ist der Standardmodus für die Sicherheit von LRPC (Ncalrpc) auf Transport Ebene und für die Sicherheit lokaler Named Pipe (ncacn \_ NP) auf Transport Ebene.                                                                                                             |
| **False**             | Effektiv = **false**; Alle tokenberechtigungs-Einstellungen, einschließlich derjenigen, die auf OFF festgelegt sind, sind im Token auf dem Server enthalten und können vom Server aktiviert werden. Berechtigungen sind nur für RPC-Aufrufe desselben Computers relevant.                                                                                                                                     |
| **Identifikation**    | Der Server enthält Informationen zum Client, kann aber keinen Identitätswechsel durchgeführt werden.                                                                                                                                                                                                                                                                                      |
| **Identitätswechsel**     | Der Server kann im Namen des Clients innerhalb des lokalen Systems agieren (die Sicherheit auf Transport Ebene unterstützt keine Delegierung).                                                                                                                                                                                                                               |
| **Statisch**            | Änderungen an der Client Sicherheitsidentität werden vom Server nicht erkannt, wenn der Server die Transportsicherheit verwendet. Dies ist der einzige Modus, der für die Sicherheit von Remote Named Pipe (ncacn \_ NP) auf Transport Ebene verfügbar ist. Die Identität des Aufrufers wird während des ersten Remote Prozedur Aufrufes für dieses Bindungs handle gespeichert, nicht zum Zeitpunkt, an dem das Bindungs Handle erstellt wird. |
| **True**              | Effektiv = **true**; nur Einstellungen für tokenprivilegien, die auf ON festgelegt sind, sind im Token auf dem Server enthalten. Berechtigungen, die auf OFF festgelegt sind, können vom Server nicht aktiviert werden, wenn diese Option verwendet wird. Berechtigungen sind nur für RPC-Aufrufe desselben Computers relevant.                                                                                                         |



 

Weitere Informationen zu Sicherheitsoptionen finden Sie unter [Sicherheit](security.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Leerraum ist in Zeichen folgen Bindungen nicht zulässig, es sei denn, dies ist für die *options* Syntax erforderlich. Die Standardeinstellungen für die Felder " *networkaddress*", " *EndPoint*" und " *Option* " variieren je nach Wert des *protocolsequence* -Members.

Für alle Zeichen folgen Bindungs Felder wird ein einzelner umgekehrter Schrägstrich ( \) als Escapezeichen interpretiert. Zum Angeben eines einzelnen literalen umgekehrten Schrägstrichs müssen Sie zwei umgekehrte Schrägstriche angeben ( \\ \) .

Eine Zeichen folgen Bindung enthält die Zeichen Darstellung eines Bindungs Handles und gelegentlich Teile eines Bindungs Handles. Zeichen folgen Bindungen sind praktisch für die Darstellung von Teilen eines Bindungs Handles, Sie können jedoch nicht zum Ausführen von Remote Prozedur aufrufen verwendet werden. Sie müssen zuerst durch Aufrufen von [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)in ein Bindungs handle konvertiert werden.

Darüber hinaus enthält eine Zeichen folgen Bindung nicht alle Informationen von einem Bindungs handle. Beispielsweise werden die einem Bindungs handle zugeordneten Authentifizierungsinformationen nicht in die durch Aufrufen von [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)zurückgegebene Zeichen folgen Bindung übersetzt.

Während der Entwicklung einer verteilten Anwendung können Server Ihre Bindungs Informationen mithilfe von Zeichen folgen Bindungen an Clients übermitteln, um eine Client/Server-Beziehung herzustellen, ohne die Datenbank der Endpunkt Zuordnung oder die Name-Service-Datenbank zu verwenden. Um eine solche Beziehung herzustellen, verwenden Sie die [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) -Funktion, um ein oder mehrere Bindungs Handles von einem Bindungs handle-Vektor in eine Zeichen folgen Bindung zu konvertieren und die Zeichen folgen Bindung an den Client bereitzustellen.

## <a name="examples"></a>Beispiele

Im folgenden finden Sie Beispiele für gültige Zeichen folgen Bindungen. In diesen Beispielen wird *obj-UUID* zur einfacheren Darstellung einer gültigen uuid in Form einer Zeichenfolge verwendet. Anstatt die UUID 308sb580-1eb2-11 ca-923b-08002b1075a7 anzuzeigen, zeigen die Beispiele *obj-UUID* an.

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

[**Rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**Rpcepregiester**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[Verwenden von http als RPC-Transport](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

