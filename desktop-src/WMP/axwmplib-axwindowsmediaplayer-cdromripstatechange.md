---
title: Cdromripstatechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromripstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-einreißen-Vorgangs ändert.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Cdromripstatechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373558"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a>Cdromripstatechange-Ereignis des AxWindowsMediaPlayer-Objekts

Das cdromripstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-einreißen-Vorgangs ändert.

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripstatechangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripstatechangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft  | BESCHREIBUNG                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| pcdromrip | WMPLib. iwmpcdromripdie Schnittstelle, die den einreißen-Vorgang darstellt, der den Fehler ausgelöst hat.<br/> |
| wmprs     | WMPLib. wmpripstateder Enumerationswert, der den neuen Zustand angibt.<br/>                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromrip-Schnittstelle (VB und c#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Wmpripstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





