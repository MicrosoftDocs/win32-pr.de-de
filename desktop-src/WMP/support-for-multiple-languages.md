---
title: Unterstützung für mehrere Sprachen
description: Unterstützung für mehrere Sprachen
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Media Metadatei-Wiedergabelisten, Unterstützung für mehrere Sprachen
- Metadatei-Wiedergabelisten, Unterstützung für mehrere Sprachen
- Wiedergabelisten, Unterstützung für mehrere Sprachen
- Windows Media Metadatei-Wiedergabelisten, Unterstützung mehrerer Sprachen
- Metadatei-Wiedergabelisten, Unterstützung mehrerer Sprachen
- Wiedergabelisten, Unterstützung mehrerer Sprachen
- Windows Media Metadatei-Wiedergabelisten, Sprachunterstützung
- Metadatei-Wiedergabelisten, Sprachunterstützung
- Wiedergabelisten, Sprachunterstützung
- Unterstützung für mehrere Sprachen
- Unterstützung mehrerer Sprachen
- Sprachenunterstützung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037443"
---
# <a name="support-for-multiple-languages"></a>Unterstützung für mehrere Sprachen

Windows Media Player 9 oder höher unterstützt Windows Media-Metadateien, die mit dem Unicode-Zeichensatz erstellt wurden. Auf diese Weise können Sie mehrsprachige Metadaten in die Metadatei-Wiedergabeliste einschließen. Die folgenden Regeln bestimmen die Verwendung mehrsprachiger Metadaten in Windows Media-Metadateien:

-   Zeichen müssen mithilfe des UTF-8-Codierungs Schemas codiert werden.
-   Die Metadatei-Wiedergabeliste muss **die folgenden Parameter** auf der Wiedergabelisten Ebene enthalten:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Diese Funktion wird nur von Windows Media Player 9 oder höher unterstützt.
-   Wenn die Metadatei-Wiedergabeliste nicht mit UTF-8-Codierung und dem korrekten **param** -Element gespeichert wird, wird Sie mithilfe der Standard Codepage des System Gebiets Schemas auf dem Computer des Benutzers analysiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Param-Element**](param-element.md)
</dt> <dt>

[**Übersicht über Windows Media-Metadatendateien**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




