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
# <a name="decompressing-multiple-files"></a>Dekomprimieren mehrerer Dateien

Eine Anwendung kann mehrere Dateien dekomprimieren, indem Sie die folgenden Aufgaben ausführt:

1.  Öffnen Sie die Quelldateien, indem Sie die [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) -Funktion aufrufen.
2.  Öffnen Sie die Zieldateien durch Aufrufen von [**lzopenfile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Kopieren Sie die Quelldateien in die Zieldateien, indem Sie die [**lzcopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) -Funktion aufrufen.
4.  Schließen Sie die Dateien, indem Sie die [**lzclose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) -Funktion aufrufen.

 

 



