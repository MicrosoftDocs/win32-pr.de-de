---
title: WebSocket-Protokollkomponenten-API
description: WebSocket-Protokollkomponenten-API
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a712234f55b0270db9da23dc0efa1da823c85907cca92ac3428cb1225fac8a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134213"
---
# <a name="websocket-protocol-component-api"></a>WebSocket-Protokollkomponenten-API

## <a name="purpose"></a>Zweck

Die WebSocket-Protokollkomponenten-API ermöglicht asynchrone, bidirektionale Kommunikationskanäle über HTTP, die über vorhandene Netzwerkhändler hinweg funktionieren. Mit der WebSocket-Protokollkomponenten-API verwendet ein Client HTTP für die Kommunikation mit einem Server, und dann wechseln beide Seiten zur Verwendung des zugrunde liegenden Protokolls, über das HTTP überlagert wurde (z. B. TCP oder SSL). Ziel ist es, zuerst HTTP zu verwenden, um Netzwerkhändler zu durchlaufen, und dann den eingerichteten zugrunde liegenden End-to-End-TCP/SSL-Kanal für die bidirektionale Anwendungskommunikation zu verwenden. Das WebSocket-Protokoll \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) wird in der IETF definiert, während eine zugeordnete \] JavaScript-API \[ [W3CAPI](https://dev.w3.org/html5/websockets/) im \] W3C definiert ist.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                          | Beschreibung                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**API-Datentypen der WebSocket-Protokollkomponente**](web-socket-protocol-component-api-data-types.md)<br/> | Die WebSocket-Protokollkomponenten-API definiert diese Datentypen.<br/>   |
| [WebSocket-Protokollkomponenten-API-Enumerationen](web-socket-protocol-component-api-enumerations.md)<br/> | Die WebSocket-Protokollkomponenten-API definiert diese Enumerationen.<br/> |
| [Api-Funktionen der WebSocket-Protokollkomponente](web-socket-protocol-component-api-functions.md)<br/>       | Die WebSocket-Protokollkomponenten-API definiert diese Funktionen.<br/>    |
| [API-Strukturen der WebSocket-Protokollkomponente](web-socket-protocol-component-api-structures.md)<br/>     | Die WebSocket-Protokollkomponenten-API definiert diese Strukturen.<br/>   |



 

## <a name="developer-audience"></a>Entwicklergruppe

Die WebSocket-Protokollkomponenten-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Sie müssen mit HTTP und Windows Netzwerk vertraut sein.

> [!Note]  
> Die bevorzugte Möglichkeit, das WebSocket-Protokoll auf Windows zu verwenden, ist die Windows [HTTP Services (WinHTTP)-API](/windows/desktop/WinHttp/winhttp-start-page) oder [die Windows. Networking.Sockets-Namespace](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die WebSocket-Protokollkomponenten-API erfordert Windows 8 und neuere Versionen des Windows Betriebssystems. Die APIs können dynamisch über die websocket.dll.

> [!Note]  
> websocket.dll unterstützt Client- und Serverhandshake-bezogene HTTP-Header, überprüft empfangene Handshakedaten und analysiert den WebSocket-Datenstrom. Er verarbeitet keine HTTP-spezifischen Vorgänge (Umleitung, Authentifizierung, Proxyunterstützung) und führt keine E/A-Vorgänge aus (Senden oder Empfangen von WebSocket-Streambytes).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

