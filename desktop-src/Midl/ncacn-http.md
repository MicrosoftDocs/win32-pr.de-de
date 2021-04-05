---
title: ncacn_http-Attribut
description: Das http-Schlüsselwort ncacn \_ identifiziert den Microsoft Internet Information Server (IIS) als Protokollfamilie für den Endpunkt.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726337"
---
# <a name="ncacn_http-attribute"></a>ncacn \_ http-Attribut

Das **\_ http-Schlüsselwort ncacn** identifiziert den Microsoft Internet Information Server (IIS) als Protokollfamilie für den Endpunkt.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*RPC- \_ Server* 
</dt> <dd>

Die Internet Adresse oder der Name des Computers, auf dem der RPC-Server Prozess ausgeführt wird.

</dd> <dt>

*Dreher* 
</dt> <dd>

Der bekannte (statische) TCP/IP-Port, der vom RPC-Server Prozess überwacht wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Durch die Identifizierung von Microsoft Internet Information Server (IIS) als Protokollfamilie können Client-und Server Anwendungen über das Internet über den Microsoft Internet Information Server (IIS) als Proxy kommunizieren. Da Aufrufe über einen eingerichteten HTTP-Port getunniert werden, können Sie Firewalls überwinden.

Alle RPC-Client-und-Server Anwendungen können das **ncacn- \_ http** -Protokoll unterstützen, solange Sie mit einem Internet Informationsserver vernetzt sind. IIS kontaktiert den RPC-Server und richtet einen TCP/IP-Socket ein, der für den Client verwaltet wird. IIS verhandelt eine TCP/IP-Verbindung mit dem RPC-Server und fungiert nach Abschluss der Aushandlung als RPC-Proxy, um Daten zwischen dem Client seitigen TCP/IP-Socket und dem serverseitigen TCP/IP-Socket weiterzuleiten. Wenn der IIS-RPC-Proxy erkennt, dass eine Sitzung auf dem Client oder auf der Serverseite geschlossen wird, wird der verbleibende Socket geschlossen.

Die Client Anwendung verwendet implizit statische Bindungen an IIS, aber der Server kann dynamische Endpunkte verwenden, wobei der RPCSS-Server (Endpoint Mapper) des Servers den RPC-Serverport auflöst. Wenn IIS sich auf einem anderen Computer als der RPC-Server befindet, empfängt IIS den Remote Aufruf, kontaktiert RPCSS auf dem RPC-Server Computer, um den Server Prozess Endpunkt abzurufen, und leitet den Aufruf an den entsprechenden RPC-Server weiter.

Wenn Internet Explorer installiert ist, überprüft der Transport die Registrierung, um festzustellen, ob eine Konfiguration für einen HTTP-Proxy vorhanden ist. Wenn ein Proxy vorhanden ist, wird er vom Transport verwendet.

## <a name="examples"></a>Beispiele

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Dreher**](endpoint.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Zeichen folgen Bindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 