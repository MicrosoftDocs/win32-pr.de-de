---
description: Erfahren Sie, wie Sie das Windows-Explorer-Menüband erweitern.
title: Erweitern der Multifunktionsleiste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525322"
---
# <a name="extending-the-ribbon"></a>Erweitern der Multifunktionsleiste

In Windows-Explorer hilft das Menüband, gängige Aktivitäten für die Dateiverwaltung von Endbenutzern einfacher und leichter auffindbar zu machen, aber es gibt Änderungen für App-Entwickler. Die alte Befehlsleiste war z. b. frei erweiterbar, aber das Menüband ist zu diesem Zeitpunkt stärker eingeschränkt. Außerdem wird das Menüband nicht standardmäßig für alle Namespace Erweiterungen angezeigt, sodass Sie sich für das Menüband entscheiden müssen. Andernfalls erhalten Sie die ältere Befehlsleiste.

Aktionen, die für Benutzer auf dem Menüband verfügbar sind, können in drei Erweiterbarkeits Kategorien eingeteilt werden:

-   Erweiterbarkeit ist nicht erforderlich. Beispiele: kopieren, einfügen, löschen. Diese Verben werden von Windows verarbeitet.
-   Die Erweiterbarkeit ist zurzeit nicht zulässig: Beispiele: ZIP, Sitzung schließen und andere benutzerdefinierte Aktionen. Verwenden Sie das Kontextmenü, um diese Szenarien abzudecken.
-   Die Erweiterbarkeit ist in die Aktion selbst integriert. Beispiele: suchen, e-Mail, drucken, neues Element. Sie müssen sich für diese Verben registrieren, um Ihre APP oder Ihr Dateiformat in das Menüband einzubeziehen.

In diesem Dokument wird beschrieben, wie Sie sich für das Menüband anmelden und wie Sie sich registrieren, um bestimmte Menüband-Verben zu behandeln.

## <a name="opting-in-to-the-ribbon"></a>Abonnieren des Menübands

Um das Menüband zu abonnieren, sollte die [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) -Implementierung das **EP- \_ Menüband** in [**iexplorerpanevisibility:: getpanestate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) angeben und den Wert " **EPS \_ Force** \| **EPS \_ default" \_ auf** zurückgeben.

## <a name="extending-the-ribbon-for-file-extensions"></a>Erweitern des Menübands für Dateierweiterungen

Diese Menüband-Schaltflächen sind auf der Grundlage von Dateierweiterungen erweiterbar:

-   Alle extrahieren
-   \|Einstellungsburn (ein ISO)
-   Wiedergabe Wiedergabe \| alles \| Hinzufügen zu Wiedergabeliste (Verb: Einreihen in Warteschlange)
-   Öffnen
-   Edit (Bearbeiten)
-   Eigenschaften

Wenn Sie sich registrieren, um die relevanten Verben für neue Dateitypen statisch zu behandeln, verarbeitet das Menüband die Verben entsprechend. Sie registrieren sich genauso wie für Kontextmenü Verben. Weitere Informationen zu Dateizuordnungen und zur Registrierung für Verben finden Sie unter [Verben und Dateizuordnungen](fa-verbs.md) und Erstellen von Kontext [Menü Handlern](context-menu-handlers.md).

## <a name="registering-as-a-default-handler-for-actionids"></a>Registrieren als Standard Handler für "aktionids"

Registrieren Sie zuerst Ihre ProgID unter dem entsprechenden Unterschlüssel "assocactionid". Jeder Unterschlüssel von assocactionid stellt ein Verb oder eine Aktion dar, die Benutzer über das Menüband aufrufen können. In diesem Beispiel registriert die APP für die zipselection-Aktions-ID, um die Schaltfläche "Alle extrahieren" im Menüband zu erweitern.

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

Nachdem diese Registrierung durchgeführt wurde, müssen Sie sich so registrieren, dass Sie die Protokolle wie gewohnt behandelt, wie in [Standardprogramme](default-programs.md)beschrieben.

 

 



