---
title: Iwmpsettings defaultframe (Eigenschaft)
description: Mit der defaultframe-Eigenschaft wird der Name des Frames abgerufen oder festgelegt, der zum Anzeigen einer URL verwendet wird, die in einem AxWindowsMediaPlayer \_ wmpocxevents \_ scriptcommandevent-Ereignis empfangen wird.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- defaultframe-Eigenschaften Fenster Media Player
- defaultframe-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, defaultframe (Eigenschaft)
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
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364860"
---
# <a name="iwmpsettingsdefaultframe-property"></a>Iwmpsettings::d efaultframe-Eigenschaft

Mit der **defaultframe** -Eigenschaft wird der Name des Frames abgerufen oder festgelegt, der zum Anzeigen einer URL verwendet wird, die in einem **AxWindowsMediaPlayer \_ wmpocxevents \_ scriptcommandevent** -Ereignis empfangen wird.

## <a name="syntax"></a>Syntax


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. String** -Wert, der dem Wert des Name-Attributs des Ziel **Frame** Elements entspricht.

## <a name="remarks"></a>Bemerkungen

Wenn im **\_ wmpocxevents \_ scriptcommandevent** -Ereignis ein Zielframe angegeben ist, wird diese Eigenschaft ignoriert.

Diese Eigenschaft wird ignoriert, wenn das Applet "Netscape Navigator Java" verwendet wird. Im Netscape Navigator zeigt jeder empfangene URL-Skript Befehl die URL in einem neuen Browserfenster an, unabhängig vom Wert von **defaultframe**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer. ScriptCommand-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





