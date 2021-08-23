---
title: DomainChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das DomainChange-Ereignis tritt auf, wenn sich die DVD-Domäne ändert. | DomainChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- DomainChange-Ereignis des AxWindowsMediaPlayer-Windows Media Player
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
ms.openlocfilehash: a37f10679225fb893fad8bcf6fc6687021256e305e8c5a08e6ebe96d16b74e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136123"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>DomainChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das DomainChange-Ereignis tritt auf, wenn sich die DVD-Domäne ändert.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft  | BESCHREIBUNG                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | System.StringIndicates die neue Domäne. Mögliche Werte finden Sie im Abschnitt „Hinweise“.<br/> |



 

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die möglichen Werte für die strDomain-Eigenschaft.



| Zeichenfolge            | Beschreibung                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Ausführen der Standardin initialisierung eines DVD-Datenträgers.                     |
| videoManagerMenu  | Anzeigen von Menüs für den gesamten Datenträger. Wird auch als Stammmenü oder topMenu bezeichnet. |
| videoTitleSetMenu | Anzeigen von Menüs für den aktuellen Titelsatz. Wird auch als titleMenu bezeichnet.     |
| title             | Anzeigen des aktuellen Titels.                                        |
| stop              | Der DVD-Navigator befindet sich in der Domäne DVD-Stopp.                         |



 

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

[**IWMPDVD-Schnittstelle (VB und C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





