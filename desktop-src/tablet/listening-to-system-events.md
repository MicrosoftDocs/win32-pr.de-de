---
description: Anwendungen können Systemereignisse überwachen, indem Sie das InkCollector-Objekt verwenden und das System Gesten-Ereignis darauf lauschen.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Lauschen auf System Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050532"
---
# <a name="listening-to-system-events"></a><span data-ttu-id="005d7-103">Lauschen auf System Ereignisse</span><span class="sxs-lookup"><span data-stu-id="005d7-103">Listening to System Events</span></span>

<span data-ttu-id="005d7-104">Anwendungen können Systemereignisse überwachen, indem Sie das [**InkCollector**](inkcollector-class.md) -Objekt verwenden und das System [**Gesten**](inkcollector-systemgesture.md) -Ereignis darauf lauschen.</span><span class="sxs-lookup"><span data-stu-id="005d7-104">Applications can listen to system events by using the [**InkCollector**](inkcollector-class.md) object and listening for the [**SystemGesture**](inkcollector-systemgesture.md) event on it.</span></span> <span data-ttu-id="005d7-105">Sie können festlegen, auf welche Ereignisse eine Anwendung lauscht.</span><span class="sxs-lookup"><span data-stu-id="005d7-105">You can set which events an application listens to.</span></span> <span data-ttu-id="005d7-106">Wenn eine tablettstiftaktion auftritt, wird das entsprechende **systemgesten** -Ereignis an die Anwendung im **InkCollector** -Objekt gesendet.</span><span class="sxs-lookup"><span data-stu-id="005d7-106">When a tablet pen action occurs, the corresponding **SystemGesture** event is sent to the application on its **InkCollector** object.</span></span> <span data-ttu-id="005d7-107">Eine Anwendung kann die Maus Meldung abbrechen, die einem bestimmten **systemgesten** -Ereignis entspricht, wenn das Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="005d7-107">An application can cancel the mouse message that corresponds to a given **SystemGesture** event when it receives the event.</span></span> <span data-ttu-id="005d7-108">Ausführliche Informationen zum Abbrechen von Maus Meldungen finden Sie unter **systemgesten** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="005d7-108">For details about canceling mouse messages, see **SystemGesture** event.</span></span>

 

 



