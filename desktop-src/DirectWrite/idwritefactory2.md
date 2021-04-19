---
title: IDWriteFactory2-Schnittstelle
description: Die Root Factory-Schnittstelle für alle DirectWrite-Objekte.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- IDWriteFactory1 Interface Direct Write
- IDWriteFactory1 Interface Direct Write, beschrieben
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
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339983"
---
# <a name="idwritefactory2-interface"></a>IDWriteFactory2-Schnittstelle

Die Root Factory-Schnittstelle für alle [DirectWrite](direct-write-portal.md) -Objekte.

## <a name="members"></a>Member

Die **IDWriteFactory1** -Schnittstelle erbt von [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1). **IDWriteFactory2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteFactory1** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**"Kreatecustomrenderingpara"**](idwritefactory2-createcustomrenderingparams.md) | Erstellt ein Renderparameter-Objekt mit den angegebenen Eigenschaften.<br/>                            |
| [**"Kreatefontfallbackbuilder"**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | Erstellt ein Schriftart Fall Back Builder-Objekt.<br/>                                                         |
| [**"Kreateglyphrunanalysis"**](idwritefactory2-createglyphrunanalysis.md)           | Erstellt ein Symbol zum Ausführen von Symbolen, das Informationen kapselt, die zum renderischen Ausführen von Symbolen verwendet werden.<br/> |
| [**Getsystemfontfallback**](idwritefactory2-getsystemfontfallback.md)             | Erstellt ein Schriftart Fall Back Objekt aus der System Schriftart-fallbackliste.<br/>                              |
| [**Translatecolorglyphrun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | Diese Methode wird für eine Glyphe-Ausführung aufgerufen, um Sie in mehrere Farb Symbol Ausführungen umzuwandeln.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**Idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

