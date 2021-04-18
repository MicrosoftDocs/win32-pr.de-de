---
description: Eine Anwendung kann eine einzelne komprimierte Datei dekomprimieren, indem Sie die lzopenfile-, lzcopy-und lzclose-Funktionen verwendet.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Dekomprimieren einer einzelnen Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347900"
---
# <a name="decompressing-a-single-file"></a><span data-ttu-id="096ca-103">Dekomprimieren einer einzelnen Datei</span><span class="sxs-lookup"><span data-stu-id="096ca-103">Decompressing a Single File</span></span>

<span data-ttu-id="096ca-104">Eine Anwendung kann eine einzelne komprimierte Datei dekomprimieren, indem Sie die folgenden Aufgaben ausführt:</span><span class="sxs-lookup"><span data-stu-id="096ca-104">An application can decompress a single compressed file by performing the following tasks:</span></span>

1.  <span data-ttu-id="096ca-105">Öffnen Sie die Quelldatei, indem Sie die [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="096ca-105">Open the source file by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="096ca-106">Öffnen Sie die Zieldatei durch Aufrufen von [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="096ca-106">Open the destination file by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="096ca-107">Kopieren Sie die Quelldatei in die Zieldatei, indem Sie die [**lzcopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) -Funktion aufrufen und die von [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)zurückgegebenen Handles übergeben.</span><span class="sxs-lookup"><span data-stu-id="096ca-107">Copy the source file to the destination file by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function and passing the handles returned by [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
4.  <span data-ttu-id="096ca-108">Schließen Sie die Dateien, indem Sie die [**lzclose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="096ca-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



