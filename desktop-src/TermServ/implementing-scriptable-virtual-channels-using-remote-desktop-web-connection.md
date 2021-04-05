---
title: Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung
description: Code Beispiele, die die Schritte zum Implementieren von Skript fähigen virtuellen Kanälen mit Remotedesktop-Webverbindung veranschaulichen.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712216"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a>Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung

In der folgenden Prozedur und in den Codebeispielen werden die Schritte zum Implementieren von Skript fähigen virtuellen Kanälen mit Remotedesktop-Webverbindung veranschaulicht. Die Beispiele wurden in Visual Basic Scripting Edition geschrieben und gehen davon aus, dass das Remotedesktop ActiveX-Steuerelement den Namen "MsRdpClient" hat.

**Erstellen und Bereitstellen von Skript fähigen virtuellen Kanälen**

1.  Stellen Sie die Serverseite der Anwendung bereit, und stellen Sie sicher, dass Sie auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird. Informationen zum Bereitstellen von Anwendungen virtueller Kanäle auf dem-Server finden Sie unter [Virtual Channel Server Application](virtual-channel-server-application.md).
2.  Nennen Sie in Ihrem Client Skript [**imstscax:: foratevirtualchannels**](imstscax-createvirtualchannels.md), und übergeben Sie eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von Namen virtueller Kanäle enthält.

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    Informationen zu Benennungs Einschränkungen für virtuelle Kanäle finden Sie unter [Virtual Channel Client Registration](virtual-channel-client-registration.md).

3.  Rufen Sie [**imstscax:: Connect**](imstscax-connect.md) auf, um die Remotedesktopdienste Verbindung zu erstellen.

    ```VB
    MsRdpClient.connect
    ```

    

4.  Verwenden Sie die [**imstscax:: sendonvirtualchannel**](imstscax-sendonvirtualchannel.md) -Methode, um Daten an den Server zu senden, und übergeben Sie dabei eine Zeichenfolge mit dem Namen des virtuellen Kanals und eine zweite Zeichenfolge, die die zu übergebenen Daten enthält.

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  Empfangen von Daten vom Server im [**imstscaxevents:: onchannelreceiveddata**](imstscaxevents-onchannelreceiveddata.md) -Ereignis.

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




