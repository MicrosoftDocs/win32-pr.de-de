---
title: Warnungsereignis des AxWindowsMediaPlayer-Objekts
description: Das Warnungsereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Warnungsereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18925236148a508e66bb34e83f7ddb69f0cb59d87c98dfe0188f780ea2fc3605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004000"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>Warnungsereignis des AxWindowsMediaPlayer-Objekts

Das Warnungsereignis ist für die zukünftige Verwendung reserviert.

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ WarningEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft    | Beschreibung                                |
|-------------|--------------------------------------------|
| warningType | **System.Int32** Nicht unterstützt.<br/>  |
| Parameter       | **System.Int32** Nicht unterstützt.<br/>  |
| description | **System.String** Nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist für die zukünftige Verwendung reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





