---
title: Controls. getaudiolanguagedescription-Methode
description: Die getaudiolanguagedescription-Methode ruft die Beschreibung für die Audiosprache ab, die dem angegebenen 1-basierten Index entspricht.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- getaudiolanguagedescription-Methode, Windows Media Player
- getaudiolanguagedescription-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, getaudiolanguagedescription-Methode
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
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354095"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Controls. getaudiolanguagedescription-Methode

Die **getaudiolanguagedescription** -Methode ruft die Beschreibung für die Audiosprache ab, die dem angegebenen 1-basierten Index entspricht.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den einbasierten audiosprachindex angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **Zeichen** folgen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen, und greifen Sie dann einzeln mithilfe eines 1-basierten Indexes auf eine Audiosprache zu.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

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

[**Controls. currentaudiolanguageindex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getaudiolanguageid**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getlanguagename**](controls-getlanguagename.md)
</dt> </dl>

 

 





