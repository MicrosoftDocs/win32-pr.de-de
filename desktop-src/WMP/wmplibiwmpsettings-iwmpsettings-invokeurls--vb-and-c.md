---
title: Iwmpsettings invokeurls (Eigenschaft)
description: Die invokeurls-Eigenschaft ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt diesen fest.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- invokeurls-Eigenschaft, Windows-Media Player
- invokeurls-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings Interface, Windows Media Player, invokeurls (Eigenschaft)
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
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371575"
---
# <a name="iwmpsettingsinvokeurls-property"></a>Iwmpsettings:: invokeurls (Eigenschaft)

Die **invokeurls** -Eigenschaft ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Boolean** -Wert, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen. Der Standardwert ist **true**.

## <a name="remarks"></a>Bemerkungen

Digitale Mediendateien und Streams können URL-Skript Befehle enthalten. Wenn ein URL-Skript Befehl an das Windows Media Player-Steuerelement gesendet wird, wird er unabhängig von dem von **invokeurls** abgerufenen Wert zuerst an den **AxWindowsMediaPlayer-Ereignishandler " \_ \_ scriptcommandevent** " übergeben. Nachdem **\_ wmpocxevents \_ scriptcommandevent** beendet wurde, überprüft Windows Media Player **invokeurls** , um zu bestimmen, ob der Standard Webbrowser mit der URL gestartet werden soll. Sie können URLs selektiv anzeigen, indem Sie Sie in **\_ wmpocxevents \_ scriptcommandevent** überprüfen und **invokeurls** wie gewünscht festlegen.

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

 

 





