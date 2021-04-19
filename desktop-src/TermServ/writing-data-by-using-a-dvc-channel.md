---
title: Schreiben von Daten mithilfe eines DVC-Kanals
description: Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DVC) ist sowohl für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server als auch für den Client symmetrisch.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338198"
---
# <a name="writing-data-by-using-a-dvc-channel"></a><span data-ttu-id="40664-103">Schreiben von Daten mithilfe eines DVC-Kanals</span><span class="sxs-lookup"><span data-stu-id="40664-103">Writing Data by Using a DVC Channel</span></span>

<span data-ttu-id="40664-104">Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DVC) ist sowohl für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server als auch für den Client symmetrisch.</span><span class="sxs-lookup"><span data-stu-id="40664-104">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span> <span data-ttu-id="40664-105">Das Schreiben von Kanaldaten wird von der [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) -Methode der [**iwzvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="40664-105">The writing of channel data is implemented by the [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) method of the [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) interface.</span></span>

<span data-ttu-id="40664-106">Die folgende Abbildung zeigt das Senden und empfangen des Datenpakets zwischen dem DVC-Client und-Server (DVC-Plug-in).</span><span class="sxs-lookup"><span data-stu-id="40664-106">The following illustration shows the sending and receiving of the data packet between the DVC client and server (DVC plug-in).</span></span>

![Senden und Empfangen eines Datenpakets zwischen dem DVC-Client und-Server](images/writedvcchannel.png)

 

 




