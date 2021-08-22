---
title: LibraryDisconnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das LibraryDisconnect-Ereignis tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- LibraryDisconnect-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a032dc95a68430768b0f2aa109a56dae80cdaecb14b67eb5dbf6b2657cdd5107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136003"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>LibraryDisconnect-Ereignis des AxWindowsMediaPlayer-Objekts

Das LibraryDisconnect-Ereignis tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, die die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | Beschreibung                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib.IWMPLibrary** Die Schnittstelle, die die bibliothek darstellt, die getrennt wurde.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt nicht für die lokale Bibliothek auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPLibrary-Schnittstelle (VB und C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





