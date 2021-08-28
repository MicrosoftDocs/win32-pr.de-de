---
title: LibraryConnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das LibraryConnect-Ereignis tritt auf, wenn eine Bibliothek verfügbar wird.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- LibraryConnect-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: 940eed16004009e928309ae1a2e5d8f792b9fd0cb36fe8e836abfefb89e3ab95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123950"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a>LibraryConnect-Ereignis des AxWindowsMediaPlayer-Objekts

Das LibraryConnect-Ereignis tritt auf, wenn eine Bibliothek verfügbar wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, die die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | Beschreibung                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib.IWMPLibrary** Die Schnittstelle, die die Bibliothek darstellt, die verbunden ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt nicht für die lokale Bibliothek auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPLibrary-Schnittstelle (VB und C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





