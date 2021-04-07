---
title: Benutzerdefinierte Dienste
description: Benutzerdefinierte Dienste
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- Multimedia-Datei-e/a, benutzerdefinierte Dienste
- Datei-e/a, benutzerdefinierte Dienste
- Eingabe und Ausgabe (e/a), benutzerdefinierte Dienste
- E/a (Eingabe und Ausgabe), benutzerdefinierte Dienste
- benutzerdefinierte e/a
- mmioinstallioproc-Funktion
- mmioopen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038943"
---
# <a name="custom-services"></a><span data-ttu-id="45a05-110">Benutzerdefinierte Dienste</span><span class="sxs-lookup"><span data-stu-id="45a05-110">Custom Services</span></span>

<span data-ttu-id="45a05-111">Multimedia-Datei-e/a-Dienste verwenden e/a-Prozeduren, um die physische Eingabe und Ausgabe zu verarbeiten, die dem Lesen und Schreiben in verschiedene Typen von Speichersystemen zugeordnet sind, z. b. Datei Archivierungssysteme und Daten Bank Speicher</span><span class="sxs-lookup"><span data-stu-id="45a05-111">Multimedia file I/O services use I/O procedures to handle the physical input and output associated with reading and writing to different types of storage systems, such as file-archival systems and database-storage systems.</span></span> <span data-ttu-id="45a05-112">Vordefinierte e/a-Prozeduren sind für die Standarddatei Systeme und für Speicherdateien vorhanden, Sie können jedoch eine benutzerdefinierte e/a-Prozedur für den Zugriff auf ein eindeutiges Speichersystem mithilfe der [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) -Funktion bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="45a05-112">Predefined I/O procedures exist for the standard file systems and for memory files, but you can supply a custom I/O procedure for accessing a unique storage system by using the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function.</span></span>

<span data-ttu-id="45a05-113">Verwenden Sie zum Öffnen einer Datei mit einer benutzerdefinierten e/a-Prozedur die [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="45a05-113">To open a file by using a custom I/O procedure, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="45a05-114">Fügen Sie ein Pluszeichen (+) oder die cfsepchar-Konstante in den Dateinamen ein, um den Namen der physischen Datei von dem Namen des Elements der Datei zu trennen, die Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="45a05-114">Include a plus sign (+) or the CFSEPCHAR constant in the filename to separate the name of the physical file from the name of the element of the file you want to open.</span></span> <span data-ttu-id="45a05-115">Im folgenden Beispiel wird ein Datei Element mit dem Namen "Element" aus der Datei "filename" geöffnet. Bogen</span><span class="sxs-lookup"><span data-stu-id="45a05-115">The following example opens a file element named "element" from a file named FILENAME.ARC:</span></span>


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



<span data-ttu-id="45a05-116">Wenn der Datei-e/a-Manager ein Pluszeichen in einem Dateinamen erkennt, wird die Dateinamenerweiterung untersucht, um zu bestimmen, welche e/a-Prozedur der Datei zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45a05-116">When the file I/O manager encounters a plus sign in a filename, it examines the filename extension to determine which I/O procedure to associate with the file.</span></span> <span data-ttu-id="45a05-117">Im vorherigen Beispiel hat der Datei-e/a-Manager versucht, die e/a-Prozedur zu verwenden, die dem zugeordnet ist. Dateinamenerweiterung des Bogens; Diese e/a-Prozedur wurde mithilfe von [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)installiert.</span><span class="sxs-lookup"><span data-stu-id="45a05-117">In the previous example, the file I/O manager would attempt to use the I/O procedure associated with the .ARC filename extension; this I/O procedure would have been installed by using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span></span> <span data-ttu-id="45a05-118">Wenn keine e/a-Prozedur installiert ist, gibt [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="45a05-118">If no I/O procedure is installed, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) returns an error.</span></span>

<span data-ttu-id="45a05-119">E/a-Prozeduren müssen auf die folgenden Meldungen Antworten:</span><span class="sxs-lookup"><span data-stu-id="45a05-119">I/O procedures must respond to the following messages:</span></span>

-   [<span data-ttu-id="45a05-120">**mmiom \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="45a05-120">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="45a05-121">**mmiom \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="45a05-121">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="45a05-122">**mmiom- \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="45a05-122">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="45a05-123">**mmiom- \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="45a05-123">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="45a05-124">**mmiom- \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="45a05-124">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="45a05-125">**Umbenennen von mmiom \_**</span><span class="sxs-lookup"><span data-stu-id="45a05-125">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="45a05-126">**mmiom- \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="45a05-126">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)

<span data-ttu-id="45a05-127">Sie können auch benutzerdefinierte Nachrichten erstellen und Sie mithilfe der [**mmiosendmessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) -Funktion an Ihre e/a-Prozedur senden.</span><span class="sxs-lookup"><span data-stu-id="45a05-127">You can also create custom messages and send them to your I/O procedure by using the [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) function.</span></span> <span data-ttu-id="45a05-128">Wenn Sie Ihre eigenen Nachrichten definieren, stellen Sie sicher, dass Sie mit dem durch die mmiom-Benutzer Konstante definierten Wert definiert oder überschritten werden \_ .</span><span class="sxs-lookup"><span data-stu-id="45a05-128">If you define your own messages, make sure they are defined at or above the value defined by the MMIOM\_USER constant.</span></span>

<span data-ttu-id="45a05-129">Zusätzlich zum Verarbeiten von Nachrichten muss ein e/a-Vorgang das **ldiskoffset** -Element der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur beibehalten (auf den der *lpmmioinfo* -Parameter der **mmioopen** -Funktion verweist).</span><span class="sxs-lookup"><span data-stu-id="45a05-129">In addition to processing messages, an I/O procedure must maintain the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure (pointed to by the *lpmmioinfo* parameter of the **mmioOpen** function).</span></span> <span data-ttu-id="45a05-130">Der **ldiskoffset** -Member muss immer den Dateioffset an dem Speicherort enthalten, auf den die nächste mmiom- \_ Lese-oder mmiom- \_ Schreib Nachricht zugreift.</span><span class="sxs-lookup"><span data-stu-id="45a05-130">The **lDiskOffset** member must always contain the file offset to the location that the next MMIOM\_READ or MMIOM\_WRITE message will access.</span></span> <span data-ttu-id="45a05-131">Der Offset wird in Bytes angegeben und ist relativ zum Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="45a05-131">The offset is specified in bytes and is relative to the beginning of the file.</span></span> <span data-ttu-id="45a05-132">Die e/a-Prozedur kann den **adwinfo** -Member verwenden, um alle erforderlichen Zustandsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="45a05-132">The I/O procedure can use the **adwInfo** member to maintain any required state information.</span></span> <span data-ttu-id="45a05-133">Die e/a-Prozedur sollte keine anderen Member in der **mmioinfo** -Struktur ändern.</span><span class="sxs-lookup"><span data-stu-id="45a05-133">The I/O procedure should not modify any other members in the **MMIOINFO** structure.</span></span>

 

 