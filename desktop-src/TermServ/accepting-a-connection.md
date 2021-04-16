---
title: Akzeptieren einer Verbindung (Remotedesktopdienste)
description: Zu einem bestimmten Zeitpunkt fordert der DVC-Client (Dynamic Virtual Channel) eine Verbindung mit dem DVC-Listener an.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104567993"
---
# <a name="accepting-a-connection-remote-desktop-services"></a><span data-ttu-id="acaf5-103">Akzeptieren einer Verbindung (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="acaf5-103">Accepting a Connection (Remote Desktop Services)</span></span>

<span data-ttu-id="acaf5-104">Zu einem bestimmten Zeitpunkt fordert der DVC-Client (Dynamic Virtual Channel) eine Verbindung mit dem DVC-Listener an.</span><span class="sxs-lookup"><span data-stu-id="acaf5-104">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span> <span data-ttu-id="acaf5-105">Wenn dies auftritt, kann der Listener einen eindeutigen Kommunikationskanal zum Client erzeugen, der von der [**onnewchannelconnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) -Methode von [**iwunglistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="acaf5-105">When this occurs, the listener can spawn a unique communication channel to the client, which is handled by the [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) method of [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span></span> <span data-ttu-id="acaf5-106">Ein Beispiel finden Sie unter Beispielcode für die Implementierung von **cdvcsampleplugin:: onnewchannelconnection** im [DVC-Client-Plug-in](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="acaf5-106">For an example, see the implementation of **CDVCSamplePlugin::OnNewChannelConnection** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

<span data-ttu-id="acaf5-107">In der folgenden Abbildung wird die Abfolge der Ereignisse für das Herstellen einer DVC-Verbindung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="acaf5-107">The following figure shows the sequence of events for establishing a DVC connection.</span></span> <span data-ttu-id="acaf5-108">Die schattierten Objekte sind vom Benutzer bereitgestellt (DVC-Anwendung/-Dienst und [**iwtionlistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), während die nicht schattierten Objekte Teil des Frameworks sind (Remotedesktop-Sitzungshost (RD-Sitzungshost), Listener und [**iwtionvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span><span class="sxs-lookup"><span data-stu-id="acaf5-108">The shaded objects are user-supplied (DVC application/service and [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), while the un-shaded objects are part of the framework (Remote Desktop Session Host (RD Session Host) service, listener, and [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span></span>

![Abfolge von Ereignissen für das Herstellen einer DVC-Verbindung](images/acceptingconnection.png)

> [!Note]  
> <span data-ttu-id="acaf5-110">In dieser Abbildung wird davon ausgegangen, dass ein Listenerobjekt durch einen "up" [**-Aufrufs**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) von " [**iwtionvirtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)" erstellt wurde und dass das Plug-in " [**iwtionlistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) " als Parameter angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="acaf5-110">This figure assumes that a listener object has been created through a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) call to [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), and that the plug-in has specified [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) as a parameter.</span></span>

 

 

 




