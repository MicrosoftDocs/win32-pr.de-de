---
title: DEFAULTFrame-Eigenschaft von IWMPSettings
description: Die defaultFrame-Eigenschaft ruft den Namen des Frames ab, der zum Anzeigen einer URL verwendet wird, die in einem AxWindowsMediaPlayer \_ WMPOCXEvents ScriptCommandEvent-Ereignis empfangen wird, oder legt diesen \_ fest.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- defaultFrame-Windows Media Player
- defaultFrame-Eigenschaft Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , defaultFrame-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39352b2c49bfdcd50f3e5c74d88a9fafef6752034dbd220cda3bb34dc0ed5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053438"
---
# <a name="iwmpsettingsdefaultframe-property"></a>IWMPSettings::d efaultFrame-Eigenschaft

Die **defaultFrame-Eigenschaft** ruft den Namen des Frames ab, der zum Anzeigen einer URL verwendet wird, die in einem **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent-Ereignis** empfangen wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,die** den Wert des Namensattributs des **FRAME-Zielelements** ist.

## <a name="remarks"></a>Hinweise

Wenn ein Zielframe im **\_ WMPOCXEvents \_ ScriptCommandEvent-Ereignis** selbst angegeben wird, wird diese Eigenschaft ignoriert.

Diese Eigenschaft wird ignoriert, wenn das Java-Netscape Navigator verwendet wird. In Netscape Navigator zeigt jeder empfangene URL-Skriptbefehl die URL in einem neuen Browserfenster an, unabhängig vom Wert von **defaultFrame**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer.ScriptCommand-Ereignis (VB und C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





