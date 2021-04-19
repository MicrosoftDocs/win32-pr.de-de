---
description: Eine Anwendung kann eine komprimierte Datei Teil Weise dekomprimieren, indem Sie die lzseek-und lzread-Funktionen verwendet.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lesen aus komprimierten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350380"
---
# <a name="reading-from-compressed-files"></a><span data-ttu-id="62c5c-103">Lesen aus komprimierten Dateien</span><span class="sxs-lookup"><span data-stu-id="62c5c-103">Reading from Compressed Files</span></span>

<span data-ttu-id="62c5c-104">Zusätzlich zur Dekomprimierung einer kompletten Datei in einem einzelnen Vorgang kann eine Anwendung eine komprimierte Datei einzeln dekomprimieren, indem Sie die [**lzseek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) -und [**lzread**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) -Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="62c5c-104">In addition to decompressing a complete file in a single operation, an application can decompress a compressed file a portion at a time by using the [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) and [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) functions.</span></span> <span data-ttu-id="62c5c-105">Diese Funktionen sind besonders nützlich, wenn es erforderlich ist, Teile großer Dateien zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="62c5c-105">These functions are particularly useful when it is necessary to extract parts of large files.</span></span> <span data-ttu-id="62c5c-106">Beispielsweise kann ein Schriftart Hersteller neben Zeichendaten auch komprimierte Dateien mit Schriftart Metrik enthalten.</span><span class="sxs-lookup"><span data-stu-id="62c5c-106">For example, a font manufacturer may have compressed files containing font metrics in addition to character data.</span></span> <span data-ttu-id="62c5c-107">Um die Informationen in diesen Dateien zu verwenden, muss eine Anwendung die Datei dekomprimieren. die meisten Anwendungen verwenden allerdings nur einen Teil der Datei zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="62c5c-107">To use the information in these files, an application would need to decompress the file; however, most applications would use only part of the file at any particular time.</span></span> <span data-ttu-id="62c5c-108">Um Informationen über Schriftart Metriken zu erhalten, extrahiert die Anwendung Daten aus dem-Header.</span><span class="sxs-lookup"><span data-stu-id="62c5c-108">To get information about font metrics, the application would extract data from the header.</span></span> <span data-ttu-id="62c5c-109">Zum Abrufen von Informationen aus dem Text würde die Anwendung den Dateizeiger neu positionieren, indem **lzseek** aufgerufen und Zeichendaten durch Aufrufen von **lzread** extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="62c5c-109">To get information from the text, the application would reposition the file pointer by calling **LZSeek** and extract character data by calling **LZRead**.</span></span>

 

 



