---
title: Verwenden Remotedesktopdienste virtuellen Kanälen
description: Um einen virtuellen Kanal zu implementieren, stellen Sie die Server- und Clientmodule der Anwendung eines virtuellen Kanals zur Verfügung.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f538259134d539104e55706578778931a1180a1901a9891eec7f62f1f40144b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423740"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Verwenden Remotedesktopdienste virtuellen Kanälen

Um einen virtuellen Kanal zu implementieren, stellen Sie die Server- und Clientmodule der Anwendung eines virtuellen Kanals zur Verfügung. Das Servermodul kann eine Anwendung im Benutzermodus oder ein Kernelmodustreiber sein. Das Clientmodul muss eine DLL sein.

Beschreibungen dieser Module finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Virtual Channel-Serveranwendung](virtual-channel-server-application.md)
</dt> <dd>

Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Anwendung im Benutzermodus sein, die in einer Clientsitzung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird. Beachten Sie, dass Sie eine Methode bereitstellen müssen, um die Serveranwendung zu starten.

</dd> <dt>

[Virtual Channel-Client-DLL](virtual-channel-client-dll.md)
</dt> <dd>

Der Client einer Anwendung für virtuelle Kanäle ist eine DLL, die während der Remotedesktopdienste auf dem Clientcomputer geladen wird. Die DLL muss auf dem Clientcomputer registriert sein.

</dd> <dt>

[Clientregistrierung für den virtuellen Kanal](virtual-channel-client-registration.md)
</dt> <dd>

Sie müssen den Namen der Client-DLL in der Registrierung speichern.

</dd> <dt>

[Persistente virtuelle Kanäle für die Remotesteuerung](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Ein persistenter virtueller Remotesteuerungskanal wird nicht geschlossen, wenn eine Remotesteuerung eine Verbindung mit der Sitzung herstellt oder trennt, die mit dem Client verbunden ist. Daten werden weiterhin über diesen Kanal übertragen und empfangen.

</dd> <dt>

[Dynamische virtuelle Kanäle](dynamic-virtual-channels.md)
</dt> <dd>

Die APIs des dynamischen virtuellen Kanals (Dynamic Virtual Channel, DVC) erweitern die vorhandenen APIs des virtuellen Kanals für Remotedesktopdienste, die als statische virtuelle Kanal-APIs (Static Virtual Channel, SVC) bezeichnet werden.

</dd> </dl>

Wenn Sie die Anwendung eines virtuellen Kanals in Ihrer Remotedesktopdienste-Bereitstellung aktiviert haben, können Sie die Anwendung auch clientcomputern zur Verfügung stellen, die über das Remotedesktop ActiveX-Steuerelement auf den RD-Sitzungshost-Server zugreifen. Weitere Informationen finden Sie unter [Verwenden des Remotedesktop ActiveX-Steuerelements mit virtuellen Kanälen.](using-the-remote-desktop-activex-control-with-virtual-channels.md)

 

 




