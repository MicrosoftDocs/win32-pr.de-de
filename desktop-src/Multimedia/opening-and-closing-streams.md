---
title: Öffnen und Schließen von Streams
description: Öffnen und Schließen von Streams
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream-Funktion
- Avistreamrelease-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036678"
---
# <a name="opening-and-closing-streams"></a>Öffnen und Schließen von Streams

Das Öffnen von Datenströmen ähnelt dem Öffnen von Dateien. Sie können einen Stream mithilfe der [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) -Funktion öffnen. Diese Funktion erstellt eine Datenstrom Schnittstelle, platziert ein Handle des Streams in der-Schnittstelle und gibt einen Zeiger auf die-Schnittstelle zurück. **AVIFileGetStream** verwaltet auch den Verweis Zähler der Anwendungen, die einen Stream geöffnet haben, jedoch nicht von den Anwendungen, die ihn geschlossen haben.

Wenn Sie auf einen einzelnen Datenstrom in einer Datei zugreifen möchten, können Sie die Datei und den Datenstrom mithilfe der [**avistreamopenfromfile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) -Funktion öffnen. Diese Funktion kombiniert die Vorgänge und Funktionsargumente der Funktionen [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) und **AVIFileGetStream** .

Wenn Sie auf mehr als einen Stream in einer Datei zugreifen möchten, verwenden Sie **AVIFileOpen** , gefolgt von mehreren Aufrufen von **AVIFileGetStream**.

Sie können den Verweis Zähler eines Streams erhöhen, indem Sie die [**avistreamadref**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) -Funktion verwenden, um einen Datenstrom geöffnet zu lassen, wenn Sie eine Funktion verwenden, die normalerweise den Datenstrom schließt.

Sie können einen Stream mit der [**avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) -Funktion schließen. Diese Funktion Dekremente den Verweis Zähler des Streams und schließt diese, wenn der Verweis Zähler Null erreicht. Ihre Anwendungen sollten den Verweis Zähler ausgleichen, indem Sie für jede Verwendung der [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)-, [**avifileforatestream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)-, **avistreamadressf**-oder **avistreamopenfromfile** -Funktion einen **avistreamrelease** -Befehl einschließen. Wenn Sie einen Stream freigeben, der mithilfe von **avistreamopenfromfile** geöffnet wurde, schließt avifile die Datei, die den Datenstrom enthält. Wenn Ihre Anwendung eine Datei mit geöffneten Datenströmen freigibt, schließt avifile die Streams erst, wenn alle Streams freigegeben wurden.

 

 




