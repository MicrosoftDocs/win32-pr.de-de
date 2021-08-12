---
title: MSWMExt-Parameter (veraltet)
description: MSWMExt-Parameter (veraltet)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows Medienmetadateien,MSWMExt-Parameter
- Metafiles,MSWMExt-Parameter
- MSWMExt-Parameter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ec80530f95d4429769758488e5a2b24b0268c57255248c7685a0d00125aa130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574597"
---
# <a name="mswmext-parameter-deprecated"></a>MSWMExt-Parameter (veraltet)

Der *MSWMExt-Parameter* gibt einem Clientprogramm das Format einer Datei an, auf die verwiesen wird.

**Syntax**


```XML

URL?MSWMExt=.
ext
```



**Beispielcode**


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a>Hinweise

Clientprogramme verwenden manchmal eine Dateierweiterung oder einen MIME-Typ, um zu bestimmen, ob eine Mediendatei als Stream gerendert, die Datei nach einem vollständigen Download gerendert oder überhaupt nicht gerendert werden soll. Wenn ein Clientprogramm nicht bestimmen kann, wie eine Mediendatei basierend auf der Dateierweiterung oder dem MIME-Typ behandelt werden soll, kann es bestimmen, wie die Datei behandelt werden soll, indem der *MSWMExt-Parameter* überprüft wird. Beispielsweise könnte der Client die Datei so behandeln, als hätte sie eine Erweiterung, die dem Wert des *MSWMExt-Parameters* entspricht. Weitere Informationen zu MIME-Typen und Dateinamenerweiterungen finden Sie unter [Dateierweiterungen](file-name-extensions.md). Weitere Informationen zum *MSWMExt-Parameter* finden Sie im artikel [236895](https://support.microsoft.com/kb/236895) in der Microsoft Knowledge Base.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Frühere Versionen von Windows Medienmetadateien (veraltet)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




