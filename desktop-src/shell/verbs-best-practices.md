---
description: 'Dieses Thema ist wie folgt organisiert:'
title: Bewährte Methoden für Kontextmenü Handler und mehrere Verben
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f8b47807c4647aec274e64dbcd137833d13e23cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980216"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Bewährte Methoden für Kontextmenü Handler und mehrere Verben

Dieses Thema ist wie folgt organisiert:

-   [Bewährte Methoden](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Bewährte Methoden für Verb Implementierungen](#best-practices-for-verb-implementations)
-   [Bewährte Methoden für Mehrfachauswahl Verben](#best-practices-for-multiple-selection-verbs)
    -   [Heterogene Auswahl](#heterogenous-selections)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices"></a>Bewährte Methoden

Statisches Verb sind einfachste Verben, die implementiert werden können, und stellen umfassende Funktionen bereit. Wir empfehlen Ihnen dringend, ein Verb mit einer der statischen Verb-Methoden zu implementieren.

### <a name="best-practices-for-verb-implementations"></a>Bewährte Methoden für Verb Implementierungen

Die folgende Liste stellt bewährte Methoden für Verb Implementierungen dar:

-   Wählen Sie immer die einfachste Verb Methode aus, die Ihren Anforderungen entspricht.
-   Verwenden Sie nach Möglichkeit eine statische Verb-Methode.
-   Führen Sie keine ressourcenintensiven Vorgänge oder e/a-Vorgänge im UI-Thread aus. Sowohl [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) als auch [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) müssen bei der Arbeit, die Sie ausführen, sehr konservativ sein. [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) muss in einem anderen Prozess ausgeführt werden, oder Sie müssen einen neuen Thread erstellen, um die Blockierung des Aufrufers zu vermeiden.
-   Präfix Verben mit dem ISV-Namen (Independent Software Vendor) wie folgt: `ISVName.verb` . Die Verwendung von nicht qualifizierten Namen kann zu Konflikten mit mehreren ISVs führen, die denselben Verb Namen ausgewählt haben.
-   Verwenden Sie immer eine anwendungsspezifische ProgID. Da einige Elementtypen diese Zuordnung nicht verwenden, ist es erforderlich, dass Hersteller eindeutige Namen besitzen.
-   Positionieren Sie die Benutzeroberfläche relativ zur aufrufenden Methode, aber nicht in einem aufrufenden Thread.
-   Akzeptieren Sie den Rückgabewert **S \_ OK** für kanonische Verben, die an die [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) -Methode übermittelt wurden. Andernfalls tritt ein Fehler auf, wenn die wirkliche Verb-Implementierung aufgerufen wird, und es wird ein Fehlercode für kanonische Verben zurückgegeben. Wenn Sie kanonische Verben nicht unterstützen, wird ein Fehler zurückgegeben, wenn ein HIWORD-Wert (lpverb) ungleich 0 (null) gefunden wird.
-   Vermeiden Sie die Verwendung von **rundll32.exe** als Host für Ihr Verb.
-   Geben Sie bei der Implementierung von [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) die Anzahl der Verben zurück, die dem Menü über den **HRESULT** -Wert mithilfe des resultfromshort-Makros hinzugefügt wurden.
-   Wenn Sie sich für einen der folgenden Registrierungsschlüssel Einträge registrieren, gehen Sie vorsichtig vor, und stellen Sie sicher, dass Sie den Handler für den spezifischsten Typ registrieren, um die möglicherweise unbeabsichtigten Folgen zu verringern:
    -   **HKEY \_ \_Klassen \\ Stamm _ \**
    -   _ *HKEY- \_ Klassen \_ root \\ AllFilesystemObjects**
    -   **Stamm Ordner der HKEY- \_ Klassen \_ \\**
    -   **Stammverzeichnis der HKEY- \_ Klassen \_ \\**
-   Legen Sie den Schlüssel " **maychangedefaultmenu** " nur fest, wenn Sie davon ausgehen, dass Sie möglicherweise das Standard Verb im Kontextmenü ändern müssen. Wenn Ihr Handler das Standardverb nicht ändert, sollten Sie diesen Schlüssel nicht festlegen, da dies dazu führt, dass das System die dll unnötig lädt.
-   Minimieren Sie die Arbeit, die Sie in [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)ausführen. Erfassen Sie bei Kontextmenü Handlern das an **ishellextinit:: Initialize** übergebenen Datenobjekt, und verarbeiten Sie es anschließend in [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)oder [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Bewährte Methoden für Mehrfachauswahl Verben

Da die Anzahl der Elemente in einem Szenario mit Mehrfachauswahl Verb groß sein kann, ist es wichtig, dass Sie die Auswirkungen der Verb-Implementierungen auf die Leistung abwägen. Wenn ein Benutzer beispielsweise \* in einem Bereich, der eine große Anzahl von Elementen enthält, nach "" sucht und dann auf **Alle auswählen** und mit der rechten Maustaste klickt, wird das Verb mit einer Auswahl angezeigt, die Tausende Elemente enthalten kann. Demzufolge sollten Verben nur das erste Element in der Auswahl und die Gesamtanzahl der Elemente berücksichtigen. Das erste Element wird entweder als Element am oberen Rand der Ansicht oder als Element definiert, auf das der Benutzer zuerst mit der rechten Maustaste geklickt hat.

In Windows 7 und höher ist die Anzahl der an ein Verb weiter gegebenen Elemente auf 16 begrenzt, wenn ein Kontextmenü abgefragt wird. Das Verb wird dann neu erstellt und mit der vollständigen Auswahl erneut initialisiert, wenn dieses Verb aufgerufen wird.

In einigen Fällen ist es sinnvoll, eine kleine Anzahl fester Elemente in Erwägung zu nehmen. Beispielsweise ist es angebracht, dass ein Verb "diff" nur die ersten beiden Elemente berücksichtigt. Im Allgemeinen müssen Sie nicht jedes Element in der Auswahl testen, um festzustellen, ob es sich um einen bestimmten Typ handelt, oder alle Elemente in der Auswahl für die zugehörigen Eigenschaften Abfragen. Suchen Sie anstelle des ersten Elements, und entscheiden Sie, ob es angebracht ist, Ihr Verb hinzuzufügen.

### <a name="heterogenous-selections"></a>Heterogene Auswahl

Optimistische Verben werden automatisch im Mehrfachauswahl Fall hinzugefügt, wobei angenommen wird, dass nicht geprüfte Elemente vom Verb verarbeitet werden können. Im Gegensatz dazu werden pessimistische Verben nicht hinzugefügt, wenn die Auswahl nicht geprüfte Elemente enthält. Sie werden nur in Fällen hinzugefügt, in denen die Anzahl der Elemente gering ist.

Die Verben des Spielstils sollten optimistisch sein und die Elemente, die nicht behandelt werden, im Hintergrund überspringen. Wenn ein Fehler beim Bearbeiten von Elementen zu Datenverlust oder Verwirrung führen kann, sollte das Verb Benutzer vor Elementen warnen, die nicht verarbeitet werden können. Ein "Backup"-Verb sollte beispielsweise angeben, dass einige Elemente nicht gesichert werden konnten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Erstellen von Kontextmenü Handlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenü Handler](context-menu.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Verweis auf das Kontextmenü](context-menu-reference.md)
</dt> </dl>

 

 



