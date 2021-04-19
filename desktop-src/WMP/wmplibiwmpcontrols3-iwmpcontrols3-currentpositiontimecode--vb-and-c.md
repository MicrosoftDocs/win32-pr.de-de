---
title: IWMPControls3 currentPositionTimecode (Eigenschaft)
description: Die currentPositionTimecode-Eigenschaft ruft die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats ab oder legt diese fest. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- currentPositionTimecode-Eigenschaften Fenster Media Player
- currentPositionTimecode-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface Windows Media Player, currentPositionTimecode-Eigenschaft
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
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365778"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>IWMPControls3:: currentPositionTimecode-Eigenschaft

Die **currentPositionTimecode** -Eigenschaft ruft die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats ab oder legt diese fest. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.

## <a name="syntax"></a>Syntax


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System. String** , bei der es sich um den SMPTE-Zeit Code handelt.

## <a name="remarks"></a>Bemerkungen

Der SMPTE-Zeit Code stellt eine Standardmethode zum Identifizieren eines einzelnen Video Rahmens dar, der für die Synchronisierung der Wiedergabe nützlich ist. Wenn eine digitale Mediendatei SMPTE-Zeit Code unterstützt, können Windows Media Player die aktuellen Zeit Code Positionsinformationen abrufen oder einen Video Frame suchen, der durch einen bestimmten Zeit Code gekennzeichnet ist.

Der SMPTE-Zeit Code identifiziert einen bestimmten Frame um die Anzahl von Stunden, Minuten, Sekunden und Frames, die ihn von einem bestimmten Verweis Rahmen aus dem Frame trennen, der als Zeit NULL festgelegt ist. Normalerweise ist der Zeit Null-Frame der Anfang der Datei, und ein bestimmter SMPTE-Zeit Codewert stellt die verstrichene Zeit seit dem Start der Datei dar.

Der Zeit Code liegt im Format \[ *Bereich* \] *HH*:*mm*:*SS*.*FF* , wobei \[ *Range* \] den Bereich darstellt, hh stellt Stunden, *mm* stellt Minuten dar, *SS* stellt Sekunden dar, und *FF* stellt Frames dar. Wenn Sie einen Wert für **currentPositionTimecode** festlegen, müssen Sie alle acht Ziffern einschließen, wobei Sie Nullen als Platzhalter verwenden.

\[*Bereich* \] entspricht dem **Wrange** -Member der **WMT- \_ \_ Erweiterungs \_ Daten** Struktur "Windows Media-Format". Weitere Informationen zu Zeit Codebereichen finden Sie im Windows Media-Format-SDK.

Das Festlegen und das erhalten von **currentPositionTimecode** wird nur für Dateien unterstützt, die SMPTE-Zeit Code Informationen enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **currentPositionTimecode** als 1 Stunde, 0 Minuten, 30 Sekunden und 5 Frames angegeben. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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

[**IWMPControls3-Schnittstelle (VB und c#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





