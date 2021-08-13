---
title: ncacn_http-Attribut
description: Das schlüsselwort ncacn \_ http identifiziert den Microsoft Internet Information Server (IIS) als Protokollfamilie für den Endpunkt.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http-Attribut MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7eed41849f59e497000e9ad56ae7c3166cf2d0212986fa9ba5f5ea910ed364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642211"
---
# <a name="ncacn_http-attribute"></a>\_ncacn-HTTP-Attribut

Das **schlüsselwort ncacn \_ http** identifiziert den Microsoft Internet Information Server (IIS) als Protokollfamilie für den Endpunkt.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_RPC-Server* 
</dt> <dd>

Die Internetadresse oder der Name des Computers, auf dem der RPC-Serverprozess ausgeführt wird.

</dd> <dt>

*endpoint* 
</dt> <dd>

Der bekannte (statische) TCP/IP-Port, an dem der RPC-Serverprozess lauscht.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Durch die Identifizierung von Microsoft Internet Information Server (IIS) als Protokollfamilie können Client- und Serveranwendungen über das Internet kommunizieren, indem Microsoft Internet Information Server (IIS) als Proxy verwendet wird. Da Aufrufe über einen eingerichteten HTTP-Port getunnelt werden, können sie firewallübergreifend erfolgen.

Alle RPC-Client- und -Serveranwendungen können das **ncacn-HTTP-Protokoll \_** unterstützen, solange sie mit einem Internetinformationsserver verbunden sind. Der IIS kontaktiert den RPC-Server und richtet einen TCP/IP-Socket ein, den er für den Client verwaltet. Der IIS handelt eine TCP/IP-Verbindung mit dem RPC-Server aus und fungiert nach Abschluss der Aushandlung als RPC-Proxy, der Daten zwischen dem clientseitigen TCP/IP-Socket und dem serverseitigen TCP/IP-Socket weiterleitet. Wenn der IIS-RPC-Proxy erkennt, dass eine Sitzung auf client- oder serverseitiger Seite geschlossen wird, wird der verbleibende Socket geschlossen.

Die Clientanwendung verwendet implizit eine statische Bindung an den IIS, aber der Server kann dynamische Endpunkte verwenden, wobei der RPCSS (Endpoint Mapper) des Servers den RPC-Serverport auflöst. Wenn sich der IIS auf einem anderen Computer als der RPC-Server befindet, empfängt der IIS den Remoteaufruf, kontaktiert RPCSS auf dem RPC-Servercomputer, um den Serverprozessendpunkt abzurufen, und leitet den Aufruf dann an den entsprechenden RPC-Server weiter.

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

[**Endpunkt**](endpoint.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Zeichenfolgenbindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 