---
title: Cdromburnmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromburnmediaerror-Ereignis tritt auf, wenn beim Brennen eines einzelnen Medien Elements auf einer CD ein Fehler auftritt.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Cdromburnmediaerror-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365148"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Cdromburnmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts

Das cdromburnmediaerror-Ereignis tritt auf, wenn beim Brennen eines einzelnen Medien Elements auf einer CD ein Fehler auftritt.

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnmediaerroreventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnmediaerrorevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft   | BESCHREIBUNG                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pcdromburn | WMPLib. iwmpcdromburndie-Schnittstelle, die den Brennvorgang darstellt, der den Fehler ausgelöst hat.<br/>               |
| pmedia     | System. objectdas Medien Element, das den Fehler ausgelöst hat. Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um generische Fehler zu erfassen, behandeln Sie AxWMPLib. \_ Wmpocxevents \_ cdromburnerror-Ereignis.

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

[**AxWindowsMediaPlayer. cdromburnerror-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





