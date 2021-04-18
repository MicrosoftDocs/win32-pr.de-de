---
title: Informationen zu Multimedia-Datei-e/a
description: Informationen zu Multimedia-Datei-e/a
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows-Multimedia, Datei-e/a
- Multimedia, Datei-e/a
- Multimedia-Eingabe, Datei-e/a
- Multimedia-Datei-e/a, Informationen
- Datei-e/a, Informationen
- Eingabe und Ausgabe (e/a), Informationen zu
- E/a (Eingabe und Ausgabe), Informationen zu
- grundlegende e/a
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340833"
---
# <a name="about-multimedia-file-io"></a><span data-ttu-id="f1d71-114">Informationen zu Multimedia-Datei-e/a</span><span class="sxs-lookup"><span data-stu-id="f1d71-114">About Multimedia File I/O</span></span>

<span data-ttu-id="f1d71-115">Die meisten Multimedia-Anwendungen erfordern Datei Eingaben und-Ausgaben (e/a) – d. h. die Fähigkeit, Datenträger Dateien zu erstellen, zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f1d71-115">Most multimedia applications require file input and output (I/O) — that is, the ability to create, read, and write disk files.</span></span> <span data-ttu-id="f1d71-116">Multimedia-Datei-e/a-Dienste bieten gepufferte und nicht gepufferte Datei-e/a und Unterstützung für Riff-Dateien.</span><span class="sxs-lookup"><span data-stu-id="f1d71-116">Multimedia file I/O services provide buffered and unbuffered file I/O and support for RIFF files.</span></span> <span data-ttu-id="f1d71-117">Die Dienste können durch benutzerdefinierte e/a-Prozeduren erweitert werden, die von den Anwendungen gemeinsam genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="f1d71-117">The services are extensible with custom I/O procedures that can be shared among applications.</span></span>

<span data-ttu-id="f1d71-118">Die meisten Anwendungen benötigen nur die grundlegenden Datei-e/a-Dienste und die Datei-e/a-Dienste von Riff Dateien.</span><span class="sxs-lookup"><span data-stu-id="f1d71-118">Most applications need only the basic file I/O services and the RIFF file I/O services.</span></span> <span data-ttu-id="f1d71-119">Anwendungen, die für die Datei-e/a-Leistung sensibel sind, z. b. Anwendungen, die Daten aus Compact Disk in Echtzeit streamen, können die Leistung optimieren, indem Sie Dienste direkt auf den Datei-e/a-Puffer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f1d71-119">Applications sensitive to file I/O performance, such as applications that stream data from compact disc in real time, can optimize performance by using services to directly access the file I/O buffer.</span></span> <span data-ttu-id="f1d71-120">Anwendungen, die auf benutzerdefinierte Speichersysteme (z. b. Dateiarchive und Datenbanken) zugreifen, können Ihre eigene e/a-Prozedur bereitstellen, mit der Elemente des Speichersystems gelesen und geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f1d71-120">Applications that access custom storage systems, such as file archives and databases, can provide their own I/O procedure that reads and writes elements of the storage system.</span></span>

 

 




