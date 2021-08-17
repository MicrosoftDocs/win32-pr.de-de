---
description: Eine Anwendung kann eine einzelne komprimierte Datei mithilfe der Funktionen LZOpenFile, LZCopy und LZClose dekomprimieren.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Dekomprimieren einer einzelnen Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99152a36a2846bfe35a9d92bc3d8fd2eb6b5c3a7f0877179262801a9141bcc61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150836"
---
# <a name="decompressing-a-single-file"></a>Dekomprimieren einer einzelnen Datei

Eine Anwendung kann eine einzelne komprimierte Datei dekomprimieren, indem sie die folgenden Aufgaben ausführen:

1.  Öffnen Sie die Quelldatei, indem Sie die [**LZOpenFile-Funktion**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) aufrufen.
2.  Öffnen Sie die Zieldatei, indem Sie [**LZOpenFile aufrufen.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)
3.  Kopieren Sie die Quelldatei in die Zieldatei, indem Sie die [**LZCopy-Funktion**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) aufrufen und die von [**LZOpenFile zurückgegebenen**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)Handles übergeben.
4.  Schließen Sie die Dateien, indem Sie die [**LZClose-Funktion**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) aufrufen.

 

 



