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
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a><span data-ttu-id="04c93-103">Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung</span><span class="sxs-lookup"><span data-stu-id="04c93-103">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>

<span data-ttu-id="04c93-104">In der folgenden Prozedur und in den Codebeispielen werden die Schritte zum Implementieren von Skript fähigen virtuellen Kanälen mit Remotedesktop-Webverbindung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="04c93-104">The following procedure and code examples show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span> <span data-ttu-id="04c93-105">Die Beispiele wurden in Visual Basic Scripting Edition geschrieben und gehen davon aus, dass das Remotedesktop ActiveX-Steuerelement den Namen "MsRdpClient" hat.</span><span class="sxs-lookup"><span data-stu-id="04c93-105">The examples were written in Visual Basic Scripting Edition and assume that the Remote Desktop ActiveX control is named "MsRdpClient".</span></span>

<span data-ttu-id="04c93-106">**Erstellen und Bereitstellen von Skript fähigen virtuellen Kanälen**</span><span class="sxs-lookup"><span data-stu-id="04c93-106">**To create and deploy scriptable virtual channels**</span></span>

1.  <span data-ttu-id="04c93-107">Stellen Sie die Serverseite der Anwendung bereit, und stellen Sie sicher, dass Sie auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04c93-107">Deploy the server side of the application and make sure it is running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="04c93-108">Informationen zum Bereitstellen von Anwendungen virtueller Kanäle auf dem-Server finden Sie unter [Virtual Channel Server Application](virtual-channel-server-application.md).</span><span class="sxs-lookup"><span data-stu-id="04c93-108">For information about deploying virtual channels applications on the server, see [Virtual Channel Server Application](virtual-channel-server-application.md).</span></span>
2.  <span data-ttu-id="04c93-109">Nennen Sie in Ihrem Client Skript [**imstscax:: foratevirtualchannels**](imstscax-createvirtualchannels.md), und übergeben Sie eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von Namen virtueller Kanäle enthält.</span><span class="sxs-lookup"><span data-stu-id="04c93-109">In your client script, call [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md), passing a string that contains a comma-separated list of virtual channel names.</span></span>

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    <span data-ttu-id="04c93-110">Informationen zu Benennungs Einschränkungen für virtuelle Kanäle finden Sie unter [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span><span class="sxs-lookup"><span data-stu-id="04c93-110">For information about virtual channel naming restrictions, see [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span></span>

3.  <span data-ttu-id="04c93-111">Rufen Sie [**imstscax:: Connect**](imstscax-connect.md) auf, um die Remotedesktopdienste Verbindung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="04c93-111">Call [**IMsTscAx::Connect**](imstscax-connect.md) to create your Remote Desktop Services connection.</span></span>

    ```VB
    MsRdpClient.connect
    ```

    

4.  <span data-ttu-id="04c93-112">Verwenden Sie die [**imstscax:: sendonvirtualchannel**](imstscax-sendonvirtualchannel.md) -Methode, um Daten an den Server zu senden, und übergeben Sie dabei eine Zeichenfolge mit dem Namen des virtuellen Kanals und eine zweite Zeichenfolge, die die zu übergebenen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="04c93-112">Use the [**IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) method to send data to the server, passing a string that contains the virtual channel name and a second string that contains the data to be passed.</span></span>

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  <span data-ttu-id="04c93-113">Empfangen von Daten vom Server im [**imstscaxevents:: onchannelreceiveddata**](imstscaxevents-onchannelreceiveddata.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="04c93-113">Receive data from the server on the [**IMsTscAxEvents::OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) event.</span></span>

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




