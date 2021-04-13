---
title: Starten eines DVC-Listener
description: Zum Herstellen einer erfolgreichen Verbindung zwischen zwei DVC-Modulen (Dynamic Virtual Channel), die auf dem-Client und-Server des-Remotedesktopverbindung (RDC) ausgeführt werden, muss ein DVC-Listener ausgeführt werden und sich in einem Empfangs Zustand befinden.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311321"
---
# <a name="starting-a-dvc-listener"></a>Starten eines DVC-Listener

Zum Herstellen einer erfolgreichen Verbindung zwischen zwei DVC-Modulen (Dynamic Virtual Channel), die auf dem-Client und-Server des-Remotedesktopverbindung (RDC) ausgeführt werden, muss ein DVC-Listener ausgeführt werden und sich in einem Empfangs Zustand befinden.

Die Instanziierung eines Listener erfolgt in der Regel in der [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) -Methode des DVC-Plug-ins. Die Instanziierung ist jedoch nicht auf die **Initialize** -Methode beschränkt und kann an jeder beliebigen Stelle der Plug-in-Ausführung gestartet werden. Der Listener wird von der [**iwunglistener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) -Schnittstelle beschrieben, die vom [**iwzvirtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)instanziiert wird. Eine Instanz des Kanal-Managers wird an das Plug-in am Initialisierungs Punkt an das Plug-in übermittelt. Das Plug-in kann einen internen Verweis auf die Instanz beibehalten, sofern dies erforderlich ist.

Ein Plug-in kann beliebig viele Listener instanziieren. Alle eingehenden Verbindungen werden von [**iwunglistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)verarbeitet [**, das in der Methode "**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) up-Methode" von [**iwsionvirtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)angegeben wird. Ein Beispiel finden Sie unter Beispielcode für die Implementierung von **cdvcsampleplugin:: Initialize** im [DVC-Client-Plug-in](dvc-client-plug-in-example.md) .

 

 




