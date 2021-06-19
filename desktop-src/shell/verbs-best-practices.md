---
description: Hier finden Sie Informationen zu bewährten Methoden für Kontextmenühandler und mehrere Verben, wenn Sie ein benutzerdefiniertes Dateiformat in der Windows-Shell implementieren.
title: Bewährte Methoden für Kontextmenühandler und mehrere Verben
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 14ec2e8915aa1df47ca21c6436ec963be3f590f5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396445"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Bewährte Methoden für Kontextmenühandler und mehrere Verben

Dieses Thema ist wie folgt organisiert:

-   [Bewährte Methoden](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Bewährte Methoden für Verbimplementierungen](#best-practices-for-verb-implementations)
-   [Bewährte Methoden für Mehrfachauswahlverben](#best-practices-for-multiple-selection-verbs)
    -   [Heterogene Auswahl](#heterogenous-selections)
-   [Verwandte Themen](#related-topics)

## <a name="best-practices"></a>Bewährte Methoden

Statische Verben sind am einfachsten zu implementierende Verben und bieten umfassende Funktionen. Es wird dringend empfohlen, ein Verb mithilfe einer der statischen Verbmethoden zu implementieren.

### <a name="best-practices-for-verb-implementations"></a>Bewährte Methoden für Verbimplementierungen

Die folgende Liste enthält bewährte Methoden für Verbimplementierungen:

-   Wählen Sie immer die einfachste Verbmethode aus, die Ihren Anforderungen entspricht.
-   Verwenden Sie nach Möglichkeit eine statische Verbmethode.
-   Führen Sie keine ressourcenintensiven Vorgänge oder E/A-Vorgänge für den UI-Thread aus. Sowohl [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) als auch [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) müssen bei ihrer Arbeit sehr konservativ sein. [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) muss in einem anderen Prozess ausgeführt werden, oder Sie müssen einen neuen Thread erstellen, um zu vermeiden, dass der Aufrufer blockiert wird.
-   Stellen Sie Verben den Namen des unabhängigen Softwareherstellers (Independent Software Vendor, ISV) wie folgt `ISVName.verb` voran: . Die Verwendung von nicht qualifizierten Namen kann zu Kollisionen mit mehreren ISVs führen, die denselben Verbnamen ausgewählt haben.
-   Verwenden Sie immer eine anwendungsspezifische ProgID. Da einige Elementtypen diese Zuordnung nicht verwenden, ist es notwendig, herstellerspezifische Namen zu verwenden.
-   Positionieren Sie die Benutzeroberfläche relativ zur aufrufenden Methode, führen Sie sie jedoch nicht in einem Invokerthread aus.
-   Akzeptieren Sie nicht den Rückgabewert **S \_ OK für** kanonische Verben, die an die [**IContextMenu::InvokeCommand-Methode übergeben**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) werden. Dies führt dazu, dass ein Fehler bei der Implementierung des echten Verbs aufgerufen wird, und gibt einen Fehlercode für kanonische Verben zurück. Wenn Sie keine kanonischen Verben unterstützen, geben Sie einen Fehler zurück, wenn ein HIWORD(lpVerb)-Wert ungleich 0 (null) gefunden wird.
-   Vermeiden Sie die Verwendung **rundll32.exe** als Host für Ihr Verb.
-   Stellen Sie beim Implementieren von [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) sicher, dass Sie die Anzahl der Verben zurückgeben, die dem Menü über den **HRESULT-Wert** mithilfe des ResultFromShort-Makros hinzugefügt wurden.
-   Wenn Sie sich für einen der folgenden Registrierungsschlüsseleinträge registrieren, sollten Sie vorsichtig sein, und achten Sie darauf, den Handler für den spezifischsten Typ zu registrieren, um die möglicherweise unbeabsichtigten Folgen zu reduzieren:
    -   **HKEY \_ CLASSES \_ ROOT\\\***
    -   **HKEY \_ CLASSES \_ ROOT \\ AllFileSystemObjects**
    -   **HKEY \_ CLASSES \_ ROOT \\ Folder**
    -   **HKEY \_ CLASSES \_ ROOT \\ Directory**
-   Legen Sie **die MayChangeDefaultMenu-Taste** nur fest, wenn Sie davon ausgehen, dass Sie möglicherweise das Standardverb im Kontextmenü ändern müssen. Wenn ihr Handler das Standardverb nicht ändert, sollten Sie diesen Schlüssel nicht festlegen, da dies dazu führt, dass das System die DLL unnötigerweise geladen.
-   Minimieren Sie die Arbeit, die Sie in [**IShellExtInit::Initialize ausführen.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) Erfassen Sie für Kontextmenühandler das an **IShellExtInit::Initialize** übergebene Datenobjekt, und verarbeiten Sie es dann in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)oder [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Bewährte Methoden für Mehrfachauswahlverben

Da die Anzahl der Elemente in einem Mehrfachauswahl-Verbszenario groß sein kann, ist es wichtig, dass Sie die Auswirkungen Ihrer Verbimplementierung auf die Leistung berücksichtigen. Wenn ein Benutzer beispielsweise in einem Bereich, der eine große Anzahl von Elementen enthält, nach " " sucht und dann auf Alles auswählen klickt und mit der rechten Maustaste klickt, wird dem Verb eine Auswahl angezeigt, die Tausende von Elementen enthalten \* kann.  Daher sollten Verben nur das erste Element in der Auswahl und die Gesamtanzahl der Elemente berücksichtigen. Das erste Element wird entweder als das Element oben in der Ansicht oder als das Element definiert, auf das der Benutzer zuerst mit der rechten Maustaste geklickt hat.

In Windows 7 und höher ist die Anzahl von Elementen, die an ein Verb übergeben werden, auf 16 beschränkt, wenn ein Kontextmenü abgefragt wird. Das Verb wird dann neu erstellt und mit der vollständigen Auswahl neu initialisiert, wenn dieses Verb aufgerufen wird.

In einigen Fällen ist es sinnvoll, eine kleine Anzahl fester Elemente zu berücksichtigen. Beispielsweise ist es für ein Diff-Verb geeignet, nur die ersten beiden Elemente zu berücksichtigen. Im Allgemeinen müssen Sie nicht jedes Element in der Auswahl testen, um zu prüfen, ob es sich um einen bestimmten Typ handelt, oder jedes Element in der Auswahl nach seinen Eigenschaften abfragen. Sehen Sie sich stattdessen das erste Element an, und entscheiden Sie, ob es sinnvoll ist, Ihr Verb hinzuzufügen.

### <a name="heterogenous-selections"></a>Heterogene Auswahl

Optimistische Verben werden im Mehrfachauswahlfall automatisch hinzugefügt, vorausgesetzt, dass nicht spektivische Elemente vom Verb behandelt werden können. Im Gegensatz dazu werden pessimistische Verben nicht hinzugefügt, wenn die Auswahl unbeabsichtigte Elemente enthält, und sie werden nur in Fällen hinzugefügt, in denen die Anzahl der Elemente klein ist.

Verben im Playerstil sollten optimistisch sein und die Elemente, die nicht behandelt werden, im Hintergrund überspringen. Wenn ein Fehler bei der Bearbeitung von Elementen zu Datenverlusten oder Verwirrung führen kann, sollte das Verb Benutzer vor Elementen warnen, die nicht verarbeitet werden können. Beispielsweise sollte ein "backup"-Verb angeben, dass einige Elemente nicht gesichert werden konnten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Erstellen von Kontextmenühandlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mit dynamischen Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenühandler](context-menu.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Kontextmenüreferenz](context-menu-reference.md)
</dt> </dl>

 

 



