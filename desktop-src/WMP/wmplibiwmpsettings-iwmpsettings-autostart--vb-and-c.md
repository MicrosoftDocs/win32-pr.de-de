---
title: Iwmpsettings Autostart (Eigenschaft)
description: Mit der Autostart-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- Autostart-Eigenschaften Fenster Media Player
- AutoStart-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, AutoStart-Eigenschaft
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
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360930"
---
# <a name="iwmpsettingsautostart-property"></a>Iwmpsettings:: AutoStart-Eigenschaft

Mit der **Autostart** -Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Boolean** -Wert, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird. Der Standardwert ist **true**.

## <a name="remarks"></a>Bemerkungen

Wenn **Autostart** auf **true** festgelegt ist, wird das Medien Element abgespielt, wenn **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentwiedergabe** oder **AxWindowsMediaPlayer. currentMedia** festgelegt ist. Andernfalls wird das Medien Element erst wieder abgespielt, wenn die **iwmpcontrols. Play** -Methode aufgerufen wird.

Wenn Sie " **Autostart** " nicht unmittelbar vor der Angabe eines Medien Elements auf " **true** " festlegen, sollten Sie diese Einstellung nicht als Ersatz für die Verwendung der **iwmpcontrols. Play** -Methode verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB und c#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. currentwiedergabe (VB und c#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB und c#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Play (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





