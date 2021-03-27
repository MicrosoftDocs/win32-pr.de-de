---
description: In diesem Abschnitt wird die Erstellung von Kontextmenüs (Kontextmenüs) und die Implementierung von Kontextmenü-Handlern (Verb) erläutert.
title: Kontextmenüs und Kontextmenü Handler
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214437"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>Kontextmenüs und Kontextmenü Handler

In diesem Abschnitt wird die Erstellung von Kontextmenüs (Kontextmenüs) und die Implementierung von Kontextmenü-Handlern (Verb) erläutert.

Dieser Abschnitt zu Dateitypen und Dateizuordnungen ist wie folgt organisiert:

-   [Verben und Dateizuordnungen](fa-verbs.md)
-   [Auswählen einer statischen oder dynamischen Kontextmenü Methode](shortcut-choose-method.md)
-   [Bewährte Methoden für Kontextmenü Handler und mehrere Verben](verbs-best-practices.md)
-   [Erstellen von Kontextmenü Handlern](context-menu-handlers.md)
-   [Erstellen von statischen kaskadierenden Menüs](creating-static-cascading-menus.md)
-   [Unterdrücken der Sichtbarkeit des Verbs](how-to-suppress-and-control-visibility.md)
-   [Verwenden des Verb Auswahl Modells](how-to-employ-the-verb-selection-model.md)
-   [Verwenden von Element Attributen](how-to-use-item-attributes.md)
-   [So implementieren Sie benutzerdefinierte Verben für Ordner über Desktop.ini](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md)
-   [Implementieren der IContextMenu-Schnittstelle](how-to-implement-the-icontextmenu-interface.md)
-   [Verweis auf das Kontextmenü](context-menu-reference.md)

## <a name="additional-resources"></a>Weitere Ressourcen

Verwandte konzeptionelle Hintergrundinformationen finden Sie in den folgenden Themen:

-   [Einführung in Dateizuordnungen](fa-intro.md).
-   Informationen zum Erweitern der Shell mit Dateityp Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).
-   Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](nse-implement.md).

Weitere Informationen zur zugehörigen Referenz Dokumentation finden Sie in den folgenden Themen:

-   Informationen zum Ausführen eines Verbs für ein shellelement finden Sie unter der [**invokeverb**](folderitem-invokeverb.md) -Methode.
-   Weitere Informationen zum Abrufen einer Auflistung von Verben, die für ein shellelement ausgeführt werden können, finden Sie in der [**Verbs**](folderitem-verbs.md) -Methode.
-   Informationen zum Ausführen eines Vorgangs für eine angegebene Datei finden Sie unter den Funktionen [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

 

 



