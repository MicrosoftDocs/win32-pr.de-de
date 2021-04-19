---
title: Reference-Element (veraltet)
description: Reference-Element (veraltet)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Windows Media-Metadatendateien, Reference-Element
- Metadatendateien, Reference-Element
- Reference-Element
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342068"
---
# <a name="reference-element-deprecated"></a>Reference-Element (veraltet)

In diesem Thema wird eine Funktion beschrieben, die in der aktuellen Version von Windows Media Metafiles nicht mehr verwendet wird.

Das **Reference** -Element enthält eine Liste mit Verweisen auf URLs. Jedes Element in der Liste hat das Format Ref *xx*  =  *URL*, wobei *xx* eine ganze Zahl und *URL* die URL einer ASF-Datei (Advanced Systems Format) ist.

**Syntax**


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



Die von *xx* dargestellten ganzzahligen müssen in aufsteigender Reihenfolge vorliegen. Das heißt, die Ganzzahl in jeder Zeile muss größer als die ganze Zahl in der vorherigen Zeile sein.

Wenn ein Client Programm ein Verweis Element liest, versucht es, eine Verbindung mit der Mediendatei herzustellen, die durch die erste URL in der Liste repräsentiert wird. Wenn dies fehlschlägt, versucht das Client Programm, eine Verbindung mit der durch die nächste URL in der Liste dargestellten Datei herzustellen. Das Client Programm fährt fort, bis eine erfolgreiche Verbindung hergestellt wurde oder das Ende der Liste erreicht wird. Beachten Sie Folgendes: Wenn das Client Programm erfolgreich eine Verbindung herstellt, liest es keine der nachfolgenden URLs in der Liste.

**Beispiel Code**

Im folgenden Beispiel versucht das Client Programm zuerst, eine Verbindung mit der durch die MMS-URL dargestellten Datei herzustellen. Wenn dies nicht der Fall ist, versucht das Client Programm, eine Verbindung mit der durch die http-URL dargestellten Datei herzustellen.


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a>Bemerkungen

Das Format der ASF-Datei umfasst eine Vielzahl von Medientypen, einschließlich Audiodaten und Videos. Bei ASF-Dateien werden auch mehrere verschiedene Dateinamen Erweiterungen verwendet, einschließlich. WMA und. wmv.

Die von *xx* dargestellten ganzzahligen müssen in aufsteigender Reihenfolge vorliegen. Das heißt, die Ganzzahl in jeder Zeile muss größer als die ganze Zahl in der vorherigen Zeile sein.

Wenn ein Client Programm ein Verweis Element liest, versucht es, eine Verbindung mit der Mediendatei herzustellen, die durch die erste URL in der Liste repräsentiert wird. Wenn dies fehlschlägt, versucht das Client Programm, eine Verbindung mit der durch die nächste URL in der Liste dargestellten Datei herzustellen. Das Client Programm fährt fort, bis eine erfolgreiche Verbindung hergestellt wurde oder das Ende der Liste erreicht wird. Beachten Sie Folgendes: Wenn das Client Programm erfolgreich eine Verbindung herstellt, liest es keine der nachfolgenden URLs in der Liste.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Frühere Versionen von Windows Media-Metadatendateien (veraltet)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




