---
description: Es gibt andere Situationen, in denen ein Lese-oder Schreibvorgang mit weniger als der angeforderten Anzahl von Zeichen abgeschlossen werden kann, obwohl kein Timeout aufgetreten ist.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Kommunikationsfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483286"
---
# <a name="communications-errors"></a><span data-ttu-id="8bfa2-103">Kommunikationsfehler</span><span class="sxs-lookup"><span data-stu-id="8bfa2-103">Communications Errors</span></span>

<span data-ttu-id="8bfa2-104">Es gibt andere Situationen, in denen ein Lese-oder Schreibvorgang mit weniger als der angeforderten Anzahl von Zeichen abgeschlossen werden kann, obwohl kein Timeout aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-104">There are other circumstances where a read or write operation can be completed with fewer than the requested number of characters, even though a time-out has not occurred.</span></span> <span data-ttu-id="8bfa2-105">Nachstehend sind einige Beispiele aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="8bfa2-105">Following are some examples:</span></span>

-   <span data-ttu-id="8bfa2-106">Einige Treiber unterstützen die Verwendung von Sonderzeichen, die einen Lesevorgang sofort mit nur den Zeichen durchführen, die bis zu dem Zeitpunkt gelesen wurden, zu dem Sie empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-106">Some drivers support the use of special characters, which complete a read operation immediately with only the characters that have been read up to the point when they are received.</span></span>
-   <span data-ttu-id="8bfa2-107">Die [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) -Funktion kann aufgerufen werden, um ausstehende Lese-oder Schreibvorgänge vorzeitig zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-107">The [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) function can be called to prematurely terminate pending read or write operations.</span></span> <span data-ttu-id="8bfa2-108">Diese Funktion kann auch den Inhalt der Ausgabe-oder Eingabepuffer oder beides löschen.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-108">This function can also delete the contents of the output or input buffers, or both.</span></span>
-   <span data-ttu-id="8bfa2-109">Wenn während eines Lese-oder Schreibvorgangs ein Kommunikationsfehler auftritt, werden alle e/a-Vorgänge für die Kommunikations Ressource beendet.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-109">If a communications error occurs during a read or write operation, all I/O operations on the communications resource are terminated.</span></span> <span data-ttu-id="8bfa2-110">Unterbrechen von Bedingungen, Paritäts Fehlern oder framingfehlern sind Beispiele für derartige Fehler.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-110">Break conditions, parity errors, or framing errors are examples of such errors.</span></span> <span data-ttu-id="8bfa2-111">Wenn ein Fehler auftritt, muss der Prozess die [**clearcommerror**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) -Funktion aufrufen, um das Fehlerflag zu löschen, bevor zusätzliche e/a-Vorgänge beginnen können.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-111">When an error occurs, the process must call the [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) function to clear the error flag before it can begin additional I/O operations.</span></span> <span data-ttu-id="8bfa2-112">**Clearcommerror** meldet den spezifischen Fehler und den aktuellen Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="8bfa2-112">**ClearCommError** reports the specific error that occurred and the current status of the device.</span></span>

 

 



