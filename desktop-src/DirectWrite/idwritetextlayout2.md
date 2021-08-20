---
title: IDWriteTextLayout2-Schnittstelle
description: Stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde. | IDWriteTextLayout2-Schnittstelle
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- IDWriteTextLayout2-Schnittstelle – Direkter Schreibzugriff
- IDWriteTextLayout2-Schnittstelle Direct Write , beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff23fea3d1ae4da7c6dba310ed28dfb8c76d65947426f0219e3868f3859c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816260"
---
# <a name="idwritetextlayout2-interface"></a>IDWriteTextLayout2-Schnittstelle

Stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde.

## <a name="members"></a>Member

Die **IDWriteTextLayout2-Schnittstelle** erbt von [**IDWriteTextLayout1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) **IDWriteTextLayout2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteTextLayout2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                | Beschreibung                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | Hier erhalten Sie das aktuelle Schriftartfallbackobjekt. <br/>                                           |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | Gibt an, ob das letzte Wort in der letzten Zeile umschlossen ist.<br/>                    |
| [**GetMetrics**](idwritetextlayout2-getmetrics.md)                                   | Ruft allgemeine Metriken für die formatierte Zeichenfolge ab. <br/>                             |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | Hier erfahren Sie, wie die Glyphen an den Rändern am Rand ausgerichtet sind. <br/>                               |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | Erhalten Sie die bevorzugte Ausrichtung von Glyphen, wenn Sie eine vertikale Leserichtung verwenden.<br/> |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | Wenden Sie ein benutzerdefiniertes Schriftartfallback auf das Layout an.<br/>                                        |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | Legen Sie fest, ob das letzte Wort in der letzten Zeile umschlossen ist. <br/>                   |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | Legen Sie fest, wie die Glyphen an den Rändern am Rand ausgerichtet werden.<br/>                                |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | Legen Sie die bevorzugte Ausrichtung von Glyphen fest, wenn Sie eine vertikale Leserichtung verwenden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

