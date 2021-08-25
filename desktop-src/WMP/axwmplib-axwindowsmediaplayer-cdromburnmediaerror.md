---
title: CholeMediaMediaError-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das C csvMediaError-Ereignis tritt auf, wenn ein Fehler auftritt, während ein einzelnes Medienelement auf eine CD geschaltet wird.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- CholeMediaMediaError-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba161945edcda7409b842987ab97768c30a6e1f0ba011772cf7f3757d3f61c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765269"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>CholeMediaMediaError-Ereignis des AxWindowsMediaPlayer-Objekts

Das C csvMediaError-Ereignis tritt auf, wenn ein Fehler auftritt, während ein einzelnes Medienelement auf eine CD geschaltet wird.

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ C csvMediaErrorEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ C csvMediaErrorEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft   | Beschreibung                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pC über die 1000-Prozent-1 | WMPLib.IWMPCiba Über die Schnittstelle, die den Vorgang darstellt, der den Fehler ausgelöst hat.<br/>               |
| pMedia     | System.ObjectDas Medienelement, das den Fehler ausgelöst hat. Sie können diese in eine IWMPMedia-Schnittstelle umleiten, um darauf zuzugreifen.<br/> |



 

## <a name="remarks"></a>Hinweise

Behandeln Sie AxWMPLib, um generische Fehler zu erfassen. \_ WMPOCXEvents-C \_ csvError-Ereignis.

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

[**AxWindowsMediaPlayer.C csvError-Ereignis (VB und C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**IWMPCorpora Überl-Schnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





