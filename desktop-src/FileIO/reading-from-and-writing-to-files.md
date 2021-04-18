---
description: Eine Anwendung liest aus einer Datei und schreibt Sie mithilfe der Funktionen "Infofile", "infofileex", "Write file" und "Write fileex".
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lesen aus und Schreiben in Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352453"
---
# <a name="reading-from-and-writing-to-files"></a><span data-ttu-id="40763-103">Lesen aus und Schreiben in Dateien</span><span class="sxs-lookup"><span data-stu-id="40763-103">Reading From and Writing to Files</span></span>

<span data-ttu-id="40763-104">Eine Anwendung liest aus einer Datei und schreibt Sie mithilfe der Funktionen " [**Infofile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)", " [**infofileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)", " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)" und " [**Write fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) ".</span><span class="sxs-lookup"><span data-stu-id="40763-104">An application reads from and writes to a file by using the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) functions.</span></span> <span data-ttu-id="40763-105">Diese Funktionen erfordern ein Handle für eine Datei, die zum Lesen bzw. Schreiben geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="40763-105">These functions require a handle to a file to be opened for reading and writing, respectively.</span></span> <span data-ttu-id="40763-106">Sie lesen und schreiben eine angegebene Anzahl von Bytes an dem Speicherort, der durch den Dateizeiger angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="40763-106">They read and write a specified number of bytes at the location indicated by the file pointer.</span></span> <span data-ttu-id="40763-107">Die Daten werden genau wie angegeben gelesen und geschrieben. die-Funktionen formatieren die Daten nicht.</span><span class="sxs-lookup"><span data-stu-id="40763-107">The data is read and written exactly as specified; the functions do not format the data.</span></span>

<span data-ttu-id="40763-108">Wenn der Dateizeiger das Ende einer Datei erreicht und die Anwendung versucht, aus der Datei zu lesen, tritt kein Fehler auf, aber es werden keine Bytes gelesen.</span><span class="sxs-lookup"><span data-stu-id="40763-108">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="40763-109">Daher bedeutet das Lesen von 0 Bytes ohne Fehler, dass die Anwendung das Ende der Datei erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="40763-109">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="40763-110">Das Schreiben von 0 Bytes bewirkt nichts.</span><span class="sxs-lookup"><span data-stu-id="40763-110">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="40763-111">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="40763-111">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="40763-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="40763-112">In this section</span></span>



| <span data-ttu-id="40763-113">Thema</span><span class="sxs-lookup"><span data-stu-id="40763-113">Topic</span></span>                                                                                                                                           | <span data-ttu-id="40763-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40763-114">Description</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40763-115">Positionieren eines Dateizeigers</span><span class="sxs-lookup"><span data-stu-id="40763-115">Positioning a File Pointer</span></span>](positioning-a-file-pointer.md)<br/>                                                                         | <span data-ttu-id="40763-116">Windows verwendet einen Dateizeiger, um die gelesenen oder geschriebenen Bytes nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="40763-116">Windows uses a file pointer to keep track of bytes read or written.</span></span><br/>                                                       |
| [<span data-ttu-id="40763-117">Lesen aus oder schreiben in Dateien mit einem Scatter-Gather Schema</span><span class="sxs-lookup"><span data-stu-id="40763-117">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | <span data-ttu-id="40763-118">Beschreibt ein Scatter-Gather-Schema zum Lesen oder Schreiben von nicht zusammenhängenden Datenblöcken in einem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="40763-118">Describes a scatter-gather scheme for reading or writing noncontiguous chunks of data in one operation.</span></span><br/>                   |
| [<span data-ttu-id="40763-119">Leeren von System-Buffered e/a-Daten auf den Datenträger</span><span class="sxs-lookup"><span data-stu-id="40763-119">Flushing System-Buffered I/O Data to Disk</span></span>](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | <span data-ttu-id="40763-120">Windows speichert die Daten in Datei Lese-und Schreibvorgängen in vom System verwalteten Daten Puffern, um die Datenträger Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="40763-120">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span><br/> |
| [<span data-ttu-id="40763-121">Abschneiden oder Erweitern von Dateien</span><span class="sxs-lookup"><span data-stu-id="40763-121">Truncating or Extending Files</span></span>](truncating-or-extending-files.md)<br/>                                                                   | <span data-ttu-id="40763-122">Eine Anwendung kann eine Datei durch Aufrufen von [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)abschneiden oder erweitern.</span><span class="sxs-lookup"><span data-stu-id="40763-122">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span><br/>                             |



 

 

 




