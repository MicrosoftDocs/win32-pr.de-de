---
title: Api-Funktionen der WebSocket-Protokollkomponente
description: Die WebSocket-Protokollkomponenten-API definiert diese Funktionen.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d88a4ef8eb9caa0e409d0ded60b6dffd2717dc74d1b2cdddeb08ee6d9de08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330338"
---
# <a name="websocket-protocol-component-api-functions"></a>Api-Funktionen der WebSocket-Protokollkomponente

Die WebSocket-Protokollkomponenten-API definiert diese Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                             | Beschreibung                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WebSocketAbortHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | bricht ein WebSocket-Sitzungshandle ab, das von [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) oder [**WebSocketCreateServerHandle erstellt wurde.**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)<br/>   |
| [**WebSocketBeginClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | startet den clientseitigen Handshake.<br/>                                                                                                                                                                |
| [**WebSocketBeginServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | startet den serverseitigen Handshake.<br/>                                                                                                                                                                |
| [**WebSocketCompleteAction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | schließt eine Aktion ab, die von [**WebSocketGetAction gestartet wurde.**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction)<br/>                                                                                                             |
| [**WebSocketCreateClientHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | erstellt ein clientseitiges WebSocket-Sitzungshand handle.<br/>                                                                                                                                                  |
| [**WebSocketCreateServerHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | erstellt ein serverseitiges WebSocket-Sitzungshand handle.<br/>                                                                                                                                                  |
| [**WebSocketDeleteHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | löscht ein WebSocket-Sitzungshandle, das von [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) oder [**WebSocketCreateServerHandle erstellt wurde.**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)<br/>  |
| [**WebSocketEndClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | schließt den clientseitigen Handshake ab.<br/>                                                                                                                                                             |
| [**WebSocketEndServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | schließt den serverseitigen Handshake ab.<br/>                                                                                                                                                             |
| [**WebSocketGetAction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | gibt eine Aktion aus einem Aufruf von [**WebSocketSend,**](/windows/desktop/api/websocket/nf-websocket-websocketsend) [**WebSocketReceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) oder [**WebSocketCompleteAction zurück.**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction)<br/> |
| [**WebSocketGetGlobalProperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | ruft eine einzelne WebSocket-Eigenschaft ab.<br/>                                                                                                                                                                |
| [**WebSocketReceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | fügt der Vorgangswarteschlange der Protokollkomponente einen Empfangsvorgang hinzu.<br/>                                                                                                                              |
| [**WebSocketSend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | fügt der Vorgangswarteschlange der Protokollkomponente einen Sendevorgang hinzu.<br/>                                                                                                                                 |



 

 

