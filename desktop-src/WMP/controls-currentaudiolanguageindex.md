---
title: Controls. currentaudiolanguageindex
description: Die currentaudiolanguageindex-Eigenschaft gibt den 1-basierten Index an, der der Audiosprache für die Wiedergabe entspricht, oder ruft ihn ab.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Controls. currentaudiolanguageindex-Fenster Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359661"
---
# <a name="controlscurrentaudiolanguageindex"></a>Controls. currentaudiolanguageindex

Die **currentaudiolanguageindex** -Eigenschaft gibt den 1-basierten Index an, der der Audiosprache für die Wiedergabe entspricht, oder ruft ihn ab.

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**). 

## <a name="remarks"></a>Bemerkungen

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft akzeptiert nur 0 oder gibt 0 zurück.

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

[**Controls. currentaudiolanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. getaudiolanguagedescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getaudiolanguageid**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getlanguagename**](controls-getlanguagename.md)
</dt> </dl>

 

 





