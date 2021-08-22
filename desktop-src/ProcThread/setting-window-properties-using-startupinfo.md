---
description: Ein übergeordneter Prozess kann Eigenschaften angeben, die dem Hauptfenster des untergeordneten Prozesses zugeordnet sind.
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: Festlegen von Fenstereigenschaften mit STARTUPINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637e8fc9c76694a468b4b8fa6d5d2bd8a3432bbb7dad078d616df753244af358
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517380"
---
# <a name="setting-window-properties-using-startupinfo"></a>Festlegen von Fenstereigenschaften mit STARTUPINFO

Ein übergeordneter Prozess kann Eigenschaften angeben, die dem Hauptfenster des untergeordneten Prozesses zugeordnet sind. Die [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) verwendet einen Zeiger auf eine [**STARTUPINFO-Struktur**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) als einen ihrer Parameter. Verwenden Sie die Member dieser Struktur, um Merkmale des Hauptfensters des untergeordneten Prozesses anzugeben. Der **dwFlags-Member** enthält ein Bitfeld, das bestimmt, welche anderen Member der -Struktur verwendet werden. Dadurch können Sie Werte für eine beliebige Teilmenge der Fenstereigenschaften angeben. Das System verwendet Standardwerte für die Eigenschaften, die Sie nicht angeben. Der **dwFlags-Member** kann auch erzwingen, dass während der Initialisierung des neuen Prozesses ein Feedbackcursor angezeigt wird.

Bei GUI-Prozessen gibt die [**STARTUPINFO-Struktur**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) die Standardwerte an, die verwendet werden sollen, wenn der neue Prozess zum ersten Mal die Funktionen [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) und [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) aufruft, um ein überlappendes Fenster zu erstellen und anzuzeigen. Die folgenden Standardwerte können angegeben werden:

-   Die Breite und Höhe des von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)erstellten Fensters in Pixel.
-   Die Position in Bildschirmkoordinaten des fensters, das von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)erstellt wurde.
-   Der *nCmdShow-Parameter* von [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).

Verwenden Sie für Konsolenprozesse die [**STARTUPINFO-Struktur,**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) um Fenstereigenschaften nur beim Erstellen einer neuen Konsole anzugeben (entweder mit [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) mit CREATE \_ NEW CONSOLE oder mit der \_ [**AllocConsole-Funktion).**](/windows/console/allocconsole) Die **STARTUPINFO-Struktur** kann verwendet werden, um die folgenden Eigenschaften des Konsolenfensters anzugeben:

-   Die Größe des neuen Konsolenfensters in Zeichenzellen.
-   Die Position des neuen Konsolenfensters in Bildschirmkoordinaten.
-   Die Größe des Bildschirmpuffers der neuen Konsole in Zeichenzellen.
-   Die Text- und Hintergrundfarbattribute des Bildschirmpuffers der neuen Konsole.
-   Der Titel des Fensters der neuen Konsole.

 

 
