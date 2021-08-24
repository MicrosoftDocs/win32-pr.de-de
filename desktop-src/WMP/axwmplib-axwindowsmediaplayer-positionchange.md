---
title: PositionChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das PositionChange-Ereignis tritt auf, wenn die aktuelle Wiedergabeposition innerhalb des Medienelements geändert wurde.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- PositionChange-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269d83c92687b5debda8b70fb4d6710b55eebd5476153759ebad36e5d17657d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764680"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>PositionChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das PositionChange-Ereignis tritt auf, wenn die aktuelle Wiedergabeposition innerhalb des Medienelements geändert wurde.

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft    | Beschreibung                                         |
|-------------|-----------------------------------------------------|
| oldPosition | System.DoubleSpecifiert die alte Position.<br/> |
| newPosition | System.DoubleSpecifiert die neue Position.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis wird während der Wiedergabe nicht routinemäßig ausgelöst. Sie tritt nur auf, wenn etwas die aktuelle Position des wiedergegebenen Medienelements aktiv ändert, z. B. wenn der Benutzer das Suchhandle verschiebt oder wenn Code ausgeführt wird, der einen Wert für IWMPControls angibt. **currentPosition**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentPosition (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





