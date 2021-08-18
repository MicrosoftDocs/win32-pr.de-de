---
title: Starten eines DVC-Listeners
description: Um eine erfolgreiche Verbindung zwischen zwei DVC-Modulen (Dynamic Virtual Channel) herzustellen, die auf dem Remotedesktopverbindung-Client und -Server (RDC) ausgeführt werden, muss ein DVC-Listener ausgeführt werden und sich im Lauschzustand befinden.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d440069cb64597c16a14323a67926376bf1c425f5a29c77e451c52866a5399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000450"
---
# <a name="starting-a-dvc-listener"></a>Starten eines DVC-Listeners

Um eine erfolgreiche Verbindung zwischen zwei DVC-Modulen (Dynamic Virtual Channel) herzustellen, die auf dem Remotedesktopverbindung-Client und -Server (RDC) ausgeführt werden, muss ein DVC-Listener ausgeführt werden und sich im Lauschzustand befinden.

Die Instanziierung eines Listeners erfolgt in der Regel in der [**Initialize-Methode**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) des DVC-Plug-Ins. Die Instanziierung ist jedoch nicht auf die **Initialize-Methode** beschränkt und kann zu jedem Zeitpunkt der Plug-In-Ausführung gestartet werden. Der Listener wird von der [**IWTSListener-Schnittstelle**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) beschrieben, die vom [**IWTSVirtualChannelManager instanziiert wird.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) Eine -Instanz an den Kanal-Manager wird am Initialisierungspunkt an das Plug-In übergeben. Das Plug-In kann einen internen Verweis auf die Instanz verwalten, solange dies benötigt wird.

Ein Plug-In kann so viele Listener instanziieren, wie es benötigt. Alle eingehenden Verbindungen werden von [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)verarbeitet, das in der [**CreateListener-Methode**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) von [**IWTSVirtualChannelManager bereitgestellt wird.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) Ein Beispiel finden Sie in der Implementierung von **CDVCSamplePlugin::Initialize** im [Beispielcode des DVC-Client-Plug-Ins.](dvc-client-plug-in-example.md)

 

 




