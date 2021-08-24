---
title: Wahrgenommene Typen (Legacy-Windows-Umgebungsfeatures)
description: PerceivedType ist eine Eigenschaft, die ein Element im Index klassifiziert.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de2baa37a46a9bd78e6e8a7ad94806dffe3a918046253bb09d4dab6090838b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610830"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Wahrgenommene Typen (Legacy-Windows-Umgebungsfeatures)

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search.](../search/-search-3x-wds-overview.md)

`PerceivedType` ist eine Eigenschaft, die ein Element im Index klassifiziert. Diese Klassifizierung unterscheidet sich von der "Art"-Klassifizierung, die von der [erweiterten](-search-2x-wds-aqsreference.md) Abfragesyntax verwendet wird. Auf ähnliche Weise können Benutzer jedoch ihre Suchergebnisse verfeinern. Mit der AQS-Art können Benutzer ihre Suchabfrage einschränken, während benutzer mit der Eigenschaft PerceivedType ihr Resultset filtern können.

## <a name="types"></a>Typen

Verwenden Sie die Eigenschaft PerceivedType, um Ihren Dateityp zu klassifizieren, sodass Benutzer ihre Suchergebnisse nach Typ filtern können. Die Ausgabe muss eine der folgenden Zeichenfolgen sein:

-   contact
-   Kommunikation
-   Kommunikation/E-Mail
-   Kommunikation/Kalender
-   communications/task
-   communications/im
-   Dokument
-   Dokument/Hinweis
-   Dokument/Text
-   Dokument/Arbeitsblatt
-   Dokument/Präsentation
-   music
-   images
-   images/picture
-   Images/Video
-   folder
-   Programm

Wenn Sie beispielsweise ein Filter-Add-In für einen neuen Bilddateityp erstellen möchten, müssen Sie Folgendes in Ihrer [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)implementieren:

-   **GetChunk** zum Zurückgeben eines FULLPROPSPEC-Werts, der Folgendes enthält: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue,** um eine PROPVARIANT zurückzugeben, die Folgendes enthält: VT \_ LPWSTR = "images/picture"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Entwickeln von IFilter-Add-Ins](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Entwickeln von Protokollhandlern](-search-2x-wds-phaddins.md)
</dt> <dt>

[Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
