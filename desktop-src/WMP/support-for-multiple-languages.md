---
title: Unterstützung für mehrere Sprachen
description: Unterstützung für mehrere Sprachen
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Wiedergabelisten von Medienmetadateien,Unterstützung für mehrere Sprachen
- Metadateiwiedergabelisten,Unterstützung für mehrere Sprachen
- Wiedergabelisten,Unterstützung für mehrere Sprachen
- Windows Wiedergabelisten von Medienmetadateien, Unterstützung mehrerer Sprachen
- Metadateiwiedergabelisten, Unterstützung mehrerer Sprachen
- Wiedergabelisten,Unterstützung mehrerer Sprachen
- Windows Wiedergabelisten von Medienmetadateien, Sprachunterstützung
- Metafile-Wiedergabelisten, Sprachunterstützung
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
ms.openlocfilehash: a04fc9f3a1f6d481ad88e85323c7bdd253ddde7dd2f020de2ea42e77c83c4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002070"
---
# <a name="support-for-multiple-languages"></a>Unterstützung für mehrere Sprachen

Windows Media Player 9-Serie oder höher unterstützt Windows Medienmetadateien, die mit dem Unicode-Zeichensatz erstellt wurden. Dadurch können Sie mehrsprachige Metadaten in Ihre Metadateiwiedergabeliste einreihen. Die folgenden Regeln regeln die Verwendung mehrsprachiger Metadaten in Windows Medienmetadateien:

-   Zeichen müssen mit dem UTF-8-Codierungsschema codiert werden.
-   Die Metadateiwiedergabeliste muss den folgenden **PARAM auf** Wiedergabelistenebene enthalten:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Nur Windows Media Player 9-Serie oder höher unterstützt diese Funktionalität.
-   Wenn die Metadateiwiedergabeliste nicht mit UTF-8-Codierung und dem richtigen **PARAM-Element** gespeichert wird, wird sie mithilfe der Standardcodepage des Systemschemas des Computers des Benutzers analysiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**PARAM-Element**](param-element.md)
</dt> <dt>

[**Windows Übersicht über Medienmetadateien**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




