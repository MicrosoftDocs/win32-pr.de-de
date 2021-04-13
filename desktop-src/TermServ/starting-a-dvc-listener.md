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
# <a name="starting-a-dvc-listener"></a><span data-ttu-id="a87c3-103">Starten eines DVC-Listener</span><span class="sxs-lookup"><span data-stu-id="a87c3-103">Starting a DVC Listener</span></span>

<span data-ttu-id="a87c3-104">Zum Herstellen einer erfolgreichen Verbindung zwischen zwei DVC-Modulen (Dynamic Virtual Channel), die auf dem-Client und-Server des-Remotedesktopverbindung (RDC) ausgeführt werden, muss ein DVC-Listener ausgeführt werden und sich in einem Empfangs Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="a87c3-104">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

<span data-ttu-id="a87c3-105">Die Instanziierung eines Listener erfolgt in der Regel in der [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) -Methode des DVC-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="a87c3-105">The instantiation of a listener typically occurs in the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of the DVC plug-in.</span></span> <span data-ttu-id="a87c3-106">Die Instanziierung ist jedoch nicht auf die **Initialize** -Methode beschränkt und kann an jeder beliebigen Stelle der Plug-in-Ausführung gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a87c3-106">However, instantiation is not limited to the **Initialize** method, and can be started at any point of the plug-in execution.</span></span> <span data-ttu-id="a87c3-107">Der Listener wird von der [**iwunglistener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) -Schnittstelle beschrieben, die vom [**iwzvirtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="a87c3-107">The listener is described by the [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) interface which is instantiated by the [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="a87c3-108">Eine Instanz des Kanal-Managers wird an das Plug-in am Initialisierungs Punkt an das Plug-in übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a87c3-108">An instance to the channel manager is passed to the plug-in at the initialization point.</span></span> <span data-ttu-id="a87c3-109">Das Plug-in kann einen internen Verweis auf die Instanz beibehalten, sofern dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a87c3-109">The plug-in can maintain an internal reference to the instance as long as it needs to.</span></span>

<span data-ttu-id="a87c3-110">Ein Plug-in kann beliebig viele Listener instanziieren.</span><span class="sxs-lookup"><span data-stu-id="a87c3-110">A plug-in can instantiate as many listeners as it needs to.</span></span> <span data-ttu-id="a87c3-111">Alle eingehenden Verbindungen werden von [**iwunglistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)verarbeitet [**, das in der Methode "**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) up-Methode" von [**iwsionvirtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a87c3-111">Any incoming connection will be handled by [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), which is supplied in the [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) method of [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="a87c3-112">Ein Beispiel finden Sie unter Beispielcode für die Implementierung von **cdvcsampleplugin:: Initialize** im [DVC-Client-Plug-in](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="a87c3-112">For an example, see the implementation of **CDVCSamplePlugin::Initialize** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

 

 




