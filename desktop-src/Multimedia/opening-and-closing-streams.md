---
title: Öffnende und schließende Streams
description: Öffnende und schließende Streams
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream-Funktion
- AVIStreamRelease-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35f678f2858d590956bc3ba724abacd12d2047e337fc8428934e0e32005bb24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038310"
---
# <a name="opening-and-closing-streams"></a>Öffnende und schließende Streams

Das Öffnen von Datenströmen ähnelt dem Öffnen von Dateien. Sie können einen Stream mithilfe der [**FUNKTION AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) öffnen. Diese Funktion erstellt eine Streamschnittstelle, platziert ein Handle des Streams in der Schnittstelle und gibt einen Zeiger auf die Schnittstelle zurück. **AVIFileGetStream** verwaltet auch eine Verweisanzahl der Anwendungen, die einen Stream geöffnet haben, aber nicht diejenigen, die ihn geschlossen haben.

Wenn Sie auf einen einzelnen Stream in einer Datei zugreifen möchten, können Sie die Datei und den Stream mithilfe der [**FUNKTION AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) öffnen. Diese Funktion kombiniert die Vorgänge und Funktionsargumente der [**FUNKTIONEN AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) und **AVIFileGetStream.**

Um auf mehr als einen Stream in einer Datei zu zugreifen, verwenden Sie **AVIFileOpen** einmal gefolgt von mehreren Aufrufen von **AVIFileGetStream**.

Sie können die Verweisanzahl eines Streams erhöhen, indem Sie die [**FUNKTION AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) verwenden, um einen Stream geöffnet zu lassen, wenn Sie eine Funktion verwenden, die den Stream normalerweise schließt.

Sie können einen Stream mithilfe der [**FUNKTION AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) schließen. Diese Funktion dekrementiert den Verweiszähler des Streams und schließt ihn, wenn der Verweiszähler null erreicht. Ihre Anwendungen sollten den Verweiszähler ausgleichen, indem sie einen Aufruf von **AVIStreamRelease** für jede Verwendung der [**AVIFileGetStream-,**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) [**AVIFileCreateStream-,**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) **AVIStreamAddRef-** oder **AVIStreamOpenFromFile-Funktion** enthalten. Wenn Sie einen Stream veröffentlichen, der mitHILFE von **AVIStreamOpenFromFile geöffnet** wurde, schließt AVIFile die Datei, die den Stream enthält. Wenn Ihre Anwendung eine Datei mit geöffneten Datenströmen frei gibt, schließt AVIFile die Datenströme erst, wenn alle Streams freigegeben wurden.

 

 




