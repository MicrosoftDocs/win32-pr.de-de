---
title: Controls.currentAudioLanguage
description: Die currentAudioLanguage-Eigenschaft gibt den Gebietsschemabezeichner (LCID) der Audiosprache für die Wiedergabe an oder ruft sie ab.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controls.currentAudioLanguage Windows Media Player
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
ms.openlocfilehash: 63c5eb53c9f408a9d50a7f738434e5dcd30fc804970b3e1ea95c985c90d62063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750612"
---
# <a name="controlscurrentaudiolanguage"></a>Controls.currentAudioLanguage

Die **currentAudioLanguage-Eigenschaft** gibt den Gebietsschemabezeichner (LCID) der Audiosprache für die Wiedergabe an oder ruft sie ab.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/Schreibnummer (**long**). 

## <a name="remarks"></a>Hinweise

Eine LCID identifiziert eindeutig einen bestimmten Sprachdialekt, der als Gebietsschema bezeichnet wird.

Für Windows Medienbasierte Inhalte unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Wenn Sie mit DVD-Inhalten arbeiten, führt die Angabe einer LCID dazu, dass die erste verfügbare Audiospur mit der angegebenen Sprach-ID ausgewählt wird.

**Windows Media Player 10 Mobile:** Diese Eigenschaft akzeptiert nur die sprachneutrale LCID (0) oder gibt sie zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls.audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





