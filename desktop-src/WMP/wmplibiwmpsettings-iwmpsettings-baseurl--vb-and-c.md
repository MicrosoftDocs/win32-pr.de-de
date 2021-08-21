---
title: IWMPSettings baseURL-Eigenschaft
description: Die baseURL-Eigenschaft ruft die Basis-URL ab, die für die relative Pfadauflösung mit URL-Skriptbefehlen verwendet wird, die in digitale Medieninhalte eingebettet sind, oder legt diese fest.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- baseURL-Windows Media Player
- baseURL-Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , baseURL-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3224a43a2689fd49dee2b2a66cc768250b1a829e61863d8cfbd029e3cdf783c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568418"
---
# <a name="iwmpsettingsbaseurl-property"></a>IWMPSettings::baseURL-Eigenschaft

Die **baseURL-Eigenschaft** ruft die Basis-URL ab, die für die relative Pfadauflösung mit URL-Skriptbefehlen verwendet wird, die in digitale Medieninhalte eingebettet sind, oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,die** die Basis-URL ist.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die HTTP-Basis-URL an, die vom **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent-Ereignis als Befehlsparameter übergeben** wird. Die Basis-URL wird wie folgt mit relative URL verkettet:

1.  Dem wert, der von der **baseURL-Eigenschaft** abgerufen wird, wird ein nachgeschlagener Schrägstrich (/) hinzugefügt.
2.  Ein führender Zeitraum, rückwärts gerichteter Schrägstrich oder Schrägstrich (., und /) wird aus der \\ relative URL.
3.  Die relative URL wird am Ende der Basis-URL hinzugefügt.
4.  Alle Schrägstriche in der resultierenden vollqualifizierten URL werden in derselben Richtung angezeigt (konvertiert in Schrägstriche oder rückwärts), basierend auf der Richtung des ersten Schrägstrichs in der neuen URL.

**Hinweis**

Das Windows Media Player-Steuerelement unterstützt nicht die Verwendung von zwei Zeiträumen (..) in der relative URL, um das übergeordnete Element des aktuellen Speicherorts anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer.ScriptCommand-Ereignis (VB und C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





