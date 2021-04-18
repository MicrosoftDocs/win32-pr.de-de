---
title: Player. buffereing-Ereignis
description: Das bufferingereignis tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet. | Player. buffereing-Ereignis
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Media Player für die Pufferung von Ereignis Fenstern
- Puffer Ereignis Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, pufferungsereignis
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
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358044"
---
# <a name="playerbuffering-event"></a>Player. buffereing-Ereignis

Das **bufferingereignis** tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet.

## <a name="syntax"></a>Syntax


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Starten* 
</dt> <dd>

**Boolescher** Wert, der einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG            |
|-------|------------------------|
| true  | Die Pufferung wurde gestartet. |
| false | Die Pufferung wurde beendet.   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, um zu bestimmen, wann ein-oder herunterladen gestartet oder beendet wird. Sie können den gleichen Ereignisblock für beide Fälle und das Test *Netzwerk* verwenden. **BufferingProgress** und *Network*. **Download Progress** , um zu bestimmen, ob der Inhalt von Windows Media Player derzeit gepuffert oder heruntergeladen wird.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Network. BufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Network. Download Progress**](network-downloadprogress.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





