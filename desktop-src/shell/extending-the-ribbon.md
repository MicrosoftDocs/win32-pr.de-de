---
description: Erfahren Sie, wie Sie das menüband Windows Explorer erweitern.
title: Erweitern des Menübands
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 635698461f897a08248ea99bf68d534ea8ad24763f926460d2e9ce64181ba2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860851"
---
# <a name="extending-the-ribbon"></a>Erweitern des Menübands

In Windows Explorer hilft das Menüband dabei, allgemeine Dateiverwaltungsaktivitäten von Endbenutzern einfacher und leichter auffindbar zu machen, aber es gibt Änderungen für App-Entwickler. Beispielsweise war die alte Befehlsleiste frei erweiterbar, aber das Menüband ist zu diesem Zeitpunkt stärker eingeschränkt. Außerdem wird das Menüband nicht standardmäßig für alle Namespaceerweiterungen angezeigt, sodass Sie sich für das Abrufen des Menübands entscheiden müssen. Andernfalls wird die ältere Befehlsleiste angezeigt.

Aktionen, die Benutzern im Menüband zur Verfügung stehen, lassen sich in drei Erweiterbarkeitskategorien unterteilen:

-   Erweiterbarkeit ist nicht erforderlich. Beispiele: Kopieren, Einfügen, Löschen. Windows verarbeitet diese Verben für Sie.
-   Erweiterbarkeit ist derzeit nicht zulässig: Beispiele: ZIP, Sitzung schließen und andere benutzerdefinierte Aktionen. Verwenden Sie das Kontextmenü, um diese Szenarien abzudecken.
-   Erweiterbarkeit ist in die Aktion selbst integriert. Beispiele: Suchen, E-Mail, Drucken, Neues Element. Sie müssen sich für diese Verben registrieren, um Ihre App oder das Dateiformat in das Menüband aufzunehmen.

In diesem Dokument wird beschrieben, wie Sie das Menüband abrufen und registrieren können, um bestimmte Menübandverben zu verarbeiten.

## <a name="opting-in-to-the-ribbon"></a>Anmelden am Menüband

Um das Menüband zu wählen, sollte Ihre [**IShellFolder2-Implementierung**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) **das \_ EP-Menüband** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) angeben und **EPS \_ FORCE** \| **EPS \_ DEFAULT \_ ON** zurückgeben.

## <a name="extending-the-ribbon-for-file-extensions"></a>Erweitern des Menübands für Dateierweiterungen

Diese Menübandschaltflächen sind basierend auf Dateierweiterungen erweiterbar:

-   Alle extrahieren
-   Mount \| Burn (an ISO)
-   Play \| Play All \| Add to Playlist (verb: Enqueue)
-   Öffnen
-   Bearbeiten
-   Eigenschaften

Wenn Sie sich registrieren, um die relevanten Verben für neue Dateitypen statisch zu behandeln, verarbeitet das Menüband die Verben entsprechend. Sie registrieren sich genau wie bei Kontextmenüverben. Weitere Informationen zu Dateizuordnungen und zur Registrierung für Verben finden Sie unter [Verben und Dateizuordnungen](fa-verbs.md) und [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)

## <a name="registering-as-a-default-handler-for-actionids"></a>Registrieren als Standardhandler für ActionIds

Registrieren Sie zunächst Ihre ProgId unter dem entsprechenden AssocActionId-Unterschlüssel. Jeder AssocActionId-Unterschlüssel stellt ein Verb oder eine Aktion dar, die Benutzer über das Menüband aufrufen können. In diesem Beispiel registriert sich die App für die ZipSelection ActionID, um die Schaltfläche "Alle extrahieren" auf dem Menüband zu erweitern.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

Sobald diese Registrierung abgeschlossen ist, müssen Sie sich registrieren, um Protokolle wie gewohnt zu verarbeiten, wie unter [Standardprogramme](default-programs.md)beschrieben.

 

 



