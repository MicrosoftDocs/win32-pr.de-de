---
title: StringCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgenauflistung ändert. | StringCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- StringCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: 0ceeba7942be4180d02a44ff19d63c10f9bc9df0bba745fdf69bcf10e97c3052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764659"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>StringCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgenauflistung ändert.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft              | Beschreibung                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| pdispStringCollection | System.ObjectDas geänderte Zeichenfolgenauflistungselement. Sie können diese in eine IWMPStringCollection-Schnittstelle umleiten, um darauf zuzugreifen.<br/> |
| lCollectionIndex      | System.Int32Der Index des geänderten Zeichenfolgenauflistungselements.<br/>                                                          |
| change (Ändern)                | WMPLib.WMPStringCollectionChangeEventTypeAn-Enumerationswert, der den Typ der aufgetretenen Änderung angibt.<br/>                 |



 

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

[**IWMPStringCollection-Schnittstelle (VB und C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**WMPStringCollectionChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





