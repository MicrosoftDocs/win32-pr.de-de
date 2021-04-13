---
title: Mswap-Parameter (veraltet)
description: Mswap-Parameter (veraltet)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows Media Metafiles, mswap-Parameter
- Metafiles, mswap-Parameter
- Mswap-Parameter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389962"
---
# <a name="mswmext-parameter-deprecated"></a>Mswap-Parameter (veraltet)

Der *mswap* -Parameter gibt einem Client Programm das Format einer referenzierten Datei an.

**Syntax**


```XML

URL?MSWMExt=.
ext
```



**Beispiel Code**


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a>Bemerkungen

Client Programme verwenden manchmal eine Dateinamenerweiterung oder einen MIME-Typ, um zu bestimmen, ob eine Mediendatei als Stream gerenbt werden soll, ob die Datei nach einem vollständigen Download gerenbt werden soll oder ob die Datei überhaupt nicht gerenbt wird. Wenn ein Client Programm nicht bestimmen kann, wie eine Mediendatei auf der Grundlage der Dateinamenerweiterung oder des MIME-Typs behandelt werden soll, kann er bestimmen, wie die Datei behandelt werden soll, indem der *mswap* -Parameter überprüft wird. Beispielsweise kann der Client die Datei so behandeln, als hätte Sie eine Erweiterung, die gleich dem Wert des *mswap* -Parameters ist. Weitere Informationen zu MIME-Typen und Dateinamen Erweiterungen finden Sie unter [Dateinamen Erweiterungen](file-name-extensions.md). Weitere Informationen zum *mswap* -Parameter finden Sie im Artikel [236895](https://support.microsoft.com/kb/236895) in der Microsoft Knowledge Base.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Frühere Versionen von Windows Media-Metadatendateien (veraltet)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




