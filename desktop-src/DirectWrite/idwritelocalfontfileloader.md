---
title: Idschreitelocalfontfileloader-Schnittstelle
description: Eine integrierte Implementierung der idschreitefontfileloader-Schnittstelle, die mit lokalen Schriftart Dateien arbeitet und lokale Schriftart Dateiinformationen aus dem Schriftart Datei-Verweis Schlüssel verfügbar macht.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Idwrite telocalfontfileloader-Schnittstelle direkt schreiben
- Direkter Schreibvorgang der idschreitelocalfontfileloader-Schnittstelle, beschrieben
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
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371185"
---
# <a name="idwritelocalfontfileloader-interface"></a>Idschreitelocalfontfileloader-Schnittstelle

Eine integrierte Implementierung der [**idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) -Schnittstelle, die mit lokalen Schriftart Dateien arbeitet und lokale Schriftart Dateiinformationen aus dem Schriftart Datei-Verweis Schlüssel verfügbar macht. Verweise auf Schriftart Dateien, [**die mithilfe von**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) "" erstellt wurden, verwenden dieses Schriftart Datei Lade Tool.

## <a name="members"></a>Member

Die **idwrite telocalfontfileloader** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idwrite telocalfontfileloader** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idwrite telocalfontfileloader** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                  | BESCHREIBUNG                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Getfilepathfromkey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Ruft den absoluten Schriftart Datei Pfad aus dem Verweis Schlüssel der Schriftart Datei ab.<br/>          |
| [**Getfilepathlängen fromkey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Ruft die Länge des absoluten Dateipfads aus dem Verweis Schlüssel der Schriftart Datei ab.<br/> |
| [**Getlastschreitetimefromkey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Ruft den Zeitpunkt des letzten Schreibzugriffs auf die Datei aus dem Verweis Schlüssel der Schriftart Datei ab.<br/>      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

