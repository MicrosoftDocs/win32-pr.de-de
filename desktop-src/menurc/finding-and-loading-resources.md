---
title: Suchen und Laden von Ressourcen
description: In diesem Thema wird erläutert, wie eine Ressource in den Arbeitsspeicher geladen wird.
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca9590927cad28772a6b4a5b761d74c9ebf101a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472828"
---
# <a name="finding-and-loading-resources"></a>Suchen und Laden von Ressourcen

Vor der Verwendung einer Ressource muss Sie von einer Anwendung in den Arbeitsspeicher geladen werden. Die Funktionen " [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) " und " [**findresourceex**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa) " suchen eine Ressource in einem Modul und geben ein Handle für die binären Ressourcen Daten zurück. **FindResource** sucht eine Ressource nach Typ und Namen. **Findresourceex** sucht die Ressource nach Typ, Name und Sprache. Informationen zu **FindResource** in diesem Thema gelten auch für **findresourceex**.

Die [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) -Funktion verwendet das von [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) zurückgegebene Ressourcen handle, um die Ressource in den Arbeitsspeicher zu laden. Nachdem eine Anwendung eine Ressource mithilfe von " **LoadResource**" geladen hat, wird der zugeordnete Speicher nur entladen, wenn alle Verweise auf das Modul über " [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary)" freigegeben werden. Anwendungen, die wiederholt auf dieselbe oder viele Ressourcen innerhalb eines bestimmten Moduls zugreifen müssen, können aufgrund der Speicher Zuordnung, die in wiederholten [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -und **FreeLibrary** -aufrufen stattfindet, zu Leistungseinbußen kommen. Anwendungen sollten ein einzelnes Modul handle speichern, bis Ressourcen nicht mehr benötigt werden, und dann **FreeLibrary** aufgerufen wird. Nachdem ein Modul aus dem Arbeitsspeicher entladen wurde, werden die Ressourcen Handles ungültig.

Eine Anwendung kann [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) und [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) verwenden, um beliebige Ressourcentypen zu suchen und zu laden. diese Funktionen sollten jedoch nur in einer der folgenden Situationen verwendet werden:

-   Wenn die Anwendung nicht mithilfe einer vorhandenen Ressourcen spezifischen Funktion auf die Ressource zugreifen kann.
-   Wenn die Anwendung auf die Ressource als Binärdaten für nachfolgende Funktionsaufrufe zugreifen muss.

Eine Anwendung sollte, wenn möglich, stattdessen eine der folgenden Ressourcen spezifischen Funktionen verwenden, um Ressourcen in einem Aufruf zu suchen und zu laden:



| Funktion                                     | Aktion                                   | So entfernen Sie die Ressource                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**Format Message**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | Lädt und formatiert einen Nachrichten Tabelleneintrag. | Keine Aktion erforderlich.                                                                                                |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | Lädt eine Zugriffstasten Tabelle.              | [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | Lädt eine Bitmap-Ressource.                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | Lädt eine Cursor Ressource.                 | [**Destroycursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | Lädt eine Symbol Ressource.                  | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | Lädt ein Symbol, einen Cursor oder eine Bitmap.        | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon), [**destroycursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor), [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**Loadmenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | Lädt eine Menü Ressource.                   | [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | Lädt einen Zeichen folgen Tabelleneintrag.              | Keine Aktion erforderlich.                                                                                                |



 

Beachten Sie die releasefunktionen in der obigen Tabelle. Vor dem beenden sollte eine Anwendung den von Zugriffstasten Tabellen, Bitmaps, Cursorn, Symbolen und Menüs belegten Speicher mithilfe der entsprechenden Funktionen freigeben.

Der Arbeitsspeicher, der mit den durch [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) und [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) geladenen Ressourcen verknüpft ist, wird freigegeben, sobald das Modul durch einen Befehl von " [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary)" entladen wurde. Alle Ressourcen, die beim Beenden der Anwendung entladen bleiben, werden automatisch vom System freigegeben.

 

 