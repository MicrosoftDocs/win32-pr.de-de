---
title: Benutzern das Angeben von Geräten und Dateien gestatten
description: Benutzern das Angeben von Geräten und Dateien gestatten
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog-Makro
- MCIWndOpen-Makro
- MCIWndOpenInterface-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9e388e4b7998a932cb22545c05509277f1f7fa705a81fbde02d4d5fb35cdd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786264"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Benutzern das Angeben von Geräten und Dateien gestatten

Sie können ein Gerät oder eine Datei einem vorhandenen MCIWnd-Fenster zuordnen, indem Sie die Makros [**MCIWndOpenDialog,**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)und [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) sowie die [**GetOpenFileNamePreview-Funktion**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) verwenden.

Verwenden Sie **MCIWndOpenDialog,** damit ein Benutzer Ihrer Anwendung eine Datei für die Wiedergabe auswählen kann. Dieses Makro zeigt das Dialogfeld **Öffnen** (im folgenden Screenshot gezeigt) zum Auswählen einer Datei an und ordnet die ausgewählte Datei dem aktuellen MCIWnd-Fenster zu.

![Bild des mciwnd-Fensters](images/mciwnd3.gif)

Sie können es einem Benutzer Ihrer Anwendung erlauben, eine Datei auszuwählen, die einem MCIWnd-Fenster zugeordnet werden soll, und eine Vorschau dieser Datei mit [**getOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) und [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)anzeigen. Die **GetOpenFileNamePreview-Funktion** zeigt das Dialogfeld **Öffnen** zum Auswählen einer Datei an und ermöglicht dem Benutzer die Vorschau (Wiedergabe) des Inhalts. Wenn der Name einer vorhandenen Datei im Dialogfeld angegeben wird, stellt **GetOpenFileNamePreview** ein kleines Steuerelement bereit, mit dem der Benutzer eine Vorschau der Inhalte der Datei anzeigen kann. Sie können eine angegebene Datei, die mit **GetOpenFileNamePreview** ausgewählt oder auf andere Weise angegeben wurde, einem MCIWnd-Fenster mithilfe von **MCIWndOpen** zuordnen.

Sie können auch **MCIWndOpen** verwenden, um ein Gerät anzugeben, das einem MCIWnd-Fenster zugeordnet werden soll. Beispielsweise können Sie einen Gerätenamen wie "CDAudio" verwenden.

Verwenden Sie das [**MCIWndOpenInterface-Makro,**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) um ein MCIWnd-Fenster einer Dateischnittstelle oder einer Datenstromschnittstelle zu Multimediadaten zuzuordnen. Weitere Informationen zu Datei- und Datenstromschnittstellen finden Sie unter [AVIFile Functions and Macros](avifile-functions-and-macros.md).

> [!Note]  
> Bevor Sie eine neue Datei oder ein neues Gerät einem MCIWnd-Fenster zuordnen, schließen [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) und [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) alle Geräte, die dem Fenster derzeit zugeordnet sind. Ihre Anwendung muss keine geöffneten Geräte schließen, bevor diese Makros verwendet werden.

 

 

 




