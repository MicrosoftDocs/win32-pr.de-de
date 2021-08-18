---
title: Pufferungsereignis des AxWindowsMediaPlayer-Objekts
description: Das Pufferungsereignis tritt auf, wenn Windows Media Player-Steuerelement mit dem Puffern oder Herunterladen beginnt oder beendet wird. | Pufferungsereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Pufferungsereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30cca5d7ebe91859162bd729cc32cc03f36f9e3c59ba4474d41311befcce1d21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765250"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Pufferungsereignis des AxWindowsMediaPlayer-Objekts

Das Pufferungsereignis tritt auf, wenn Windows Media Player-Steuerelement mit dem Puffern oder Herunterladen beginnt oder beendet wird.

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | BESCHREIBUNG                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Start    | System.BooleanS gibt an, ob die Pufferung begonnen oder beendet wurde. Der Wert true gibt an, dass er begonnen hat. Der Wert false gibt an, dass er beendet wurde.<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, um zu bestimmen, wann das Puffern oder Herunterladen gestartet oder beendet wird. Sie können denselben Ereignisblock für beide Fälle verwenden und *IWMPNetwork testen.* **bufferingProgress** und *IWMPNetwork*. **downloadProgress,** um zu bestimmen, Windows Media Player derzeit Inhalte puffert oder herunterladt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.bufferingProgress (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.downloadProgress (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





