---
title: IDWriteTextAnalyzer2-Schnittstelle
description: Analysiert verschiedene Texteigenschaften für die komplexe Skriptverarbeitung.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- IDWriteTextAnalyzer2-Schnittstelle – Direct Write
- IDWriteTextAnalyzer2-Schnittstelle Direct Write , beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a76d4b4b7c2ef09f82834ed2e7f40ee89d2ab80bd0595db62790f38831b86fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075570"
---
# <a name="idwritetextanalyzer2-interface"></a>IDWriteTextAnalyzer2-Schnittstelle

Analysiert verschiedene Texteigenschaften für die komplexe Skriptverarbeitung.

## <a name="members"></a>Member

Die **IDWriteTextAnalyzer2-Schnittstelle** erbt von [**IDWriteTextAnalyzer1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) **IDWriteTextAnalyzer2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteTextAnalyzer2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                    | Beschreibung                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**CheckTypographicFeature**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Überprüft, ob ein typografisches Feature für ein Glyphen oder eine Gruppe von Glyphen verfügbar ist.<br/> |
| [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Gibt eine 2x3-Transformationsmatrix für den jeweiligen Winkel zurück, um die Glyphenlauf zu zeichnen.<br/> |
| [**GetTypographicFeatures**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Gibt eine vollständige Liste der OpenType-Features zurück, die für ein Skript oder eine Schriftart verfügbar sind.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

