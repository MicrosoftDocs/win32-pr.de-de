---
title: Controls.getAudioLanguageID-Methode
description: Die getAudioLanguageID-Methode ruft den Locale Identifier (LCID) für einen angegebenen Audiosprachindex ab.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- getAudioLanguageID-Windows Media Player
- getAudioLanguageID-Methode Windows Media Player , Controls-Klasse
- Steuert die Windows Media Player , getAudioLanguageID-Methode
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2352162d810ca75aeeee6db1c3d59c297b85414be46a365909c4ed56af179f8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119339"
---
# <a name="controlsgetaudiolanguageid-method"></a>Controls.getAudioLanguageID-Methode

Die **getAudioLanguageID-Methode** ruft den Locale Identifier (LCID) für einen angegebenen Audiosprachindex ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**) gibt den Audiosprachindex an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** **(long) zurück.**

## <a name="remarks"></a>Hinweise

Eine LCID identifiziert eindeutig einen bestimmten Sprachdialekt, der als "Locale" bezeichnet wird.

Für Windows Medienbasierte Inhalte unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer die sprachneutrale LCID (0) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls.audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





