---
title: Controls. currentaudiolanguage
description: Die currentaudiolanguage-Eigenschaft gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) der Audiosprache für die Wiedergabe an oder ruft ihn ab.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Steuerelemente. currentaudiolanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365521"
---
# <a name="controlscurrentaudiolanguage"></a>Controls. currentaudiolanguage

Die **currentaudiolanguage** -Eigenschaft gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) der Audiosprache für die Wiedergabe an oder ruft ihn ab.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**). 

## <a name="remarks"></a>Bemerkungen

Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Beim Arbeiten mit DVD-Inhalten bewirkt die Angabe einer LCID, dass die erste verfügbare Audiospur mit der angegebenen Sprach-ID ausgewählt wird.

**Windows Media Player 10 Mobile:** Diese Eigenschaft akzeptiert nur die sprachneutrale LCID (0) oder gibt Sie zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls. audiolanguagecount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. currentaudiolanguageindex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getaudiolanguagedescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getaudiolanguageid**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getlanguagename**](controls-getlanguagename.md)
</dt> </dl>

 

 





