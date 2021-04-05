---
title: Client-DLL des virtuellen Kanals
description: Der Client einer virtuellen Channels-Anwendung ist eine DLL, die während der Remotedesktopdienste Initialisierung auf dem Client Computer geladen wird. Die dll muss auf dem Client Computer registriert werden.
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd7ffccda8b1da7dfc3920b0a47a12e97840e0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037023"
---
# <a name="virtual-channel-client-dll"></a>Client-DLL des virtuellen Kanals

Der Client einer virtuellen Channels-Anwendung ist eine DLL, die während der Remotedesktopdienste Initialisierung auf dem Client Computer geladen wird. Die dll muss auf dem Client Computer registriert werden. Weitere Informationen finden Sie unter [Virtual Channel Client Registration](virtual-channel-client-registration.md).

Die Client-DLL muss eine [**virtualchannelentry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) -Funktion exportieren, die während der Initialisierung Remotedesktopdienste aufruft. Der Einstiegspunkt " **virtualchannelentry** " erhält einen Zeiger auf die Struktur der [**Kanal \_ Einstiegs \_ Punkte**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points) . Diese Struktur enthält Zeiger auf die Funktionen, die von der Client-DLL aufgerufen werden, um auf virtuelle Kanäle zuzugreifen.



| Funktion                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Virtualchannelinit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | Registriert die Namen der virtuellen Kanäle, die vom Client verwendet werden sollen, und stellt eine [**virtualchannelinitevent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) -Rückruffunktion bereit, über die Remotedesktopdienste den Client über Ereignisse benachrichtigt, die die Client Verbindung beeinflussen.<br/> |
| [**Virtualchannelopen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | Öffnet das Client Ende eines angegebenen virtuellen Kanals und stellt eine [**virtualchannelopenevent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) -Rückruffunktion bereit, über die Remotedesktopdienste den Client über Ereignisse benachrichtigt, die den virtuellen Kanal betreffen.<br/>                    |
| [**Virtualchannelwrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | Schreibt Daten in einen virtuellen Kanal. Remotedesktopdienste sendet diese Daten an das Server Ende des virtuellen Kanals. Das Server Ende Ruft die [**Wout virtualchannelread**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) -Funktion auf, um die Daten zu lesen.<br/>                                             |
| [**Virtualchannelclose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | Schließt einen virtuellen Kanal.<br/>                                                                                                                                                                                                                                                  |



 

Die [**virtualchannelentry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) -Funktion der dll muss die [**virtualchannelinit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) -Funktion aufrufen, um den Zugriff auf virtuelle Kanäle zu initialisieren. Wenn Sie **virtualchannelinit** aufgerufen haben, müssen Sie einen Zeiger an die [**virtualchannelinitevent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) -Rückruffunktion übergeben. Remotedesktopdienste ruft diese Rückruffunktion auf, wenn die Initialisierung abgeschlossen ist, und wieder, wenn eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost) Server hergestellt wurde.

Nachdem die Verbindung hergestellt wurde, können Sie die [**virtualchannelopen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) -Funktion zum Öffnen der durch den [**virtualchannelinit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) -Befehl registrierten virtuellen Kanäle aufzurufen. Der **virtualchannelopen** -Befehl gibt einen Zeiger auf die [**virtualchannelopenevent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) -Rückruffunktion an.

Nachdem der [**virtualchannelopen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) -Rückruf zurückgegeben wurde, können Sie die [**virtualchannelwrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) -Funktion zum Schreiben in den virtuellen Kanal abrufen. Der Schreibvorgang ist asynchron. Daher dürfen Sie den an **virtualchannelwrite** über gebenden Puffer nicht freigeben oder wieder verwenden, bis Remotedesktopdienste die [**virtualchannelopenevent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) -Funktion aufruft, um anzugeben, dass der Schreibvorgang abgeschlossen wurde. Wenn Sie **virtualchannelwrite** aufgerufen haben, können Sie ein Benutzerdaten-Element übergeben, das den Schreibvorgang identifiziert. Remotedesktopdienste übergibt diese Benutzerdaten zurück, wenn **virtualchannelopenevent** aufgerufen wird, um Sie zu benachrichtigen, dass der Vorgang abgeschlossen wurde. Am Server Ende des virtuellen Kanals ruft das Server-Add-in die Funktion [**Wout virtualchannelread**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) auf, um die Daten zu lesen.

Remotedesktopdienste ruft auch Ihre [**virtualchannelopenevent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) -Funktion auf, wenn Daten vom Servermodul in den virtuellen Kanal geschrieben werden. Das Servermodul Ruft die [**Wout virtualchannelwrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) -Funktion auf, um Daten auf das Server Ende des virtuellen Kanals zu schreiben.

Die Module Client und Server können Datenblöcke beliebiger Größe in den virtuellen Kanal schreiben. Vor dem Senden der Daten werden die Daten jedoch Remotedesktopdienste in Segmente von Segmenten mit channellänge von Segmenten segmentiert \_ \_ . Remotedesktopdienste die [**virtualchannelopenevent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) -Funktion für jeden Datenblock einmal aufruft, anstatt die Daten in einen Block der ursprünglichen Größe neu zu erstellen. Jeder Aufrufe von **virtualchannelopenevent** gibt die Größe des Blocks, die vom Server geschriebene Gesamtgröße an und gibt an, ob die Daten den Anfang, das Mittel oder das Ende eines Blocks darstellen, der vom Server geschrieben wird.

Sie können die [**virtualchannelclose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) -Funktion zum Schließen eines Kanals aufzurufen. Es ist jedoch nicht notwendig, ihn aufzurufen, da Remotedesktopdienste alle Kanäle automatisch schließt, wenn der Client die Verbindung mit dem Server trennt.

 

 





