---
title: IDWriteFactory2-Schnittstelle
description: Die Stammfactoryschnittstelle für alle DirectWrite-Objekte.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Direktes Schreiben der IDWriteFactory1-Schnittstelle
- IDWriteFactory1 interface Direct Write , beschrieben
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370292387f2c42e3f749e24a063e05bb24280ec5c8e8941a430f996fe7f349da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902800"
---
# <a name="idwritefactory2-interface"></a>IDWriteFactory2-Schnittstelle

Die Stammfactoryschnittstelle [](direct-write-portal.md) für alle DirectWrite-Objekte.

## <a name="members"></a>Member

Die **IDWriteFactory1-Schnittstelle** erbt von [**IDWriteFactory1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) **IDWriteFactory2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteFactory1-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CreateCustomRenderingParams**](idwritefactory2-createcustomrenderingparams.md) | Erstellt ein Renderingparameterobjekt mit den angegebenen Eigenschaften.<br/>                            |
| [**CreateFontFallbackBuilder**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | Erstellt ein Schriftartfallback-Generatorobjekt.<br/>                                                         |
| [**CreateGlyphRunAnalysis**](idwritefactory2-createglyphrunanalysis.md)           | Erstellt ein Glyphenlaufanalyseobjekt, das Informationen kapselt, die zum Rendern einer Glyphenlauf verwendet werden.<br/> |
| [**GetSystemFontFallback**](idwritefactory2-getsystemfontfallback.md)             | Erstellt ein Schriftartfallbackobjekt aus der Fallbackliste der Systemschriftart.<br/>                              |
| [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | Diese Methode wird für eine Glyphen-Ausführung aufgerufen, um sie in mehrere Farbglyphenläufe zu übersetzen.<br/>           |



 

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

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

