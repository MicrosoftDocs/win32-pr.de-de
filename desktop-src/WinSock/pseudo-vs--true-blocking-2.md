---
description: Pseudo blockierende Pseudo Blockierungs Vorgänge in Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo Blockierung und echte Blockierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347073"
---
# <a name="pseudo-blocking-and-true-blocking"></a><span data-ttu-id="a60ec-103">Pseudo Blockierung und echte Blockierung</span><span class="sxs-lookup"><span data-stu-id="a60ec-103">Pseudo Blocking and True Blocking</span></span>

<span data-ttu-id="a60ec-104">In 16 Windows-Umgebungen wird eine echte Blockierung vom Betriebssystem nicht unterstützt. Daher wird ein blockierender Vorgang, der nicht sofort abgeschlossen werden kann, wie folgt behandelt:</span><span class="sxs-lookup"><span data-stu-id="a60ec-104">In 16 Windows environments, true blocking is not supported by the operating system; therefore, a blocking operation that cannot be completed immediately is handled as follows:</span></span>

-   <span data-ttu-id="a60ec-105">Der Dienstanbieter initiiert den Vorgang und gibt dann eine Schleife ein, in der alle Windows-Meldungen gesendet werden (falls erforderlich, wenn der Prozessor einem anderen Thread bereit steht).</span><span class="sxs-lookup"><span data-stu-id="a60ec-105">The service provider initiates the operation, and then enters a loop during which it dispatches any Windows messages (yielding the processor to another thread if necessary)</span></span>
-   <span data-ttu-id="a60ec-106">Anschließend wird überprüft, ob die Windows Sockets-Funktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a60ec-106">It then checks for the completion of the Windows Sockets function.</span></span>
-   <span data-ttu-id="a60ec-107">Wenn die Funktion abgeschlossen wurde oder [**wspcancelblockingcallaufgerufen**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) wurde, wird die Schleife beendet, und die blockierende Funktion wird mit einem entsprechenden Ergebnis abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a60ec-107">If the function has completed, or if [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) has been invoked, the loop is terminated and the blocking function completes with an appropriate result.</span></span>

<span data-ttu-id="a60ec-108">Dies ist der Begriff "Pseudo Blockierung", und die oben erwähnte Schleife wird als standardmäßiger blockierender Hook bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a60ec-108">This is what is meant by the term pseudo blocking, and the loop referred to above is known as the default blocking hook.</span></span>

 

 
