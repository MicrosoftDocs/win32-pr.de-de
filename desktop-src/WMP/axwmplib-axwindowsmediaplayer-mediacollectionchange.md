---
title: Mediacollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das mediacollectionchange-Ereignis tritt auf, wenn die Mediensammlung geändert wird. | Mediacollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- Mediacollectionchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720207de3475544074b87c56686d0a47da97785c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369222"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a>Mediacollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts

Das mediacollectionchange-Ereignis tritt auf, wenn die Mediensammlung geändert wird.

``` syntax
[C#]
private void player_MediaCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_MediaCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.MediaCollectionChange
```

## <a name="event-data"></a>Ereignisdaten

Dieses Ereignis enthält keine Daten.

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

[**AxWindowsMediaPlayer. mediacollection (VB und c#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





