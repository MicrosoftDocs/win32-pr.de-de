---
title: IWMPSettings invokeURLs-Eigenschaft
description: Die invokeURLs-Eigenschaft ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt diesen fest.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- invokeURLs-Eigenschaft Windows Media Player
- invokeURLs-Eigenschaft Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , invokeURLs-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba44af7e6ec700f9df810486acb57af24a14c9e5d4966fddbfe4b242d346a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053428"
---
# <a name="iwmpsettingsinvokeurls-property"></a>IWMPSettings::invokeURLs-Eigenschaft

Die **invokeURLs-Eigenschaft** ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Boolean-Wert, der** angibt, ob URL-Ereignisse einen Webbrowser starten sollen. Der Standardwert ist **true**.

## <a name="remarks"></a>Hinweise

Digitale Mediendateien und Streams können URL-Skriptbefehle enthalten. Wenn ein URL-Skriptbefehl an das Windows Media Player-Steuerelement gesendet wird, wird er unabhängig vom von **invokeURLs** abgerufenen Wert zuerst an den **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent-Ereignishandler** übergeben. Nachdem **\_ WMPOCXEvents \_ ScriptCommandEvent** beendet wurde, überprüft Windows Media Player **invokeURLs,** um zu bestimmen, ob der Standardwebbrowser mit der URL gestartet werden soll. Sie können URLs selektiv anzeigen, indem Sie sie in **\_ WMPOCXEvents \_ ScriptCommandEvent** überprüfen und **invokeURLs** wie gewünscht festlegen.

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

 

 





