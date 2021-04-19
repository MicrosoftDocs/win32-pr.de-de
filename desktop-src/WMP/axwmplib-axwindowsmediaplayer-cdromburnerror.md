---
title: Cdromburnerror-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromburnerror-Ereignis tritt auf, wenn während eines CD-Brennvorgangs ein generischer Fehler auftritt.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Cdromburnerror-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364024"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>Cdromburnerror-Ereignis des AxWindowsMediaPlayer-Objekts

Das cdromburnerror-Ereignis tritt auf, wenn während eines CD-Brennvorgangs ein generischer Fehler auftritt.

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnerroreventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnerrorevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft   | BESCHREIBUNG                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| hrError    | **System. Int32** Der Fehler, der das Ereignis ausgelöst hat.<br/>                                               |
| pcdromburn | WMPLib. iwmpcdromburndie-Schnittstelle, die den Brennvorgang darstellt, der den Fehler ausgelöst hat.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um medienspezifische Fehler zu erfassen, behandeln Sie AxWMPLib. \_ Wmpocxevents \_ cdromburnmediaerror-Ereignis.

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

[**AxWindowsMediaPlayer. cdromburnmediaerror-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





