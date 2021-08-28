---
title: Virtual Channel-Client-DLL
description: Der Client einer Anwendung für virtuelle Kanäle ist eine DLL, die während der Remotedesktopdienste auf dem Clientcomputer geladen wird. Die DLL muss auf dem Clientcomputer registriert sein.
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f9ba01db57de6dc030e6c47b09c4173156ef8f85e3969716ae6e10dfc069f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423580"
---
# <a name="virtual-channel-client-dll"></a>Virtual Channel-Client-DLL

Der Client einer Anwendung für virtuelle Kanäle ist eine DLL, die während der Remotedesktopdienste auf dem Clientcomputer geladen wird. Die DLL muss auf dem Clientcomputer registriert sein. Weitere Informationen finden Sie unter [Virtual Channel Client Registration](virtual-channel-client-registration.md).

Die Client-DLL muss eine [**VirtualChannelEntry-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) exportieren, die Remotedesktopdienste Initialisierung aufruft. Der **VirtualChannelEntry-Einstiegspunkt** empfängt einen Zeiger auf eine [**CHANNEL ENTRY \_ \_ POINTS-Struktur.**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points) Diese Struktur enthält Zeiger auf die Funktionen, die die Client-DLL aufruft, um auf virtuelle Kanäle zu zugreifen.



| Funktion                                                      | Beschreibung                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | Registriert die Namen der virtuellen Kanäle, die vom Client verwendet werden sollen, und stellt eine [**VirtualChannelInitEvent-Rückruffunktion**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) zur Verfügung, über die Remotedesktopdienste den Client über Ereignisse benachrichtigt, die sich auf die Clientverbindung auswirken.<br/> |
| [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | Öffnet das Clientende eines angegebenen virtuellen Kanals und stellt eine [**VirtualChannelOpenEvent-Rückruffunktion**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) zur Verfügung, über die Remotedesktopdienste den Client über Ereignisse benachrichtigt, die sich auf den virtuellen Kanal auswirken.<br/>                    |
| [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | Schreibt Daten in einen virtuellen Kanal. Remotedesktopdienste sendet diese Daten an das Serverende des virtuellen Kanals. Das Serverende ruft die [**WTSVirtualChannelRead-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) auf, um die Daten zu lesen.<br/>                                             |
| [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | Schließt einen virtuellen Kanal.<br/>                                                                                                                                                                                                                                                  |



 

Die [**VirtualChannelEntry-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) Ihrer DLL muss die [**VirtualChannelInit-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) aufrufen, um den Zugriff auf virtuelle Kanäle zu initialisieren. Wenn Sie **VirtualChannelInit aufrufen,** müssen Sie einen Zeiger auf die [**VirtualChannelInitEvent-Rückruffunktion**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) übergeben. Remotedesktopdienste ruft diese Rückruffunktion auf, wenn die Initialisierung abgeschlossen ist, und erneut, wenn eine Verbindung mit einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) hergestellt wurde.

Nachdem die Verbindung hergestellt wurde, können Sie die [**VirtualChannelOpen-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) aufrufen, um die durch den [**VirtualChannelInit-Aufruf**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) registrierten virtuellen Kanäle zu öffnen. Der **VirtualChannelOpen-Aufruf** gibt einen Zeiger auf Ihre [**VirtualChannelOpenEvent-Rückruffunktion**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) an.

Nachdem der [**VirtualChannelOpen-Aufruf**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) zurückgegeben wurde, können Sie die [**VirtualChannelWrite-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) aufrufen, um in den virtuellen Kanal zu schreiben. Der Schreibvorgang ist asynchron. Daher dürfen Sie den an **VirtualChannelWrite** übergebenen Puffer erst wiederverwenden, wenn Remotedesktopdienste Ihre [**VirtualChannelOpenEvent-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) aufruft, um anzugeben, dass der Schreibvorgang abgeschlossen wurde. Wenn Sie **VirtualChannelWrite** aufrufen, können Sie eine Reihe von Benutzerdaten übergeben, die den Schreibvorgang identifizieren. Remotedesktopdienste diese Benutzerdaten zurück, wenn **VirtualChannelOpenEvent aufgerufen** wird, um Sie zu benachrichtigen, dass der Vorgang abgeschlossen wurde. Am Serverende des virtuellen Kanals ruft das Server-Add-In die [**WTSVirtualChannelRead-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) auf, um die Daten zu lesen.

Remotedesktopdienste auch Ihre [**VirtualChannelOpenEvent-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) auf, wenn Daten vom Servermodul in den virtuellen Kanal geschrieben werden. Das Servermodul ruft die [**WTSVirtualChannelWrite-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) auf, um Daten auf das Serverende des virtuellen Kanals zu schreiben.

Die Client- und Servermodule können Datenblöcke beliebiger Größe in den virtuellen Kanal schreiben. Vor dem Senden der Daten segmentiert Remotedesktopdienste daten jedoch in Segmente von CHANNEL \_ CHUNK \_ LENGTH-Bytes. Remotedesktopdienste ruft ihre [**VirtualChannelOpenEvent-Funktion**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) einmal für jeden Datenblock auf, anstatt die Daten in einem Block der ursprünglichen Größe neu zu erstellen. Jeder Aufruf von **VirtualChannelOpenEvent** gibt die Größe des Blocks, die vom Server geschriebene Gesamtgröße und an, ob die Daten den Anfang, die Mitte oder das Ende eines vom Server geschriebenen Blocks bilden.

Sie können die [**VirtualChannelClose-Funktion aufrufen,**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) um einen Kanal zu schließen. Der Aufruf ist jedoch nicht erforderlich, da Remotedesktopdienste alle Kanäle automatisch schließt, wenn der Client die Verbindung mit dem Server trennt.

 

 





