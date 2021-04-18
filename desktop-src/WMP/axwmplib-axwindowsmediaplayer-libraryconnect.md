---
title: Libraryconnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das libraryconnect-Ereignis tritt auf, wenn eine Bibliothek verfügbar wird.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Libraryconnect-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371720"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a>Libraryconnect-Ereignis des AxWindowsMediaPlayer-Objekts

Das libraryconnect-Ereignis tritt auf, wenn eine Bibliothek verfügbar wird.

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ libraryconnecteventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ libraryconnectevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| plibrary | **WMPLib. iwmplibrary** Die-Schnittstelle, die die verbundene Bibliothek darstellt.<br/> |



 

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

 

 





