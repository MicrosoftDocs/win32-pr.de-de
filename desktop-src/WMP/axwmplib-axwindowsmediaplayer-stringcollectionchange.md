---
title: Stringcollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert. | Stringcollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Stringcollectionchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352015"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>Stringcollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts

Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert.

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ stringcollectionchangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ stringcollectionchangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft              | BESCHREIBUNG                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| pdispstringcollection | System. objectdas Zeichen folgen Auflistungs Element, das geändert wurde. Sie können dies in eine iwmpstringcollection-Schnittstelle umwandeln, um darauf zuzugreifen.<br/> |
| lcollectionindex      | System. Int32The-Index des Elements der Zeichen folgen Auflistung, das geändert wurde.<br/>                                                          |
| change (Ändern)                | WMPLib. wmpstringcollectionchangeeventtypea-Enumerationswert, der den Typ der aufgetretenen Änderung angibt.<br/>                 |



 

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

[**Iwmpstringcollection-Schnittstelle (VB und c#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Wmpstringcollectionchangeeventtype**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





