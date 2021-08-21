---
title: Player.AudioLanguageChange-Ereignis
description: Das AudioLanguageChange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert. | Player.AudioLanguageChange-Ereignis
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- AudioLanguageChange-Ereignis Windows Media Player
- AudioLanguageChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , AudioLanguageChange-Ereignis
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
ms.openlocfilehash: 9642f7831fda827b5e64ccff4f4b5d94ea3ef921c50108ad24f38e3c8ec5310a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835858"
---
# <a name="playeraudiolanguagechange-event"></a>Player.AudioLanguageChange-Ereignis

Das **AudioLanguageChange-Ereignis** tritt auf, wenn sich die aktuelle Audiosprache ändert.

## <a name="syntax"></a>Syntax


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Langid* 
</dt> <dd>

**Number** (**long**), die den neuen Gebietsschemabezeichner (LCID) angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine LCID identifiziert eindeutig einen bestimmten Sprachdialekt, der als Gebietsschema bezeichnet wird.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten Microsoft JScript-Datei aufgerufen oder an eine Methode übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





