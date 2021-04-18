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
# <a name="decompressing-a-single-file"></a>Dekomprimieren einer einzelnen Datei

Eine Anwendung kann eine einzelne komprimierte Datei dekomprimieren, indem Sie die folgenden Aufgaben ausführt:

1.  Öffnen Sie die Quelldatei, indem Sie die [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) -Funktion aufrufen.
2.  Öffnen Sie die Zieldatei durch Aufrufen von [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Kopieren Sie die Quelldatei in die Zieldatei, indem Sie die [**lzcopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) -Funktion aufrufen und die von [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)zurückgegebenen Handles übergeben.
4.  Schließen Sie die Dateien, indem Sie die [**lzclose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) -Funktion aufrufen.

 

 



