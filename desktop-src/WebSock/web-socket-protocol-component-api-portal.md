---
title: WebSocket-Protokoll Komponenten-API
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101962"
---
# <a name="websocket-protocol-component-api"></a>WebSocket-Protokoll Komponenten-API

## <a name="purpose"></a>Zweck

Die WebSocket-Protokoll Komponenten-API ermöglicht asynchrone bidirektionale Kommunikationskanäle über HTTP, die über vorhandene Netzwerk Vermittler hinweg funktionieren. Mit der WebSocket-Protokoll Komponenten-API verwendet ein Client HTTP für die Kommunikation mit einem Server. dann wechseln beide Seiten zur Verwendung des zugrunde liegenden Protokolls, für das http überlagert wurde (z. b. TCP oder SSL). Ziel ist es, zuerst http zum Durchlaufen von Netzwerk Vermittlern zu verwenden und dann den eingerichteten End-to-End-TCP/SSL-Kanal für die bidirektionale Anwendungs Kommunikation zu verwenden. Das WebSocket-Protokoll \[ [wsproto](https://tools.ietf.org/html/rfc6455) \] wird im IETF definiert, während ein zugeordnetes JavaScript-API- \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] im W3C definiert wird.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                          | BESCHREIBUNG                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Datentypen der WebSocket-Protokoll Komponenten-API**](web-socket-protocol-component-api-data-types.md)<br/> | Die WebSocket-Protokoll Komponenten-API definiert diese Datentypen.<br/>   |
| [API-Enumerationen der WebSocket-Protokoll Komponente](web-socket-protocol-component-api-enumerations.md)<br/> | Die WebSocket-Protokoll Komponenten-API definiert diese Enumerationen.<br/> |
| [Funktionen der WebSocket-Protokoll Komponenten-API](web-socket-protocol-component-api-functions.md)<br/>       | Die WebSocket-Protokoll Komponenten-API definiert diese Funktionen.<br/>    |
| [API-Strukturen der WebSocket-Protokoll Komponente](web-socket-protocol-component-api-structures.md)<br/>     | Diese Strukturen werden von der WebSocket-Protokoll Komponenten-API definiert.<br/>   |



 

## <a name="developer-audience"></a>Entwicklergruppe

Die WebSocket-Protokoll Komponenten-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Vertrautheit mit http-und Windows-Netzwerken ist erforderlich.

> [!Note]  
> Der bevorzugte Weg, das WebSocket-Protokoll unter Windows zu verwenden, ist die [Windows HTTP-Dienste (WinHTTP)-API](/windows/desktop/WinHttp/winhttp-start-page) oder der [Windows. Networking. Sockets-Namespace](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die WebSocket-Protokoll Komponenten-API erfordert Windows 8 und höhere Versionen des Windows-Betriebssystems. Die APIs können dynamisch über websocket.dll verknüpft werden.

> [!Note]  
> websocket.dll bietet Unterstützung für Client-und Server Handshake-bezogene HTTP-Header, überprüft empfangene Handshake-Daten und analysiert den WebSocket-Datenstrom. Er verarbeitet keine HTTP-spezifischen Vorgänge (Umleitung, Authentifizierung, Proxy Unterstützung) und führt keine e/a-Vorgänge aus (senden oder empfangen von WebSocket-Datenstrom Bytes).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

