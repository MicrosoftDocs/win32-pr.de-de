---
description: In diesem Thema werden die wichtigsten Programmierelemente aufgeführt, die mit Kontextmenüs und Kontextmenühandlern verwendet werden. Kontextmenühandler, die auch als Kontextmenühandler oder Verbhandler bezeichnet werden, sind ein Typ von Dateityphandler.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Kontextmenüreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f80b62b88750200456da76c22017b3f18fbba584272dc028809771c807ad85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090770"
---
# <a name="shortcut-menu-reference"></a>Kontextmenüreferenz

In diesem Thema werden die wichtigsten Programmierelemente aufgeführt, die mit Kontextmenüs und Kontextmenühandlern verwendet werden. Kontextmenühandler, die auch als Kontextmenühandler oder Verbhandler bezeichnet werden, sind ein Typ von Dateityphandler.

## <a name="about-shortcut-menu-implemetation"></a>Informationen zur Verknüpfungsmenü-Implemetation

Es wird dringend empfohlen, ein Kontextmenü mit einer der statischen Verbmethoden zu implementieren. Lesen Sie die folgenden Anweisungen:

-   Informationen zum Verwenden einer statischen Verbmethode zum Implementieren eines Kontextmenüs finden Sie im Abschnitt "Anpassen eines Kontextmenüs mit statischen Verben" unter [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)
-   Informationen zum Abrufen des dynamischen Verhaltens für statische Verben in Windows 7 und höher finden Sie unter "Getting Dynamic Behavior for Static Verbs" (Abrufen des dynamischen Verhaltens für statische Verben) in [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)
-   Ausführliche Informationen zur Implementierung statischer Verben und zu den zu vermeidenden dynamischen Verben finden Sie unter Auswählen eines statischen oder dynamischen [Verbs für das Kontextmenü.](shortcut-choose-method.md)
-   Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie ein dynamisches Verb für den Dateityp registrieren, befolgen Sie die Anweisungen unter Anpassen eines Kontextmenüs mit dynamischen [Verben.](shortcut-menu-using-dynamic-verbs.md)

### <a name="interfaces"></a>Schnittstellen



| Thema                                        | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Macht Methoden verfügbar, die ein einem Shell-Objekt zugeordnetes Kontextmenü erstellen oder zusammenführen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Macht Methoden verfügbar, die entweder ein Kontextmenü erstellen oder zusammenführen, das einem Shell-Objekt zugeordnet ist. Erweitert [**IContextMenu, indem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) eine Methode hinzugefügt wird, mit der Clientobjekte Nachrichten verarbeiten können, die besitzergezeichneten Menüelementen zugeordnet sind.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Macht Methoden verfügbar, die ein einem Shell-Objekt zugeordnetes Kontextmenü erstellen oder zusammenführen. Ermöglicht Clientobjekten das Verarbeiten von Nachrichten, die besitzergezeichneten Menüelementen zugeordnet sind, und erweitert [**IContextMenu2,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) indem ein Rückgabewert aus dieser Nachrichtenbehandlung akzeptiert wird.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Macht eine Methode verfügbar, die den Rückruf eines Kontextmenüs ermöglicht. Zum Beispiel, um einem **menuItem** ein Schildsymbol hinzuzufügen, für das eine Erhöhung erforderlich ist.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Wird von der Standardordneransicht implementiert, die mit [**SHCreateShellFolderView erstellt wurde.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) Eine Implementierung von [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) unterstützt [**IContextMenu::QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)und [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) sowie jede für diese Funktion erforderliche Nachrichtenweiterleitung. **IContextMenuSite** aktualisiert in der Regel auch die Statusleiste.<br/> |



 

### <a name="functions"></a>Functions



| Thema                                                            | Inhalte                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Erstellt ein Kontextmenü für eine ausgewählte Gruppe von Dateiordnerobjekten.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Definiert den Prototyp für die Rückruffunktion, die Nachrichten von der standardmäßigen Kontextmenüimplementierung der Shell empfängt.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Erstellt ein -Objekt, das die Standardmäßige Kontextmenüimplementierung der Shell darstellt.<br/>                                           |



 

### <a name="structures"></a>Strukturen



| Thema                                                  | Inhalte                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Enthält Informationen, die [**von IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) zum Aufrufen eines Kontextmenübefehls benötigt werden.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Enthält erweiterte Informationen zu einem Kontextmenübefehl. Diese Struktur ist eine erweiterte Version von [**CMINVOKECOMMANDINFO,**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) die die Verwendung von Unicode-Werten ermöglicht.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Enthält Kontextmenüinformationen, die von [**SHCreateDefaultContextMenu verwendet werden.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)<br/>                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontextmenüs und Kontextmenühandler](context-menu.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Bewährte Methoden für Kontextmenühandler und Mehrfachauswahlverben](verbs-best-practices.md)
</dt> <dt>

[Erstellen von Kontextmenühandlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mit dynamischen Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
