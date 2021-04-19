---
title: Wahrgenommene Typen (Features der Legacy-Windows-Umgebung)
description: "\"Wahrnehmvedtype\" ist eine Eigenschaft, die ein Element im Index klassifiziert."
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341987"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Wahrgenommene Typen (Features der Legacy-Windows-Umgebung)

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

`PerceivedType` ist eine Eigenschaft, die ein Element im Index klassifiziert. Diese Klassifizierung unterscheidet sich von der "Kind"-Klassifizierung, die von der [erweiterten Abfrage Syntax](-search-2x-wds-aqsreference.md) verwendet wird, aber auf ähnliche Weise können Benutzer Ihre Suchergebnisse verfeinern. Mit der AQS-Art können Benutzer Ihre Suchabfrage einschränken, während die Eigenschaft "wahrvedtype" Benutzern das Filtern des Resultsets ermöglicht.

## <a name="types"></a>Typen

Verwenden Sie die Eigenschaft "wahrnehmvedtype", um den Dateityp zu klassifizieren, sodass Benutzer Ihre Suchergebnisse nach Typ filtern können. Die Ausgabe muss eine der folgenden Zeichen folgen sein:

-   contact
-   Kommunikation
-   Kommunikation/e-Mail
-   Kommunikation/Kalender
-   Kommunikation/Aufgabe
-   Kommunikation/im
-   Dokument
-   Dokument/Hinweis
-   Dokument/Text
-   Dokument/Kalkulations Tabelle
-   Dokument/Präsentation
-   music
-   images
-   Bilder/Bild
-   Bilder/Video
-   folder
-   Programm

Wenn Sie z. b. ein Filter-Add-in für einen neuen Bilddateityp erstellen möchten, müssen Sie Folgendes in Ihrer [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle implementieren:

-   **GetChunk** zum Zurückgeben einer fullpropspec, die Folgendes enthält: D5CDD505-2E9C-101B-9397-08002B2CF9AE/wahrnehmvedtype
-   **GetValue** zum Zurückgeben einer PROPVARIANT, die Folgendes enthält: VT \_ LPWSTR = "Images/Bild"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Entwickeln von IFilter-Add-ins](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-2x-wds-phaddins.md)
</dt> <dt>

[Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Schema Tabelle](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
