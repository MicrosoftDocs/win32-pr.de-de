---
title: Referenz zu Windows Media-Metadateien
description: Referenz zu Windows Media-Metadateien
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Media-Metadateien, Referenz
- Metadatendateien, Referenz
- Referenz für Windows Media-Metadatendateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036926"
---
# <a name="windows-media-metafile-reference"></a>Referenz zu Windows Media-Metadateien

Dieser Verweis dokumentiert Elemente und Dateinamen Erweiterungen für Windows Media-Metadatendateien. Der Verweis ist in die folgenden Abschnitte unterteilt.



| `Section`                                                                                    | BESCHREIBUNG                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Verweis auf Windows Media-Metadateielemente](windows-media-metafile-elements-reference.md) | Dokumentiert Metadatei-Elemente, einschließlich Definitionen, Attribute und deren Werte, sowie spezielle Bedingungen, die sich auf die einzelnen Elemente beziehen. |
| [Dateinamenerweiterungen](file-name-extensions.md)                                           | Dokumentiert Dateinamen Erweiterungen für Metadateien mit Regeln und Richtlinien zur Verwendung.                                                  |



 

Windows Media-Metadateien sind Textdateien, die Informationen über einen Dateistream und seine Präsentation bereitstellen. Die Metadatendateien basieren auf der Syntax von Extensible Markup Language (XML) und bestehen aus verschiedenen XML-ähnlichen Elementen mit ihren Tags und Attributen. Jedes Element definiert eine Einstellung oder Aktion für Streaming-Medien.

Es sind zwei Sätze von Element Tags für Metadateien verfügbar. Client seitige Metadateien haben einen Satz von Elementen, und serverseitige Metadateien verfügen über einen anderen Satz von Elementen.

Wenn ein Elementtag keine untergeordneten Elemente hat (die Elemente, die sich in einem anderen Element ändern oder befinden), kann ein einzelner Schrägstrich (/) am Ende des öffnenden Tags anstelle eines Endtags verwendet werden. Wenn untergeordnete Elemente nicht zwischen dem öffnenden und dem schließenden Tag für ein Element angezeigt werden, sind Sie keine untergeordneten Elemente für dieses Element und werden ignoriert, oder es wird ein Fehler in der Syntax der Metadatei verursacht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Windows Media-Metadateien**](about-windows-media-metafiles.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Media-Metadateien**](windows-media-metafiles.md)
</dt> </dl>

 

 




