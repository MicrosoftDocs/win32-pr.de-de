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
# <a name="accepting-a-connection-remote-desktop-services"></a>Akzeptieren einer Verbindung (Remotedesktopdienste)

Zu einem bestimmten Zeitpunkt fordert der DVC-Client (Dynamic Virtual Channel) eine Verbindung mit dem DVC-Listener an. Wenn dies auftritt, kann der Listener einen eindeutigen Kommunikationskanal zum Client erzeugen, der von der [**onnewchannelconnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) -Methode von [**iwunglistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)verarbeitet wird. Ein Beispiel finden Sie unter Beispielcode für die Implementierung von **cdvcsampleplugin:: onnewchannelconnection** im [DVC-Client-Plug-in](dvc-client-plug-in-example.md) .

In der folgenden Abbildung wird die Abfolge der Ereignisse für das Herstellen einer DVC-Verbindung veranschaulicht. Die schattierten Objekte sind vom Benutzer bereitgestellt (DVC-Anwendung/-Dienst und [**iwtionlistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), während die nicht schattierten Objekte Teil des Frameworks sind (Remotedesktop-Sitzungshost (RD-Sitzungshost), Listener und [**iwtionvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).

![Abfolge von Ereignissen für das Herstellen einer DVC-Verbindung](images/acceptingconnection.png)

> [!Note]  
> In dieser Abbildung wird davon ausgegangen, dass ein Listenerobjekt durch einen "up" [**-Aufrufs**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) von " [**iwtionvirtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)" erstellt wurde und dass das Plug-in " [**iwtionlistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) " als Parameter angegeben hat.

 

 

 




