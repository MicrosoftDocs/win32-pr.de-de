---
description: In diesem Thema werden die Haupt Programmierungs Elemente aufgelistet, die mit Kontextmenüs (Kontextmenüs) und Kontextmenü Handlern verwendet werden. Kontextmenü Handler, die auch als Kontextmenü Handler oder Verb Handler bezeichnet werden, sind ein Dateityp Handler.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Verweis auf das Kontextmenü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb1552c8f2f383b08984e9142e464b6831a3c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214438"
---
# <a name="shortcut-menu-reference"></a>Verweis auf das Kontextmenü

In diesem Thema werden die Haupt Programmierungs Elemente aufgelistet, die mit Kontextmenüs (Kontextmenüs) und Kontextmenü Handlern verwendet werden. Kontextmenü Handler, die auch als Kontextmenü Handler oder Verb Handler bezeichnet werden, sind ein Dateityp Handler.

## <a name="about-shortcut-menu-implemetation"></a>Informationen zum Kontextmenü "Implementierung"

Es wird dringend empfohlen, dass Sie ein Kontextmenü mit einer der statischen Verb-Methoden implementieren. Lesen Sie die folgenden Anweisungen:

-   Informationen zum Verwenden einer statischen Verb-Methode zum Implementieren eines Kontextmenüs finden Sie im Abschnitt "Anpassen eines Kontextmenüs mit statischen Verben" unter Erstellen von Kontext [Menü Handlern](context-menu-handlers.md).
-   Weitere Informationen zum dynamischen Verhalten von statischen Verben in Windows 7 und höher finden Sie unter "Get Dynamic Behavior for static Verbs" unter Erstellen von Kontext [Menü Handlern](context-menu-handlers.md).
-   Ausführliche Informationen über die statische Verb-Implementierung und welche dynamischen Verben zu vermeiden sind, finden [Sie unter Auswählen eines statischen oder dynamischen Verbs für](shortcut-choose-method.md)das Kontextmenü.
-   Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie für den Dateityp ein dynamisches Verb registrieren, befolgen Sie die Anweisungen unter [Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md).

### <a name="interfaces"></a>Schnittstellen



| Thema                                        | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Macht Methoden verfügbar, die ein einem Shellobjekt zugeordnetes Kontextmenü erstellen oder zusammenführen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Macht Methoden verfügbar, die ein Kontextmenü (Kontextmenü) erstellen oder zusammenführen, das einem Shellobjekt zugeordnet ist. Erweitert [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) durch Hinzufügen einer Methode, die es Client Objekten ermöglicht, Nachrichten zu verarbeiten, die mit vom Besitzer gezeichneten Menü Elementen verknüpft sind.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Macht Methoden verfügbar, die ein einem Shellobjekt zugeordnetes Kontextmenü erstellen oder zusammenführen. Ermöglicht Client Objekten das Verarbeiten von Nachrichten, die mit vom Besitzer gezeichneten Menü Elementen verknüpft sind, und erweitert [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) durch akzeptieren eines Rückgabewerts aus der Nachrichtenverarbeitung.<br/>                                                                                                                                                                                                                         |
| [**Icontextmenucb**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Macht eine Methode verfügbar, die den Rückruf eines Kontextmenüs ermöglicht. Beispielsweise, um einem **MenuItem** , das eine Erhöhung erfordert, ein Schild Symbol hinzuzufügen.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**Icontextmenusite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Wird von der Standardordner Ansicht implementiert, die mit [**shkreateshellfolderview**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview)erstellt wurde. Eine-Implementierung von [**icontextmenusite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) unterstützt [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)und [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) sowie alle für diese Funktion erforderlichen Weiterleitungs Weiterleitungs Anforderungen. **Icontextmenusite** aktualisiert in der Regel auch die Statusleiste.<br/> |



 

### <a name="functions"></a>Functions



| Thema                                                            | Inhalte                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Erstellt ein Kontextmenü für eine ausgewählte Gruppe von Datei Ordner Objekten.<br/>                                                          |
| [**Lpfndfmcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Definiert den Prototyp für die Rückruffunktion, mit der Nachrichten aus der standardmäßigen Kontextmenü Implementierung der Shell empfangen werden.<br/> |
| [**Shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Erstellt ein-Objekt, das die standardmäßige Kontextmenü Implementierung der Shell darstellt.<br/>                                           |



 

### <a name="structures"></a>Strukturen



| Thema                                                  | Inhalte                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Enthält Informationen, die von [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) zum Aufrufen eines Kontextmenü Befehls benötigt werden.<br/>                                                             |
| [**Cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Enthält erweiterte Informationen zu einem Kontextmenü Befehl. Bei dieser Struktur handelt es sich um eine erweiterte Version von [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , die die Verwendung von Unicode-Werten ermöglicht.<br/> |
| [**Defcontextmenu**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Enthält Kontextmenü Informationen, die von [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)verwendet werden.<br/>                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontextmenüs und Kontextmenü Handler](context-menu.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben](verbs-best-practices.md)
</dt> <dt>

[Erstellen von Kontextmenü Handlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
