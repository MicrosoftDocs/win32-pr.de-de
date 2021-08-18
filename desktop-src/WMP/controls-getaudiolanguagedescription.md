---
title: Controls.getAudioLanguageDescription-Methode
description: Die getAudioLanguageDescription-Methode ruft die Beschreibung für die Audiosprache ab, die dem angegebenen einbasierten Index entspricht.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- getAudioLanguageDescription-Windows Media Player
- getAudioLanguageDescription-Methode Windows Media Player , Controls-Klasse
- Steuert die Windows Media Player , getAudioLanguageDescription-Methode
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aa5f7b5c0ad72ff13b571505283b243bd62d79ebc4339717ed8283cccb2a5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997500"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Controls.getAudioLanguageDescription-Methode

Die **getAudioLanguageDescription-Methode** ruft die Beschreibung für die Audiosprache ab, die dem angegebenen einbasierten Index entspricht.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Zahl** (**long**), die den 1-basierten Audiosprachindex an gibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **Zeichenfolgenwert** zurück.

## <a name="remarks"></a>Hinweise

Für Windows Medienbasierte Inhalte unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Verwenden Sie **die audioLanguageCount-Eigenschaft,** um die Anzahl der unterstützten Audiosprachen zu erhalten, und greifen Sie dann einzeln mithilfe eines einbasierten Indexes auf eine Audiosprache zu.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

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

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





