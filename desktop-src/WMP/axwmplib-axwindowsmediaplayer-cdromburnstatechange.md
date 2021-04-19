---
title: Cdromburnstatechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromburnstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-Brennvorgangs ändert.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Cdromburnstatechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355855"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>Cdromburnstatechange-Ereignis des AxWindowsMediaPlayer-Objekts

Das cdromburnstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-Brennvorgangs ändert.

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnstatechangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnstatechangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft   | BESCHREIBUNG                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pcdromburn | WMPLib. iwmpcdromburndie-Schnittstelle, die den Brennvorgang darstellt, der den Fehler ausgelöst hat.<br/> |
| wmpsb      | WMPLib. wmpburnstateder Enumerationswert, der den neuen Zustand angibt.<br/>                         |



 

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

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Wmpburnstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





