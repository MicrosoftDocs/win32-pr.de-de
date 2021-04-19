---
description: Die einfachste Art von e/a in Windows Sockets 2 ist das Blockieren von e/a.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blockieren von Eingaben/Ausgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348393"
---
# <a name="blocking-inputoutput"></a><span data-ttu-id="f6346-103">Blockieren von Eingaben/Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6346-103">Blocking Input/Output</span></span>

<span data-ttu-id="f6346-104">Die einfachste Art von e/a in Windows Sockets 2 ist das Blockieren von e/a.</span><span class="sxs-lookup"><span data-stu-id="f6346-104">The simplest form of I/O in Windows Sockets 2 is blocking I/O.</span></span> <span data-ttu-id="f6346-105">Wie in [socketattributflags und-Modi](socket-attribute-flags-and-modes-2.md)erwähnt, werden Sockets standardmäßig im Blockierungs Modus erstellt.</span><span class="sxs-lookup"><span data-stu-id="f6346-105">As mentioned in [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md), sockets are created in blocking mode by default.</span></span> <span data-ttu-id="f6346-106">Ein e/a-Vorgang mit einem blockierenden Socket wird erst zurückgegeben, wenn der Vorgang vollständig abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f6346-106">Any I/O operation with a blocking socket will not return until the operation has been fully completed.</span></span> <span data-ttu-id="f6346-107">Daher kann jeder Thread nur einen e/a-Vorgang gleichzeitig ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6346-107">Thus, any thread can only execute one I/O operation at a time.</span></span> <span data-ttu-id="f6346-108">Wenn ein Thread z. b. einen Empfangsvorgang ausgibt und derzeit keine Daten verfügbar sind, wird der Thread blockiert, bis die Daten verfügbar sind und in den Puffer des Threads eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f6346-108">For example, if a thread issues a receive operation and no data is currently available, the thread will block until data becomes available and is placed into the thread's buffer.</span></span> <span data-ttu-id="f6346-109">Obwohl dies einfach ist, ist es nicht notwendigerweise die effizienteste Methode, e/a-Vorgänge durchzuführen (Weitere Informationen finden Sie unter [Pseudo Blockierung und echte Blockierung](pseudo-vs--true-blocking-2.md) ).</span><span class="sxs-lookup"><span data-stu-id="f6346-109">Although this is simple, it is not necessarily the most efficient way to do I/O (see [Pseudo Blocking and True Blocking](pseudo-vs--true-blocking-2.md) for more information).</span></span>

 

 



