---
description: Eine Anwendung kann mehrere Dateien mithilfe der Funktionen lzopenfile, lzcopy und lzclose dekomprimieren.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Dekomprimieren mehrerer Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354612"
---
# <a name="decompressing-multiple-files"></a><span data-ttu-id="a5089-103">Dekomprimieren mehrerer Dateien</span><span class="sxs-lookup"><span data-stu-id="a5089-103">Decompressing Multiple Files</span></span>

<span data-ttu-id="a5089-104">Eine Anwendung kann mehrere Dateien dekomprimieren, indem Sie die folgenden Aufgaben ausführt:</span><span class="sxs-lookup"><span data-stu-id="a5089-104">An application can decompress multiple files by performing the following tasks:</span></span>

1.  <span data-ttu-id="a5089-105">Öffnen Sie die Quelldateien, indem Sie die [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5089-105">Open the source files by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="a5089-106">Öffnen Sie die Zieldateien durch Aufrufen von [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="a5089-106">Open the destination files by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="a5089-107">Kopieren Sie die Quelldateien in die Zieldateien, indem Sie die [**lzcopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5089-107">Copy the source files to the destination files by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function.</span></span>
4.  <span data-ttu-id="a5089-108">Schließen Sie die Dateien, indem Sie die [**lzclose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5089-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



