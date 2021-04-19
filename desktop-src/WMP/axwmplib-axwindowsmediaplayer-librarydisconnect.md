---
title: Librarydisconnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das librarydisconnect-Ereignis tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Librarydisconnect-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373944"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>Librarydisconnect-Ereignis des AxWindowsMediaPlayer-Objekts

Das librarydisconnect-Ereignis tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ librarydisconnecteventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ librarydisconnectevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| plibrary | **WMPLib. iwmplibrary** Die-Schnittstelle, die die getrennte Bibliothek darstellt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt nicht für die lokale Bibliothek auf.

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

[**Iwmplibrary-Schnittstelle (VB und c#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





