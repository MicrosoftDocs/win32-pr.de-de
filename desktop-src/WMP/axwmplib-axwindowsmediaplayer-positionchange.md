---
title: PositionChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Positions Change-Ereignis tritt auf, wenn die aktuelle Wiedergabe Position innerhalb des Medien Elements geändert wurde.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Positions Change-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354086"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>PositionChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das Positions Change-Ereignis tritt auf, wenn die aktuelle Wiedergabe Position innerhalb des Medien Elements geändert wurde.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ positionchangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ PositionChangeEvent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft    | BESCHREIBUNG                                         |
|-------------|-----------------------------------------------------|
| oldposition | System. doublegibt die alte Position an.<br/> |
| neuposition | System. doublegibt die neue Position an.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird während der Wiedergabe nicht routinemäßig ausgelöst. Sie tritt nur dann auf, wenn die aktuelle Position des Wiedergabe-Medien Elements aktiv geändert wird, z. b. wenn der Benutzer das Seek-handle verschiebt oder wenn Code ausgeführt wird, der einen Wert für iwmpcontrols angibt. **CurrentPosition**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. CurrentPosition (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





