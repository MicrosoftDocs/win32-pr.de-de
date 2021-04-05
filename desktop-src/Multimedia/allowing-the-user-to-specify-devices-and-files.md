---
title: Zulassen der Angabe von Geräten und Dateien durch den Benutzer
description: Zulassen der Angabe von Geräten und Dateien durch den Benutzer
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- Mciwndopendialog-Makro
- Mciwndopen-Makro
- Mciwndopeninterface-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710985"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Zulassen der Angabe von Geräten und Dateien durch den Benutzer

Mithilfe der Makros [**mciwndopendialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)und [**mciwndopeninterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) und der [**getopenfileamepreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) -Funktion können Sie ein Gerät oder eine Datei mit einem vorhandenen mciwnd-Fenster verknüpfen.

Verwenden Sie **mciwndopendialog**, damit ein Benutzer Ihrer Anwendung eine wieder zugebende Datei auswählen kann. Dieses Makro zeigt das Dialogfeld **Öffnen** (im folgenden Screenshot gezeigt) zum Auswählen einer Datei an und ordnet die ausgewählte Datei dem aktuellen mciwnd-Fenster zu.

![Bild des mciwnd-Fensters](images/mciwnd3.gif)

Sie können einem Benutzer Ihrer Anwendung gestatten, eine Datei auszuwählen, die einem mciwnd-Fenster zugeordnet werden soll, und die Datei mithilfe von [**getopenfileamepreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) und [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)in einer Vorschau anzeigen. Die Funktion **getopenfileamepreview** zeigt das Dialogfeld **Öffnen** zum Auswählen einer Datei an und ermöglicht dem Benutzer, seinen Inhalt anzuzeigen (wiederzugeben). Wenn der Name einer vorhandenen Datei im Dialogfeld angegeben wird, stellt **getopenfileamepreview** ein kleines Steuerelement bereit, damit der Benutzer den Inhalt der Datei in der Vorschau anzeigen kann. Mithilfe von **mciwndopen** können Sie eine angegebene, mit **getopenfileamepreview** ausgewählte oder auf andere Weise angegebene Datei mit einem mciwnd-Fenster verknüpfen.

Sie können auch **mciwndopen** verwenden, um ein Gerät anzugeben, das einem mciwnd-Fenster zugeordnet werden soll. Beispielsweise können Sie einen Gerätenamen verwenden, z. b. "CDAudio".

Verwenden Sie das [**mciwndopeninterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) -Makro, um Multimediadaten ein mciwnd-Fenster mit einer Datei Schnittstelle oder einer Datenstrom Schnittstelle zuzuordnen. Weitere Informationen zu Datei-und Datenstrom Schnittstellen finden Sie unter [avifile-Funktionen und-Makros](avifile-functions-and-macros.md).

> [!Note]  
> Vor dem Zuordnen einer neuen Datei oder eines Geräts zu einem mciwnd-Fenster schließen [**mciwndopendialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) und [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) alle Geräte, die derzeit dem Fenster zugeordnet sind. Die Anwendung muss keine geöffneten Geräte schließen, bevor Sie diese Makros verwenden können.

 

 

 




