---
description: Windows speichert die Daten in Datei Lese-und Schreibvorgängen in vom System verwalteten Daten Puffern, um die Datenträger Leistung zu optimieren.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Leeren von System-Buffered e/a-Daten auf den Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529999"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a><span data-ttu-id="926cc-103">Leeren von System-Buffered e/a-Daten auf den Datenträger</span><span class="sxs-lookup"><span data-stu-id="926cc-103">Flushing System-Buffered I/O Data to Disk</span></span>

<span data-ttu-id="926cc-104">Windows speichert die Daten in Datei Lese-und Schreibvorgängen in vom System verwalteten Daten Puffern, um die Datenträger Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="926cc-104">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span> <span data-ttu-id="926cc-105">Wenn eine Anwendung in eine Datei schreibt, puffert das System in der Regel die Daten und schreibt die Daten in regelmäßigen Abständen auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="926cc-105">When an application writes to a file, the system usually buffers the data and writes the data to the disk on a regular basis.</span></span> <span data-ttu-id="926cc-106">Eine Anwendung kann erzwingen, dass das Betriebssystem den Inhalt dieser Datenpuffer mithilfe der [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) -Funktion auf den Datenträger schreibt.</span><span class="sxs-lookup"><span data-stu-id="926cc-106">An application can force the operating system to write the contents of these data buffers to the disk by using the [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) function.</span></span> <span data-ttu-id="926cc-107">Alternativ kann eine Anwendung festlegen, dass Schreibvorgänge den Datenpuffer umgehen und direkt auf den Datenträger schreiben, indem das **\_ Dateiflag \_ No \_ buffereing** Flag festgelegt wird, [**Wenn die Datei**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) erstellt oder mit der Funktion "Funktion" geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="926cc-107">Alternatively, an application can specify that write operations are to bypass the data buffer and write directly to the disk by setting the **FILE\_FLAG\_NO\_BUFFERING** flag when the file is created or opened using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="926cc-108">Wenn beim Schließen der Datei Daten im internen Puffer vorhanden sind, schreibt das Betriebssystem nicht automatisch den Inhalt des Puffers auf den Datenträger, bevor die Datei geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="926cc-108">If there is data in the internal buffer when the file is closed, the operating system does not automatically write the contents of the buffer to the disk before closing the file.</span></span> <span data-ttu-id="926cc-109">Wenn die Anwendung das Betriebssystem nicht zwingt, den Puffer vor dem Schließen der Datei auf den Datenträger zu schreiben, bestimmt der cachingalgorithmus, wann der Puffer geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="926cc-109">If the application does not force the operating system to write the buffer to disk before closing the file, the caching algorithm determines when the buffer is written.</span></span>

> [!Note]  
> <span data-ttu-id="926cc-110">Wenn Sie auf einen Datenpuffer zugreifen, während ein Lese-oder Schreibvorgang verwendet wird, kann der Puffer beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="926cc-110">Accessing a data buffer while a read or write operation is using it may corrupt the buffer.</span></span> <span data-ttu-id="926cc-111">Anwendungen dürfen den Datenpuffer, den ein Lese-oder Schreibvorgang verwendet, nicht lesen, schreiben, neu zuordnen oder freigeben, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="926cc-111">Applications must not read from, write to, reallocate, or free the data buffer that a read or write operation is using until the operation completes.</span></span>

 

 

 



