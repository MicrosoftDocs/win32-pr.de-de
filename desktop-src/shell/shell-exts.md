---
description: In diesem Thema wird erläutert, wie Sie die Erweiterungshandler implementieren, mit denen Sie eine Vielzahl von Shellaktionen ändern können.
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

Die Funktionen der Shell können mit Registrierungseinträgen und .ini Dateien erweitert werden. Obwohl dieser Ansatz zum Erweitern der Shell einfach und für viele Zwecke geeignet ist, ist er begrenzt. Wenn Sie beispielsweise die Registrierung verwenden, um ein benutzerdefiniertes Symbol für einen Dateityp anzugeben, wird das gleiche Symbol für jede Datei dieses Typs angezeigt. Wenn Sie die Shell mit der Registrierung erweitern, können Sie das Symbol für verschiedene Member des Dateityps nicht ändern. Andere Aspekte der Shell,  z. B. das Eigenschafteneigenschaftenblatt, das angezeigt werden kann, wenn mit der rechten Maustaste auf eine Datei geklickt wird, können mit der Registrierung überhaupt nicht geändert werden.

Ein leistungsfähigerer und flexiblerer Ansatz zum Erweitern der Shell ist die Implementierung von *Shellerweiterungshandlern.* Diese Handler können für eine Vielzahl von Aktionen implementiert werden, die die Shell ausführen kann. Vor dem Ergreifen der Aktion fragt die Shell den Erweiterungshandler ab und gibt ihm die Möglichkeit, die Aktion zu ändern. Ein gängiges Beispiel ist ein Kontextmenüerweiterungshandler. Wenn einer für einen Dateityp implementiert ist, wird er jedes Mal abgefragt, wenn mit der rechten Maustaste auf eine der Dateien geklickt wird. Der Handler kann dann dateiweise zusätzliche Menüelemente angeben, anstatt für alle Dateien dieses Dateityps denselben Satz festzulegen.

In diesem Thema wird erläutert, wie Sie die Erweiterungshandler implementieren, mit denen Sie eine Vielzahl von Shellaktionen ändern können. Die folgenden Handler sind einem bestimmten Dateityp zugeordnet und ermöglichen es Ihnen, dateiweise anzugeben.



| Handler                                               | BESCHREIBUNG                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenühandler](context-menu-handlers.md)    | Wird aufgerufen, bevor das Kontextmenü einer Datei angezeigt wird. Sie können dem Kontextmenü Datei für Datei Elemente hinzufügen.                                               |
| [Datenhandler](how-to-create-data-handlers.md)       | Wird aufgerufen, wenn ein Drag & Drop-Vorgang für Shell-Objekte ausgeführt wird. Sie können dem Ablageziel zusätzliche Zwischenablageformate bereitstellen.                            |
| [Drop-Handler](how-to-create-drop-handlers.md)       | Wird aufgerufen, wenn ein Datenobjekt über eine Datei gezogen oder abgelegt wird. Sie ermöglicht es Ihnen, eine Datei in ein Ablageziel zu verwandeln.                                                          |
| [Symbolhandler](how-to-create-icon-handlers.md)       | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Sie können das Standardsymbol der Datei durch ein benutzerdefiniertes Symbol auf Dateibasis ersetzen.                                    |
| [Eigenschaftenblatthandler](propsheet-handlers.md)      | Wird aufgerufen, bevor das **Eigenschaftenblatt eigenschaften** eines Objekts angezeigt wird. Sie können Seiten hinzufügen oder ersetzen.                                                              |
| [**Handler für Miniaturansichtsbilder**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Stellt ein Bild bereit, das das Element darstellt.                                                                                                                                   |
| [**QuickInfo-Handler**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Stellt Popuptext bereit, wenn der Benutzer mit dem Mauszeiger auf das Objekt zeigt.                                                                                               |
| [**Metadatenhandler**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Bietet Lese- und Schreibzugriff auf Metadaten (Eigenschaften), die in einer Datei gespeichert sind. Dies kann verwendet werden, um die Detailansicht, Infotips, die Eigenschaftenseite und Gruppierungsfunktionen zu erweitern. |



 

Andere sind keinem bestimmten Dateityp zugeordnet, werden aber vor einigen Shell-Vorgängen aufgerufen.



| Handler                                                            | BESCHREIBUNG                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Spaltenhandler](../lwef/column-handlers.md)                             | Wird von Windows Explorer aufgerufen, bevor die Detailansicht eines Ordners angezeigt wird. Sie können der Detailansicht benutzerdefinierte Spalten hinzufügen.        |
| [Hookhandler kopieren](how-to-create-copy-hook-handlers.md)          | Wird aufgerufen, wenn ein Ordner- oder Druckerobjekt verschoben, kopiert, gelöscht oder umbenannt werden soll. Sie können den Vorgang genehmigen oder genehmigen.   |
| [Drag &amp;amp; Drop-Handler](context-menu-handlers.md)                 | Wird aufgerufen, wenn eine Datei mit der rechten Maustaste gezogen wird. Sie können das angezeigte Kontextmenü ändern.                     |
| [Symbolüberlagerungshandler](how-to-implement-icon-overlay-handlers.md) | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Sie können eine Überlagerung für das Dateisymbol angeben.                                          |
| [Suchhandler](../lwef/search-handlers.md)                             | Wird aufgerufen, um eine Suchmaschine zu starten. Sie können eine benutzerdefinierte Suchmaschine implementieren, auf die über das **Startmenü** oder Windows Explorer zugegriffen werden kann. |



 

Die Details zum Implementieren bestimmter Erweiterungshandler werden in den oben aufgeführten Abschnitten behandelt. Informationen zu Implementierungsproblemen, die allen Shell-Erweiterungshandlern gemeinsam sind, finden Sie in den folgenden Themen:

-   [Initialisieren von Shellerweiterungshandlern](int-shell-exts.md)
-   [Registrieren von Shellerweiterungshandlern](reg-shell-exts.md)

 

 
