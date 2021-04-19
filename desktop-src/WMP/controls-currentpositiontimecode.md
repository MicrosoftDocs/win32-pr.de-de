---
title: Controls. currentPositionTimecode
description: Die currentPositionTimecode-Eigenschaft gibt die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats an oder ruft diese ab. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Steuerelemente. currentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356332"
---
# <a name="controlscurrentpositiontimecode"></a>Controls. currentPositionTimecode

Die **currentPositionTimecode** -Eigenschaft gibt die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats an oder ruft diese ab. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Der SMPTE-Zeit Code stellt eine Standardmethode zum Identifizieren eines einzelnen Video Rahmens dar, der für die Synchronisierung der Wiedergabe nützlich ist. Wenn eine digitale Mediendatei SMPTE-Zeit Code unterstützt, können Windows-Media Player die aktuellen Zeit Code Positionsinformationen abrufen oder einen Video Frame suchen, der durch eine bestimmte Zeit Code **Zeichenfolge** identifiziert wird.

Der SMPTE-Zeit Code identifiziert einen bestimmten Frame um die Anzahl von Stunden, Minuten, Sekunden und Frames, die ihn von einem bestimmten Verweis Rahmen aus dem Frame trennen, der als Zeit NULL festgelegt ist. Normalerweise ist der Zeit Null-Frame der Anfang der Datei, und ein bestimmter SMPTE-Zeit Codewert stellt die verstrichene Zeit seit dem Start der Datei dar.

Die Zeit Code **Zeichenfolge** liegt im Format \[ *Bereich* \] *HH*:*mm*:*SS*.*FF* , wobei \[ *Range* \] den Bereich darstellt, *HH* stellt Stunden, *mm* stellt Minuten dar, *SS* stellt Sekunden dar, und *FF* stellt Frames dar. Wenn Sie mithilfe von **currentPositionTimecode** einen Wert angeben, müssen Sie alle acht Ziffern mit Nullen als Platzhalter einschließen.

Der \[  \] Bereichsspezifizierer entspricht dem **Wrange** -Member der **WMT- \_ \_ Erweiterungs \_ Daten** Struktur von Windows Media-Format. Weitere Informationen zu Zeit Codebereichen finden Sie im Windows Media-Format-SDK.

Das angeben und Abrufen von **currentPositionTimecode** wird nur für Dateien unterstützt, die SMPTE-Zeit Code Informationen enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **currentPositionTimecode** als 1 Stunde, 0 Minuten, 30 Sekunden und 5 Frames angegeben. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 





