---
title: Player.Buffering-Ereignis
description: Das Pufferungsereignis tritt auf, wenn das Windows Media Player-Steuerelement mit dem Puffern oder Herunterladen beginnt oder beendet. | Player.Buffering-Ereignis
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Pufferereignis Windows Media Player
- Pufferereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , Pufferungsereignis
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ac382315d37fcd36a5470ae3f7f07bf4454687b660a2311498b5b0866e32b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747521"
---
# <a name="playerbuffering-event"></a>Player.Buffering-Ereignis

Das **Pufferungsereignis** tritt auf, wenn das Windows Media Player-Steuerelement mit dem Puffern oder Herunterladen beginnt oder beendet.

## <a name="syntax"></a>Syntax


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

**Boolescher Wert,** der einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG            |
|-------|------------------------|
| true  | Die Pufferung wurde gestartet. |
| false | Die Pufferung wurde beendet.   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, um zu bestimmen, wann das Puffern oder Herunterladen gestartet oder beendet wird. Sie können den gleichen Ereignisblock für beide Fälle verwenden und *Network* testen. **bufferingProgress** und *Network*. **downloadProgress,** um zu bestimmen, ob Windows Media Player derzeit Inhalt puffert oder herunterlädt.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Network.bufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Network.downloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





