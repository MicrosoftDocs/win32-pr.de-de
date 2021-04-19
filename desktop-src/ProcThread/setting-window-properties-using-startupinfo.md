---
description: Ein übergeordneter Prozess kann Eigenschaften angeben, die dem Hauptfenster des untergeordneten Prozesses zugeordnet sind.
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: Festlegen von Fenster Eigenschaften mithilfe von STARTUPINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff59f9ae4473174325880a863f5b1f2fc4203e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359033"
---
# <a name="setting-window-properties-using-startupinfo"></a>Festlegen von Fenster Eigenschaften mithilfe von STARTUPINFO

Ein übergeordneter Prozess kann Eigenschaften angeben, die dem Hauptfenster des untergeordneten Prozesses zugeordnet sind. Die Funktion " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " übernimmt einen Zeiger auf eine [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur als einen ihrer Parameter. Verwenden Sie die Elemente dieser Struktur, um die Eigenschaften des Hauptfensters des untergeordneten Prozesses anzugeben. Der **dwFlags** -Member enthält ein Bitfeld, das bestimmt, welche anderen Member der Struktur verwendet werden. Auf diese Weise können Sie Werte für eine beliebige Teilmenge der Fenster Eigenschaften angeben. Das System verwendet die Standardwerte für die Eigenschaften, die Sie nicht angeben. Der **dwFlags** -Member kann auch erzwingen, dass während der Initialisierung des neuen Prozesses ein Feedback Cursor angezeigt wird.

Für GUI-Prozesse gibt die [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur die Standardwerte an, die verwendet werden sollen, wenn der neue Prozess zum ersten Mal die Funktionen " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " und " [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) " aufruft, um ein überlappendes Fenster zu erstellen und anzuzeigen. Die folgenden Standardwerte können angegeben werden:

-   Die Breite und Höhe des Fensters, das von " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)" erstellt wurde.
-   Die Position in Bildschirm Koordinaten des Fensters, das von " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)" erstellt wurde.
-   Der *nCmdShow* -Parameter von [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).

Verwenden Sie für Konsolen Prozesse die [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur, um Fenster Eigenschaften nur beim Erstellen einer neuen Konsole (entweder [**mithilfe von**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) "Create \_ New Console" \_ oder mit der Funktion " [**Zuordnungs Konsole**](/windows/console/allocconsole) ") anzugeben. Die **STARTUPINFO** -Struktur kann verwendet werden, um die folgenden Eigenschaften des Konsolenfensters anzugeben:

-   Die Größe des neuen Konsolenfensters in Zeichen Zellen.
-   Der Speicherort des neuen Konsolenfensters in Bildschirm Koordinaten.
-   Die Größe des Bildschirm Puffers der neuen Konsole in Zeichen Zellen.
-   Die Text-und Hintergrundfarben Attribute des Bildschirm Puffers der neuen Konsole.
-   Der Titel des Fensters der neuen Konsole.

 

 
