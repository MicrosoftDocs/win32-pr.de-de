---
title: MediaCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaCollectionChange-Ereignis tritt auf, wenn sich die Mediensammlung ändert. | MediaCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- MediaCollectionChange-Ereignis des AxWindowsMediaPlayer-Windows Media Player
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
ms.openlocfilehash: 8a3019bab6f71c54688b2c47fec8e8bf94dfd5809797cbe1b875d7f7c23818c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119378290"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a>MediaCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das MediaCollectionChange-Ereignis tritt auf, wenn sich die Mediensammlung ändert.

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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.mediaCollection (VB und C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





