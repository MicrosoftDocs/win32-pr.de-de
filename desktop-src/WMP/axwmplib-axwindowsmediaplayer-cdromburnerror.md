---
title: C cyberError-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Cerror-Ereignis tritt auf, wenn während eines CD-Vorgangs ein generischer Fehler auftritt.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- CerrorError-Ereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ea2ca4c510685e8a9d23a3fdc507e055f30c8916c7bf8bbbfbb30a5c4591b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864740"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>C cyberError-Ereignis des AxWindowsMediaPlayer-Objekts

Das Cerror-Ereignis tritt auf, wenn während eines CD-Vorgangs ein generischer Fehler auftritt.

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ CerrorErrorEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ CerrorErrorEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft   | BESCHREIBUNG                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| hrError    | **System.Int32** Der Fehler, der das Ereignis ausgelöst hat.<br/>                                               |
| pC wies | WMPLib.IWMPC wie Die Schnittstelle, die den Vorgang darstellt, der den Fehler ausgelöst hat.<br/> |



 

## <a name="remarks"></a>Hinweise

Behandeln Sie AxWMPLib, um medienspezifische Fehler zu erfassen. \_ \_WMPOCXEvents-CmediaMediaError-Ereignis.

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

[**AxWindowsMediaPlayer.CmediaMediaError-Ereignis (VB und C#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**IWMPCführungsschnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





