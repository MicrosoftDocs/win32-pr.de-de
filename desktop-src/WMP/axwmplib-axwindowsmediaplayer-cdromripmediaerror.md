---
title: Cdromripmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromripmediaerror-Ereignis tritt auf, wenn ein Fehler auftritt, während ein einzelner Track-Vorgang von einer CD durchgeführt wird.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Cdromripmediaerror-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367510"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Cdromripmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts

Das cdromripmediaerror-Ereignis tritt auf, wenn ein Fehler auftritt, während ein einzelner Track-Vorgang von einer CD durchgeführt wird.

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripmediaerroreventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripmediaerrorevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft  | BESCHREIBUNG                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| pcdromrip | WMPLib. iwmpcdromripdie Schnittstelle, die den einreißen-Vorgang darstellt, der den Fehler ausgelöst hat.<br/>                |
| pmedia    | System. objectdas Medien Element, das den Fehler ausgelöst hat. Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.<br/> |



 

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

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





