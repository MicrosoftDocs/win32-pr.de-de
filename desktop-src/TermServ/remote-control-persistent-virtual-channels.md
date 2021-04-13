---
title: Persistente virtuelle Kanäle für die Remote Steuerung
description: Ein persistenter virtueller Kanal für die Remote Steuerung wird nicht geschlossen, wenn eine Remote Steuerung die Verbindung mit dem Client herstellt oder die Verbindung trennt. Daten werden weiterhin über diesen Kanal übertragen und empfangen.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388694"
---
# <a name="remote-control-persistent-virtual-channels"></a><span data-ttu-id="804e7-104">Persistente virtuelle Kanäle für die Remote Steuerung</span><span class="sxs-lookup"><span data-stu-id="804e7-104">Remote Control Persistent Virtual Channels</span></span>

<span data-ttu-id="804e7-105">Unter Windows XP kann eine DLL einen oder mehrere virtuelle Kanäle als *persistente Remote Steuerung* angeben.</span><span class="sxs-lookup"><span data-stu-id="804e7-105">On Windows XP, a DLL can specify one or more virtual channels as *remote control persistent*.</span></span> <span data-ttu-id="804e7-106">Ein persistenter virtueller Kanal für die Remote Steuerung wird nicht geschlossen, wenn eine Remote Steuerung die Verbindung mit dem Client herstellt oder die Verbindung trennt.</span><span class="sxs-lookup"><span data-stu-id="804e7-106">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="804e7-107">Daten werden weiterhin über diesen Kanal übertragen und empfangen.</span><span class="sxs-lookup"><span data-stu-id="804e7-107">Data will continue to be transmitted and received through this channel.</span></span> <span data-ttu-id="804e7-108">Virtuelle Kanäle, die von der dll nicht als persistente Remote Steuerung angegeben werden, werden in diesem Szenario geschlossen.</span><span class="sxs-lookup"><span data-stu-id="804e7-108">Virtual channels that the DLL does not specify as remote control persistent will close in this scenario.</span></span>

<span data-ttu-id="804e7-109">Persistente virtuelle Kanäle für die Remote Steuerung werden während des Aufrufes von **virtualchannelinit** angegeben.</span><span class="sxs-lookup"><span data-stu-id="804e7-109">Remote control persistent virtual channels are specified during the call to **VirtualChannelInit**.</span></span> <span data-ttu-id="804e7-110">Spezifische Informationen hierzu finden Sie auf der Referenzseite für [**virtualchannelinit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .</span><span class="sxs-lookup"><span data-stu-id="804e7-110">Refer to the reference page for [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) for specific information about this.</span></span>

 

 




