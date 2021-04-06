---
description: Verwenden des medienlocators
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Verwenden des medienlocators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961099"
---
# <a name="using-the-media-locator"></a>Verwenden des medienlocators

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Der medienlocator ist ein Hilfsobjekt, das Dateinamen überprüft und nach fehlenden Dateien in lokalen Verzeichnissen oder Netzwerkverzeichnissen sucht. Der Medien Detektor speichert einen Cache von Verzeichnis Pfaden, in denen er Dateien in früheren Such Vorgängen erfolgreich gefunden hat. Um eine Datei zu suchen, durchsucht Sie die Verzeichnisse im Cache. Wenn ein Fehler auftritt, kann der Medien Detektor ein Dialogfeld "Datei öffnen" anzeigen, in dem der Benutzer eine Datei manuell finden kann. Wenn der Benutzer die Datei eingibt, fügt der medienlocator das neue Verzeichnis dem Cache hinzu. Der medienlocator macht die [**imedialocator**](imedialocator.md) -Schnittstelle verfügbar.

In der Regel erstellt Ihre Anwendung nicht direkt eine Instanz des medienlocators. Stattdessen stellen die Zeitachse und die Renderingengine die folgenden Methoden zum Validieren von Dateinamen mithilfe des Medien Detektors bereit.

-   Um Dateinamen in der Zeitachse zu validieren, nennen Sie [**iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md). Optional aktualisiert diese Methode auch die Quell Objekte mit den richtigen Dateinamen.
-   Zum Überprüfen von Dateinamen, wenn das Projekt gerendert wird, nennen Sie " [**irienderengine:: setsourcenamevalidation**](irenderengine-setsourcenamevalidation.md)".

Beide Methoden verwenden Flags, die das Verhalten des medienlocators steuern. Beispielsweise können Sie die Suche auf lokale Verzeichnisse beschränken.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



