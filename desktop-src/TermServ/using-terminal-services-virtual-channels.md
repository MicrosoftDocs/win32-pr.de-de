---
title: Verwenden von Remotedesktopdienste virtuellen Kanälen
description: Zum Implementieren eines virtuellen Kanals stellen Sie die Server-und Client Module der Anwendung eines virtuellen Kanals bereit.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708753"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Verwenden von Remotedesktopdienste virtuellen Kanälen

Zum Implementieren eines virtuellen Kanals stellen Sie die Server-und Client Module der Anwendung eines virtuellen Kanals bereit. Das Servermodul kann eine Benutzermodusanwendung oder ein Kernelmodustreiber sein. Das Client Modul muss eine DLL sein.

Beschreibungen dieser Module finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Virtual Channel-Server Anwendung](virtual-channel-server-application.md)
</dt> <dd>

Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Benutzermodusanwendung sein, die in einer Client Sitzung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird. Beachten Sie, dass Sie eine Methode zum Starten der Serveranwendung bereitstellen müssen.

</dd> <dt>

[Client-DLL des virtuellen Kanals](virtual-channel-client-dll.md)
</dt> <dd>

Der Client einer virtuellen Channels-Anwendung ist eine DLL, die während der Remotedesktopdienste Initialisierung auf dem Client Computer geladen wird. Die dll muss auf dem Client Computer registriert werden.

</dd> <dt>

[Client Registrierung des virtuellen Kanals](virtual-channel-client-registration.md)
</dt> <dd>

Der Name der Client-DLL muss in der Registrierung gespeichert werden.

</dd> <dt>

[Persistente virtuelle Kanäle für die Remote Steuerung](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Ein persistenter virtueller Kanal für die Remote Steuerung wird nicht geschlossen, wenn eine Remote Steuerung die Verbindung mit dem Client herstellt oder die Verbindung trennt. Daten werden weiterhin über diesen Kanal übertragen und empfangen.

</dd> <dt>

[Dynamische virtuelle Kanäle](dynamic-virtual-channels.md)
</dt> <dd>

Die APIs des dynamischen virtuellen Kanals (DVC) erweitern die vorhandenen virtuellen Channel-APIs für Remotedesktopdienste, die als statische virtuelle Kanal-APIs bezeichnet werden.

</dd> </dl>

Wenn Sie die Anwendung eines virtuellen Kanals in der Remotedesktopdienste-Bereitstellung aktiviert haben, können Sie die Anwendung auch Client Computern zur Verfügung stellen, die mithilfe des Remotedesktop ActiveX-Steuer Elements auf den RD-Sitzungshost Server zugreifen. Weitere Informationen finden Sie unter [Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




