---
title: Band Initialisierung
description: Eine Anwendung muss die Funktion "Funktion" verwenden, um ein Handle eines Bandgeräts zu erstellen. Dieses Handle wird bei nachfolgenden Vorgängen auf dem Band des Geräts verwendet.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Sicherung der Band Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473677"
---
# <a name="tape-initialization"></a><span data-ttu-id="714e4-105">Band Initialisierung</span><span class="sxs-lookup"><span data-stu-id="714e4-105">Tape Initialization</span></span>

<span data-ttu-id="714e4-106">Eine Anwendung muss [**die Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Funktion" verwenden, um ein Handle eines Bandgeräts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="714e4-106">An application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to create a handle of a tape device.</span></span> <span data-ttu-id="714e4-107">Dieses Handle wird bei nachfolgenden Vorgängen auf dem Band des Geräts verwendet.</span><span class="sxs-lookup"><span data-stu-id="714e4-107">This handle is used in subsequent operations on the tape in the device.</span></span>

<span data-ttu-id="714e4-108">Bevor eine Anwendung auf ein Band schreibt, muss das Band gemäß den Anforderungen der Anwendung und den Funktionen des verwendeten Band Laufwerks formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="714e4-108">Before an application writes to a tape, the tape must be formatted according to the needs of the application and the capabilities of the tape drive being used.</span></span> <span data-ttu-id="714e4-109">Die Funktion " [**kreatetapepartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) " formatiert ein Band neu und erstellt dabei eine angegebene Anzahl von Partitionen mit einer angegebenen Größe.</span><span class="sxs-lookup"><span data-stu-id="714e4-109">The [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) function reformats a tape, creating on it a given number of partitions of a specified size.</span></span>

<span data-ttu-id="714e4-110">Die [**preparetape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) -Funktion bereitet ein Band für den Zugriff oder die Entfernung vor.</span><span class="sxs-lookup"><span data-stu-id="714e4-110">The [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) function prepares a tape to be accessed or removed.</span></span> <span data-ttu-id="714e4-111">Mit dieser Funktion kann ein Band geladen, entladen, gesperrt oder entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="714e4-111">This function can load, unload, lock, or unlock a tape.</span></span> <span data-ttu-id="714e4-112">Diese Funktion kann auch das Band spannen, indem Sie das Band an das Ende des Bands und zurück an den Anfang verschiebt.</span><span class="sxs-lookup"><span data-stu-id="714e4-112">This function can also tension the tape by moving the tape to the end of the tape and back to the beginning.</span></span>

<span data-ttu-id="714e4-113">Zum Abrufen und Festlegen von Informationen zu einem Band und Bandlaufwerk verwendet eine Anwendung die Funktionen [**gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**settapeparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)und [**gettapestatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .</span><span class="sxs-lookup"><span data-stu-id="714e4-113">To retrieve and set information about a tape and tape drive, an application uses the [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters), and [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) functions.</span></span>

<span data-ttu-id="714e4-114">[**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) Ruft Informationen ab, die ein Band oder ein Bandlaufwerk beschreiben.</span><span class="sxs-lookup"><span data-stu-id="714e4-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) retrieves information that describes a tape or a tape drive.</span></span> <span data-ttu-id="714e4-115">Die Bandinformationen umfassen den Typ, die Dichte und die Blockgröße des Bands. die Anzahl der Partitionen auf dem Band. die verbleibende bandmenge. Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="714e4-115">The tape information includes the tape's type, density, and block size; the number of partitions on the tape; the amount of tape remaining; and so on.</span></span> <span data-ttu-id="714e4-116">Die Informationen zum Bandlaufwerk enthalten die Standard Blockgröße des Laufwerks, die maximale Anzahl von Partitionen und die unterstützten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="714e4-116">The tape drive information includes the drive's default block size, the maximum partition count, and the features that are supported.</span></span>

<span data-ttu-id="714e4-117">Mit [**settapeparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) wird entweder die Band Blockgröße festgelegt oder die Bandlaufwerks-Flags festgelegt, die angeben, ob das Laufwerk Hardwarefehler Korrektur, Datenkomprimierung, Daten Auffüll Vorgänge oder eine beliebige Kombination der drei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="714e4-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) either sets the tape block size or sets the tape drive flags that indicate whether the drive supports hardware error correction, data compression, data padding, or any combination of the three.</span></span>

<span data-ttu-id="714e4-118">[**Gettapestatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) gibt an, ob das Bandlaufwerk für die Verarbeitung von Band Befehlen bereit ist.</span><span class="sxs-lookup"><span data-stu-id="714e4-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indicates whether the tape drive is ready to process tape commands.</span></span>

 

 