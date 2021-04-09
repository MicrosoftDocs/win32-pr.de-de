---
title: Eingabe des passiven Zustands
description: Eingabe des passiven Zustands
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856780"
---
# <a name="entering-the-passive-state"></a><span data-ttu-id="4a5af-103">Eingabe des passiven Zustands</span><span class="sxs-lookup"><span data-stu-id="4a5af-103">Entering the Passive State</span></span>

<span data-ttu-id="4a5af-104">Die Objekt Schließung erzwingt ein eingebettetes oder verknüpftes Objekt in den passiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="4a5af-104">Object closure forces an embedded or linked object into the passive state.</span></span> <span data-ttu-id="4a5af-105">Sie wird in der Regel von der Benutzeroberfläche der OLE Server-Anwendung initiiert, z. b. wenn der Benutzer den Befehl zum Schließen der Datei auswählt.</span><span class="sxs-lookup"><span data-stu-id="4a5af-105">It is typically initiated from the OLE server application's user interface, such as when the user selects the File Close command.</span></span> <span data-ttu-id="4a5af-106">In diesem Fall benachrichtigt die OLE Server-Anwendung den Container, der seinen Verweis Zähler für das Objekt freigibt.</span><span class="sxs-lookup"><span data-stu-id="4a5af-106">In this case, the OLE server application notifies the container, which releases its reference count on the object.</span></span> <span data-ttu-id="4a5af-107">Wenn alle Verweise auf das Objekt freigegeben wurden, kann das Objekt freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a5af-107">When all references to the object have been released, the object can be freed.</span></span> <span data-ttu-id="4a5af-108">Wenn alle Objekte freigegeben wurden, kann die OLE-Serveranwendung sicher beendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a5af-108">When all objects have been freed, the OLE server application can safely terminate.</span></span>

<span data-ttu-id="4a5af-109">Eine Containeranwendung kann auch die Objekt Schließung initiieren.</span><span class="sxs-lookup"><span data-stu-id="4a5af-109">A container application can also initiate object closure.</span></span> <span data-ttu-id="4a5af-110">Um ein Objekt zu schließen, gibt der Container seinen Verweis Zähler frei, nachdem ein optionaler Speichervorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4a5af-110">To close an object, the container releases its reference count after completing an optional save operation.</span></span> <span data-ttu-id="4a5af-111">Sie können Container so entwerfen, dass Objekte freigegeben werden, wenn Sie nach einer direkten Aktivierungs Sitzung deaktiviert werden, sodass der Benutzer außerhalb des Objekts auf das Objekt klicken kann, ohne die aktive Bearbeitungs Sitzung zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="4a5af-111">You can design containers to release objects when they are deactivating after an in-place activation session, allowing the user to click outside the object without losing the active editing session.</span></span>

 

 




