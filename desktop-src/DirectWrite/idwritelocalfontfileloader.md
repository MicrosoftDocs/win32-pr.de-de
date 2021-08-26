---
title: IDWriteLocalFontFileLoader-Schnittstelle
description: Eine integrierte Implementierung der IDWriteFontFileLoader-Schnittstelle, die für lokale Schriftartdateien verwendet wird und lokale Schriftartdateiinformationen aus dem Schriftartdateiverweisschlüssel verfügbar macht.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- IDWriteLocalFontFileLoader-Schnittstelle – Direkter Schreibzugriff
- IDWriteLocalFontFileLoader-Schnittstelle Direct Write , beschrieben
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa073b0d39e5dfbcdb90f2cd67db5f09a04e21c3e36790d4d841e5719490c753
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048690"
---
# <a name="idwritelocalfontfileloader-interface"></a>IDWriteLocalFontFileLoader-Schnittstelle

Eine integrierte Implementierung der [**IDWriteFontFileLoader-Schnittstelle,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) die für lokale Schriftartdateien verwendet wird und lokale Schriftartdateiinformationen aus dem Schriftartdateiverweisschlüssel verfügbar macht. Schriftartdateiverweise, die mit [**CreateFontFileReference erstellt wurden,**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) verwenden dieses Schriftartdateilader.

## <a name="members"></a>Member

Die **IDWriteLocalFontFileLoader-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteLocalFontFileLoader** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteLocalFontFileLoader-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                  | BESCHREIBUNG                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Erhält den absoluten Schriftartdateipfad aus dem Schriftartdateiverweisschlüssel.<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Erhält die Länge des absoluten Dateipfads aus dem Verweisschlüssel der Schriftartdatei.<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Erhält den Zeitpunkt des letzten Schreibzugriffs der Datei aus dem Verweisschlüssel der Schriftartdatei.<br/>      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

