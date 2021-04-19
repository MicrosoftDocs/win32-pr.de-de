---
description: Stations Sätze, die über einen Drittanbieter Link überwacht werden, werden als Linien Gerät und möglicherweise als zugehöriges Telefongerät modelliert.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Station
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360875"
---
# <a name="stations"></a><span data-ttu-id="126ff-103">Station</span><span class="sxs-lookup"><span data-stu-id="126ff-103">Stations</span></span>

<span data-ttu-id="126ff-104">Stations Sätze, die über einen Drittanbieter Link überwacht werden, werden als Linien Gerät und möglicherweise als zugehöriges Telefongerät modelliert.</span><span class="sxs-lookup"><span data-stu-id="126ff-104">Station sets being monitored through a third-party link are modeled as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="126ff-105">Das liniengerät kann mehrere Adressen haben, wenn das modellierte Terminal mehr als eine Verzeichnis Nummer (DN) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="126ff-105">The line device can have multiple addresses, if the modeled terminal supports more than one directory number (DN).</span></span> <span data-ttu-id="126ff-106">Mehrere Aufrufe zum Aufrufen desselben DN können als einzelne Adresse modelliert werden, die mehrere Aufrufe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="126ff-106">Multiple call appearances on the same DN can be modeled as a single address that supports multiple calls.</span></span>

<span data-ttu-id="126ff-107">Aufrufe zwischen zwei Stationen auf dem Switch verfügen über zwei Aufruf Handles, von denen eine die Aufruf Ansicht von der ersten Station (auf Ihrem liniengerät) und die andere die Aufruf Ansicht von der zweiten Station (auf dem liniengerät) gibt.</span><span class="sxs-lookup"><span data-stu-id="126ff-107">Calls between two stations on the switch have two call handles, one giving the call view from the first station (on its line device), and the other giving the call view from the second station (on its line device).</span></span> <span data-ttu-id="126ff-108">Beispielsweise würde ein [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) eines Drittanbieters, das von einer Anwendung auf dem Server platziert wurde, an das Zeilen Gerät geleitet, das der Station zugeordnet ist, von der der Anruf gewählt werden soll. in dieser Zeile wird ein Anruf Handle für die in [**linecallparamemes**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) angegebene Adresse erstellt (auf diese Weise wird gesteuert, welcher DN auf einem Telefon verwendet wird, das mehrere DNS unterstützt).</span><span class="sxs-lookup"><span data-stu-id="126ff-108">For example, a third-party [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) placed by an application on the server would be directed to the line device associated with the station from which the call is to be dialed; a call handle would be created on that line, on the address specified in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (thereby giving control over which DN is used on a phone that supports multiple DNs).</span></span> <span data-ttu-id="126ff-109">Wenn der-Befehl für die Zieladresse bereitgestellt wird, wird ein neues Rückruf Handle erstellt, das einen aufrufenden Ansichts *Zustand anzeigt* . Anwendungen wissen, dass es sich um eine weitere Ansicht desselben Aufrufs durch den **dwcallid** -Member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) handelt, der für beide Aufrufe gleich ist.</span><span class="sxs-lookup"><span data-stu-id="126ff-109">When the call is offered to the destination address, a new call handle showing a call in *offering* state is created; applications would know that it was another view of the same call by the **dwCallID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) being equal for both calls.</span></span> <span data-ttu-id="126ff-110">Beide Aufrufe laufen in den *Leerlauf* , wenn der Aufruf gelöscht wurde. ein-Rückruf konnte von der Drittanbieter Anwendung gelöscht werden, indem ein [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) für einen der-Rückruf Handles ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="126ff-110">Both calls would go *idle* when the call was dropped; a call could be dropped from the third-party application by doing a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on either of the call handles.</span></span>

 

 



