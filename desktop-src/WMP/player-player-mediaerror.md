---
title: Player. MediaError-Ereignis
description: Das MediaError-Ereignis tritt auf, wenn das Medienobjekt einen Fehlerzustand aufweist.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Media Player "MediaError-Ereignisfenster"
- MediaError-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, MediaError-Ereignis
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
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372595"
---
# <a name="playermediaerror-event"></a>Player. MediaError-Ereignis

Das **MediaError** -Ereignis tritt auf, wenn das **Medien** Objekt einen Fehlerzustand aufweist.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediaobject* 
</dt> <dd>

Ein **Medien** Objekt, das über eine Fehlerbedingung verfügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





