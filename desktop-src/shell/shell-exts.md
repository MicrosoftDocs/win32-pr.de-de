---
description: In diesen Themen wird erläutert, wie Sie die Erweiterungshandler implementieren, mit denen Sie eine Vielzahl von Shellaktionen ändern können.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Arbeiten mit Shellerweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 804b121ccf633b44574ae956b367143eebdaf7a2a3a8a9cc8400995522b4cbef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452848"
---
# <a name="working-with-shell-extensions"></a>Arbeiten mit Shellerweiterungen

Die Funktionen der Shell können mit Registrierungseinträgen und .ini erweitert werden. Dieser Ansatz zum Erweitern der Shell ist zwar einfach und für viele Zwecke ausreichend, aber er ist begrenzt. Wenn Sie beispielsweise die Registrierung verwenden, um ein benutzerdefiniertes Symbol für einen Dateityp anzugeben, wird für jede Datei dieses Typs das gleiche Symbol angezeigt. Wenn Sie die Shell mit der Registrierung erweitern, können Sie das Symbol für verschiedene Member des Dateityps nicht ändern. Andere Aspekte der Shell,  z. B. das Eigenschaftenblatt, das angezeigt werden kann, wenn mit der rechten Maustaste auf eine Datei geklickt wird, können mit der Registrierung überhaupt nicht geändert werden.

Ein leistungsstärkerer und flexiblerer Ansatz zum Erweitern der Shell ist die Implementierung von *Shellerweiterungshandlern.* Diese Handler können für eine Vielzahl von Aktionen implementiert werden, die die Shell ausführen kann. Vor dem Ausführen der Aktion fragt die Shell den Erweiterungshandler ab und gibt ihr die Möglichkeit, die Aktion zu ändern. Ein häufiges Beispiel ist ein Kontextmenü-Erweiterungshandler. Wenn eine Datei für einen Dateityp implementiert ist, wird sie jedes Mal abgefragt, wenn mit der rechten Maustaste auf eine der Dateien geklickt wird. Der Handler kann dann dateispezifische zusätzliche Menüelemente angeben, anstatt für alle Dateien dieses Dateityps denselben Satz festzulegen.

In diesen Themen wird erläutert, wie Sie die Erweiterungshandler implementieren, mit denen Sie eine Vielzahl von Shellaktionen ändern können. Die folgenden Handler sind einem bestimmten Dateityp zugeordnet und ermöglichen die Datei-für-Datei-Angabe.



| Handler                                               | BESCHREIBUNG                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenühandler](context-menu-handlers.md)    | Wird aufgerufen, bevor das Kontextmenü einer Datei angezeigt wird. Dadurch können Sie dem Kontextmenü Datei für Datei Elemente hinzufügen.                                               |
| [Datenhandler](how-to-create-data-handlers.md)       | Wird aufgerufen, wenn ein Drag & Drop-Vorgang für Shellobjekte ausgeführt wird. Sie können dem Ablageziel zusätzliche Zwischenablageformate bereitstellen.                            |
| [Drop-Handler](how-to-create-drop-handlers.md)       | Wird aufgerufen, wenn ein Datenobjekt in einer Datei gezogen oder gelöscht wird. Dadurch können Sie eine Datei zu einem Abbruchziel machen.                                                          |
| [Symbolhandler](how-to-create-icon-handlers.md)       | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Sie können das Standardsymbol der Datei durch ein benutzerdefiniertes Symbol auf Dateibasis ersetzen.                                    |
| [Eigenschaftenblatthandler](propsheet-handlers.md)      | Wird aufgerufen, bevor das **Eigenschaftenblatt Eigenschaften** eines Objekts angezeigt wird. Dadurch können Sie Seiten hinzufügen oder ersetzen.                                                              |
| [**Handler für Miniaturansichtsbilder**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Stellt ein Bild zur Darstellung des Elements dar.                                                                                                                                   |
| [**QuickInfo-Handler**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Stellt Popuptext zum Zeitpunkt der Mauszeigerbewegung über das -Objekt zurVerfingung von Text zur Verall-/Ausblendung zur -Objekt-100000000-1000-1000-                                                                                               |
| [**Metadatenhandler**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Bietet Lese- und Schreibzugriff auf Metadaten (Eigenschaften), die in einer Datei gespeichert sind. Dies kann verwendet werden, um die Detailansicht, Infotips, die Eigenschaftenseite und Gruppierungsfeatures zu erweitern. |



 

Andere sind nicht einem bestimmten Dateityp zugeordnet, werden jedoch vor einigen Shellvorgängen aufgerufen.



| Handler                                                            | BESCHREIBUNG                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Spaltenhandler](../lwef/column-handlers.md)                             | Wird vom Windows-Explorer aufgerufen, bevor die Detailansicht eines Ordners angezeigt wird. Sie können der Detailansicht benutzerdefinierte Spalten hinzufügen.        |
| [Hookhandler kopieren](how-to-create-copy-hook-handlers.md)          | Wird aufgerufen, wenn ein Ordner oder Druckerobjekt verschoben, kopiert, gelöscht oder umbenannt werden soll. Sie können den Vorgang genehmigen oder blockieren.   |
| [Drag &amp;amp; Drop-Handler](context-menu-handlers.md)                 | Wird aufgerufen, wenn eine Datei mit der rechten Maustaste gezogen wird. Sie können das angezeigte Kontextmenü ändern.                     |
| [Symbolüberlagerungshandler](how-to-implement-icon-overlay-handlers.md) | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Dadurch können Sie eine Überlagerung für das Symbol der Datei angeben.                                          |
| [Suchhandler](../lwef/search-handlers.md)                             | Wird aufgerufen, um eine Suchmaschine zu starten. Sie können eine benutzerdefinierte Suchmaschine implementieren, auf die über das **Startmenü oder** den Windows kann. |



 

Die Details zum Implementieren bestimmter Erweiterungshandler werden in den oben aufgeführten Abschnitten behandelt. Informationen zu Implementierungsproblemen, die allen Shell-Erweiterungshandlern gemeinsam sind, finden Sie in den folgenden Themen:

-   [Initialisieren von Shellerweiterungshandlern](int-shell-exts.md)
-   [Registrieren von Shellerweiterungshandlern](reg-shell-exts.md)

 

 
