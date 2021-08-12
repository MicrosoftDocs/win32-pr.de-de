---
title: Player.MediaError-Ereignis
description: Das MediaError-Ereignis tritt auf, wenn das Medienobjekt eine Fehlerbedingung aufweist.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- MediaError-Ereignis Windows Media Player
- MediaError-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , MediaError-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1eb94d245f0b0a91786b2b1a7b677429cc9040d8cbb1372164bf6e7ed209d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572840"
---
# <a name="playermediaerror-event"></a>Player.MediaError-Ereignis

Das **MediaError-Ereignis** tritt auf, wenn das **Medienobjekt** eine Fehlerbedingung aufweist.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaObject* 
</dt> <dd>

**Medienobjekt,** das eine Fehlerbedingung aufweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





