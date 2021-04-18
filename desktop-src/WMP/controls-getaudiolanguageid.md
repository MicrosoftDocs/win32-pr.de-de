---
title: Controls. getaudiolanguageid-Methode
description: Die getaudiolanguageid-Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex ab.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- getaudiolanguageid-Methode, Windows Media Player
- getaudiolanguageid-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, getaudiolanguageid-Methode
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
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352912"
---
# <a name="controlsgetaudiolanguageid-method"></a>Controls. getaudiolanguageid-Methode

Die **getaudiolanguageid** -Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den audiosprachindex angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück.

## <a name="remarks"></a>Bemerkungen

Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer die sprachneutrale LCID (0) zurück.

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

[**Controls. getaudiolanguagedescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getlanguagename**](controls-getlanguagename.md)
</dt> </dl>

 

 





