---
description: Verwenden des Medienlocator
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Verwenden des Medienlocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be064a375f121f7c4e3dad54c2615bf8d6f7df489e119ec9cbb2c6f4b4294628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633130"
---
# <a name="using-the-media-locator"></a>Verwenden des Medienlocator

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Der Medienlocator ist ein Hilfsobjekt, das Dateinamen überprüft und nach fehlenden Dateien in lokalen Verzeichnissen oder Netzwerkverzeichnissen sucht. Die Medienerkennung speichert einen Cache von Verzeichnispfaden, in denen dateien in früheren Suchvorgängen erfolgreich gefunden wurden. Um eine Datei zu suchen, durchsucht sie die Verzeichnisse im Cache. Wenn dies nicht der Fehler ist, kann die Medienerkennung ein Dialogfeld Datei öffnen anzeigen, in dem der Benutzer manuell nach einer Datei suchen kann. Wenn der Benutzer die Datei findet, fügt der Medienlocator das neue Verzeichnis dem Cache hinzu. Der Medienlocator macht die [**IMediaLocator-Schnittstelle**](imedialocator.md) verfügbar.

In der Regel erstellt Ihre Anwendung nicht direkt eine Instanz des Medienlocator. Stattdessen stellen die Zeitachse und die Render-Engine die folgenden Methoden zum Überprüfen von Dateinamen mithilfe der Medienerkennung zur Verfügung.

-   Um Dateinamen auf der Zeitachse zu überprüfen, rufen [**Sie IAMTimeline::ValidateSourceNames auf.**](iamtimeline-validatesourcenames.md) Optional aktualisiert diese Methode auch die Quellobjekte mit den richtigen Dateinamen.
-   Um Dateinamen beim Rendern des Projekts zu überprüfen, rufen Sie [**IRenderEngine::SetSourceNameValidation auf.**](irenderengine-setsourcenamevalidation.md)

Beide Methoden verwenden Flags, die das Verhalten des Medienlocator steuern. Beispielsweise können Sie die Suche auf lokale Verzeichnisse beschränken.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



