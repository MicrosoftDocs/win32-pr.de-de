---
title: IWMPSettings autoStart-Eigenschaft
description: Die autoStart-Eigenschaft ruft einen Wert ab, der angibt, ob das aktuelle Medienelement automatisch abspielt, oder legt diesen fest.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- autoStart-Windows Media Player
- autoStart-Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , autoStart-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7be64a030bbfe8abbd81830a7638094cd3da93939f3184ad3a4cfca0063c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568467"
---
# <a name="iwmpsettingsautostart-property"></a>IWMPSettings::autoStart-Eigenschaft

Die **autoStart-Eigenschaft** ruft einen Wert ab, der angibt, ob das aktuelle Medienelement automatisch abspielt, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Boolean-Wert,** der angibt, ob die Wiedergabe des aktuellen Medienelements automatisch beginnt. Der Standardwert ist **true**.

## <a name="remarks"></a>Hinweise

Wenn **autoStart** auf **TRUE** festgelegt ist, beginnt die Wiedergabe des Medienelements, wenn **AxWindowsMediaPlayer.URL,** **AxWindowsMediaPlayer.currentPlaylist** oder **AxWindowsMediaPlayer.currentMedia** festgelegt ist. Andernfalls beginnt die Wiedergabe des Medienelements erst, wenn **die IWMPControls.play-Methode** aufgerufen wird.

Wenn Sie **autoStart nicht unmittelbar** vor der Angabe eines Medienelements auf **TRUE** festlegen, sollten Sie sich nicht auf diese Einstellung als Ersatz für die Verwendung der **IWMPControls.play-Methode** verlassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB und C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.currentPlaylist (VB und C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB und C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





