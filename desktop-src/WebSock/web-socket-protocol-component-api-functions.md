---
title: Funktionen der WebSocket-Protokoll Komponenten-API
description: Die WebSocket-Protokoll Komponenten-API definiert diese Funktionen.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d778fef6680112007b0f4a459787a51eb20bfe0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728784"
---
# <a name="websocket-protocol-component-api-functions"></a>Funktionen der WebSocket-Protokoll Komponenten-API

Die WebSocket-Protokoll Komponenten-API definiert diese Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                             | BESCHREIBUNG                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Websocketaborthandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | bricht ein WebSocket-Sitzungs Handle ab, das von [**websocketkreateclienthandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) oder [**websocketkreateserverhandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)erstellt wurde.<br/>   |
| [**Websocketbeginclienthandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | startet den Client seitigen Handshake.<br/>                                                                                                                                                                |
| [**Websocketbeginserverhandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | startet den serverseitigen Handshake.<br/>                                                                                                                                                                |
| [**Websocketcompleteaction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | schließt eine Aktion ab, die von [**websocketgetaction**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction)gestartet wurde.<br/>                                                                                                             |
| [**Websocketkreateclienthandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | erstellt ein Client seitiges WebSocket-Sitzungs handle.<br/>                                                                                                                                                  |
| [**Websocketkreateserverhandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | erstellt ein serverseitiges WebSocket-Sitzungs handle.<br/>                                                                                                                                                  |
| [**Websocketdeletehandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | Löscht ein WebSocket-Sitzungs handle, das von [**websocketkreateclienthandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) oder [**websocketkreateserverhandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)erstellt wurde.<br/>  |
| [**Websocketendclienthandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | schließt den Client seitigen Handshake ab.<br/>                                                                                                                                                             |
| [**Websocketendserverhandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | schließt den serverseitigen Handshake ab.<br/>                                                                                                                                                             |
| [**Websocketgetaction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | gibt eine Aktion aus einem [**websocketsend**](/windows/desktop/api/websocket/nf-websocket-websocketsend)-, [**websocketreceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) -oder [**websocketcompleteaction**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction)-Befehl zurück.<br/> |
| [**Websocketgetglobalproperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | Ruft eine einzelne WebSocket-Eigenschaft ab.<br/>                                                                                                                                                                |
| [**Websocketreceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | Fügt der Warteschlange für Protokoll Komponenten Vorgänge einen Empfangsvorgang hinzu.<br/>                                                                                                                              |
| [**Websocketsend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | Fügt der Warteschlange für Protokoll Komponenten Vorgänge einen Sendevorgang hinzu.<br/>                                                                                                                                 |



 

 

