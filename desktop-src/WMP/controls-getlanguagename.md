---
title: Controls. getlanguagename-Methode
description: Die getlanguagename-Methode ruft den Namen der Audiosprache mit dem angegebenen Gebiets Schema Bezeichner (LCID) ab.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- getlanguagename-Methode, Windows-Media Player
- getlanguagename-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, getlanguagename-Methode
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365578"
---
# <a name="controlsgetlanguagename-method"></a>Controls. getlanguagename-Methode

Die **getlanguagename** -Methode ruft den Namen der Audiosprache mit dem angegebenen Gebiets Schema Bezeichner (LCID) ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LCID* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die die LCID angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

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

[**Controls. getaudiolanguageid**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





