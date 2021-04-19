---
title: Player. audiolanguagechange-Ereignis
description: Das audiolanguagechange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert. | Player. audiolanguagechange-Ereignis
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Media Player für audiolanguagechange-Ereignisfenster
- Audiolanguagechange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, audiolanguagechange-Ereignis
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373724"
---
# <a name="playeraudiolanguagechange-event"></a>Player. audiolanguagechange-Ereignis

Das **audiolanguagechange** -Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert.

## <a name="syntax"></a>Syntax


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LangID* 
</dt> <dd>

**Number** (**Long**), der den neuen Gebiets Schema Bezeichner (LCID) angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten Microsoft JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls. currentaudiolanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





