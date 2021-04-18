---
title: Domainchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das domainchange-Ereignis tritt auf, wenn die DVD-Domäne geändert wird. | Domainchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Das domainchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360979"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Domainchange-Ereignis des AxWindowsMediaPlayer-Objekts

Das domainchange-Ereignis tritt auf, wenn die DVD-Domäne geändert wird.

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ domainchangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ domainchangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft  | BESCHREIBUNG                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| Domäne | System. stringindikiert die neue Domäne. Mögliche Werte finden Sie im Abschnitt „Hinweise“.<br/> |



 

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle sind die möglichen Werte für die Eigenschaft "Eigenschaft" (Eigenschaft) aufgeführt.



| Zeichenfolge            | Beschreibung                                                          |
|-------------------|----------------------------------------------------------------------|
| FirstPlay         | Die Standard Initialisierung einer DVD-CD wird durchgeführt.                     |
| videomanagermenu  | Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "Root Menu" oder "topmenu" bezeichnet. |
| videotitlesetmenu | Anzeigen von Menüs für den aktuellen Titel Satz. Wird auch als titlemenu bezeichnet.     |
| title             | Anzeigen des aktuellen Titels.                                        |
| stop              | Der DVD-Navigator befindet sich in der DVD-stoppdomäne.                         |



 

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

[**Iwmpdvd-Schnittstelle (VB und c#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





