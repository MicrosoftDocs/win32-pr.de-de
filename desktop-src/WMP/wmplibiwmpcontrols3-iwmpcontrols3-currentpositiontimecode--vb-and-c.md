---
title: IWMPControls3 currentPositionTimecode-Eigenschaft
description: Die currentPositionTimecode-Eigenschaft ruft die aktuelle Position im aktuellen Medienelement mithilfe eines Zeitcodeformats ab oder legt sie fest. Diese Eigenschaft unterstützt derzeit SMPTE-Zeitcode.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- currentPositionTimecode-Windows Media Player
- currentPositionTimecode-Eigenschaft Windows Media Player , IWMPControls3-Schnittstelle
- IWMPControls3-Schnittstelle Windows Media Player , currentPositionTimecode-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c00c166050f4f3a3bc05861fa92d4fb66efcfa139e726c7cc799e21623fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760920"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>IWMPControls3::currentPositionTimecode-Eigenschaft

Die **currentPositionTimecode-Eigenschaft** ruft die aktuelle Position im aktuellen Medienelement mithilfe eines Zeitcodeformats ab oder legt sie fest. Diese Eigenschaft unterstützt derzeit SMPTE-Zeitcode.

## <a name="syntax"></a>Syntax


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,** bei der es sich um den SMPTE-Zeitcode handelt.

## <a name="remarks"></a>Hinweise

Der SMPTE-Zeitcode stellt eine Standard-Möglichkeit zum Identifizieren eines einzelnen Videoframes zur Synchronisierung der Wiedergabe zur Möglichkeit zur Synchronisierung von Videoaufnahmen. Wenn eine digitale Mediendatei SMPTE-Zeitcode unterstützt, kann Windows Media Player die aktuellen Zeitcodepositionsinformationen abrufen oder nach einem Videoframe suchen, der durch einen bestimmten Zeitcode identifiziert wird.

Der SMPTE-Zeitcode identifiziert einen bestimmten Frame durch die Anzahl von Stunden, Minuten, Sekunden und Frames, die ihn von einem bestimmten Referenzrahmen trennen, der als Zeit 0 festgelegt ist. Normalerweise ist der Zeitrahmen 0 (null) der Anfang der Datei, und ein bestimmter SMPTE-Zeitcodewert stellt die seit dem Start der Datei verstrichene Zeit dar.

Der Zeitcode liegt im Format \[  \] *hh*:*mm*:*ss*.*ff,* \[ *wobei range* \] den Bereich darstellt, hh stunden, *mm* minuten, *ss* sekunden und *ff Frames* darstellt. Wenn Sie einen Wert für **currentPositionTimecode festlegen,** müssen Sie alle acht Ziffern mit Nullen als Platzhaltern verwenden.

\[*Bereich* \] entspricht dem **wRange-Member** der Windows Media Format **WMT \_ TIMECODE \_ EXTENSION \_ DATA-Struktur.** Weitere Informationen zu Zeitcodebereichen finden Sie im Windows Media Format SDK.

Das Festlegen und Abrufen **von currentPositionTimecode** wird nur für Dateien unterstützt, die SMPTE-Zeitcodeinformationen enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **currentPositionTimecode** als 1 Stunde, null Minuten, 30 Sekunden und 5 Frames angegeben. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls3-Schnittstelle (VB und C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





