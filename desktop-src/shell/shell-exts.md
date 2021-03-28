---
description: In diesen Themen wird erläutert, wie die Erweiterungs Handler implementiert werden, mit denen Sie eine Vielzahl von shellaktionen ändern können.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Arbeiten mit Shellerweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb696f4536cdb0fb6869be073771d431bd8d2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980649"
---
# <a name="working-with-shell-extensions"></a>Arbeiten mit Shellerweiterungen

Die Funktionen der Shell können mit Registrierungs Einträgen und INI-Dateien erweitert werden. Diese Vorgehensweise zur Erweiterung der Shell ist einfach und für viele Zwecke ausreichend, Sie ist jedoch begrenzt. Wenn Sie z. b. die Registrierung verwenden, um ein benutzerdefiniertes Symbol für einen Dateityp anzugeben, wird das gleiche Symbol für jede Datei dieses Typs angezeigt. Wenn Sie die Shell mit der Registrierung erweitern, können Sie das Symbol für verschiedene Member des Dateityps nicht verändern. Andere Aspekte der Shell, wie z. b. das **Eigenschaften Blatt Eigenschaften** , das angezeigt werden kann, wenn mit der rechten Maustaste auf eine Datei geklickt wird, können überhaupt nicht mit der Registrierung geändert werden.

Eine leistungsfähigere und flexiblere Methode zur Erweiterung der Shell ist die Implementierung von *Shellerweiterungs Handlern*. Diese Handler können für eine Reihe von Aktionen implementiert werden, die die Shell ausführen kann. Vor dem Ausführen der Aktion fragt die Shell den Erweiterungs Handler ab und gibt ihm die Möglichkeit, die Aktion zu ändern. Ein gängiges Beispiel ist ein Erweiterungs Handler für den Kontextmenü. Wenn eine Datei für einen Dateityp implementiert ist, wird Sie jedes Mal abgefragt, wenn auf eine der Dateien mit der rechten Maustaste geklickt wird. Der Handler kann dann zusätzliche Menü Elemente auf Datei Basis angeben, anstatt denselben Satz für alle Dateien dieses Dateityps zu haben.

In diesen Themen wird erläutert, wie die Erweiterungs Handler implementiert werden, mit denen Sie eine Vielzahl von shellaktionen ändern können. Die folgenden Handler sind einem bestimmten Dateityp zugeordnet und ermöglichen es Ihnen, Datei-für-Datei-Basis anzugeben.



| Handler                                               | BESCHREIBUNG                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenü Handler](context-menu-handlers.md)    | Wird aufgerufen, bevor das Kontextmenü einer Datei angezeigt wird. Sie ermöglicht das Hinzufügen von Elementen zum Kontextmenü auf Datei Basis.                                               |
| [Daten Handler](how-to-create-data-handlers.md)       | Wird aufgerufen, wenn ein Drag & Drop-Vorgang für Shellobjekte ausgeführt wird. Sie ermöglicht es Ihnen, zusätzliche Zwischenablage Formate für das Ablage Ziel bereitzustellen.                            |
| [Drop-Handler](how-to-create-drop-handlers.md)       | Wird aufgerufen, wenn ein Datenobjekt in einer Datei gezogen oder gelöscht wird. Sie ermöglicht es Ihnen, eine Datei in ein Ablage Ziel zu übernehmen.                                                          |
| [Symbol Handler](how-to-create-icon-handlers.md)       | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Dadurch können Sie das Standard Symbol der Datei durch ein benutzerdefiniertes Symbol auf Datei Basis ersetzen.                                    |
| [Eigenschaftenblatthandler](propsheet-handlers.md)      | Wird aufgerufen, bevor das **Eigenschaften** Blatt eines Objekts angezeigt wird. Sie können Seiten hinzufügen oder ersetzen.                                                              |
| [**Miniatur Ansichts Bild Handler**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Stellt ein Bild bereit, das das Element darstellt.                                                                                                                                   |
| [**QuickInfo-Handler**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Stellt Popup Text bereit, wenn der Benutzer mit dem Mauszeiger auf das-Objekt zeigt.                                                                                               |
| [**Metadatenhandler**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Bietet Lese-und Schreibzugriff auf Metadaten (Eigenschaften), die in einer Datei gespeichert sind. Dies kann verwendet werden, um die Detailansicht, die Infotipps, die Eigenschaften Seite und die Gruppierungsfunktionen zu erweitern. |



 

Andere sind keinem bestimmten Dateityp zugeordnet, werden jedoch vor einigen shellvorgängen aufgerufen.



| Handler                                                            | BESCHREIBUNG                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Spaltenhandler](../lwef/column-handlers.md)                             | Wird von Windows Explorer aufgerufen, bevor die Detailansicht eines Ordners angezeigt wird. Damit können Sie der Detailansicht benutzerdefinierte Spalten hinzufügen.        |
| [Hook-Handler kopieren](how-to-create-copy-hook-handlers.md)          | Wird aufgerufen, wenn ein Ordner oder ein Drucker Objekt verschoben, kopiert, gelöscht oder umbenannt wird. Dies ermöglicht es Ihnen, den Vorgang zu genehmigen oder zu überstehen.   |
| [Drag &amp;amp; Drop-Handler](context-menu-handlers.md)                 | Wird aufgerufen, wenn eine Datei mit der rechten Maustaste gezogen wird. Es ermöglicht Ihnen, das angezeigte Kontextmenü zu ändern.                     |
| [Symbol Überlagerungs Handler](how-to-implement-icon-overlay-handlers.md) | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Damit können Sie ein Overlay für das Symbol der Datei angeben.                                          |
| [Such Handler](../lwef/search-handlers.md)                             | Wird aufgerufen, um eine Suchmaschine zu starten. Damit können Sie eine benutzerdefinierte Suchmaschine implementieren, auf die Sie über das **Startmenü** oder den Windows-Explorer zugreifen können. |



 

Die Details zur Implementierung bestimmter Erweiterungs Handler werden in den oben aufgeführten Abschnitten behandelt. Erörterung der Implementierungsprobleme, die allen Shellerweiterungs Handlern gemeinsam sind, finden Sie in den folgenden Themen:

-   [Initialisieren von Shellerweiterungs Handlern](int-shell-exts.md)
-   [Registrieren von Shellerweiterungs Handlern](reg-shell-exts.md)

 

 
