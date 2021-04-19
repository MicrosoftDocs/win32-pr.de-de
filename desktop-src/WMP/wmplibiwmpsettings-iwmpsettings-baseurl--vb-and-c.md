---
title: Iwmpsettings baseurl (Eigenschaft)
description: Die baseurl-Eigenschaft ruft die Basis-URL ab oder legt Sie fest, die für die relative Pfad Auflösung mit URL-Skript Befehlen verwendet wird, die in Inhalte digitaler Medien eingebettet sind
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- baseurl-Eigenschaften Fenster Media Player
- baseurl-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, baseurl-Eigenschaft
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
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369531"
---
# <a name="iwmpsettingsbaseurl-property"></a>Iwmpsettings:: baseurl (Eigenschaft)

Die **baseurl** -Eigenschaft ruft die Basis-URL ab oder legt Sie fest, die für die relative Pfad Auflösung mit URL-Skript Befehlen verwendet wird, die in Inhalte digitaler Medien eingebettet sind

## <a name="syntax"></a>Syntax


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. String** -Wert, der die Basis-URL ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Basis-http-URL an, die vom **AxWindowsMediaPlayer \_ wmpocxevents \_ scriptcommandevent** -Ereignis als Befehlsparameter übergeben wird. Die Basis-URL wird wie folgt mit der relative URL verkettet:

1.  Dem Wert, der von der **baseurl** -Eigenschaft abgerufen wird, wird ein nach stehender Schrägstrich (/) hinzugefügt.
2.  Ein führender Zeitraum, ein umgekehrter Schrägstrich oder ein Schrägstrich (., \\ , und/) wird aus der relative URL gelöscht.
3.  Der relative URL wird am Ende der Basis-URL hinzugefügt.
4.  Alle Schrägstriche in der resultierenden voll qualifizierten URL werden in der gleichen Richtung (konvertiert in vorwärts-oder rückwärts Schrägstriche) basierend auf der Richtung des ersten Schrägstrichs in der neuen URL gezeigt.

**Hinweis**

Das Windows Media Player-Steuerelement unterstützt nicht die Verwendung von zwei Punkten (..) in der relative URL, um das übergeordnete Element des aktuellen Speicher Orts anzugeben.

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

 

 





