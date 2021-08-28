---
title: Controls.currentPositionTimecode
description: Die currentPositionTimecode-Eigenschaft gibt die aktuelle Position im aktuellen Medienelement mithilfe eines Zeitcodeformats an oder ruft sie ab. Diese Eigenschaft unterstützt derzeit SMPTE-Zeitcode.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls.currentPositionTimecode Windows Media Player
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
ms.openlocfilehash: 2dd0dcdf4c5337cf8dc447452ce9667c261a9c7ea4b11f98753a294bca20c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736540"
---
# <a name="controlscurrentpositiontimecode"></a>Controls.currentPositionTimecode

Die **currentPositionTimecode-Eigenschaft** gibt die aktuelle Position im aktuellen Medienelement mithilfe eines Zeitcodeformats an oder ruft sie ab. Diese Eigenschaft unterstützt derzeit SMPTE-Zeitcode.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Der SMPTE-Zeitcode stellt eine Standard-Möglichkeit zum Identifizieren eines einzelnen Videoframes zur Synchronisierung der Wiedergabe zur Möglichkeit zur Synchronisierung von Videoaufnahmen. Wenn eine digitale Mediendatei SMPTE-Zeitcode unterstützt, kann Windows Media Player die aktuellen Zeitcodepositionsinformationen abrufen oder nach einem Videoframe suchen, der durch einen bestimmten Zeitcode identifiziert **wird.**

Der SMPTE-Zeitcode identifiziert einen bestimmten Frame durch die Anzahl von Stunden, Minuten, Sekunden und Frames, die ihn von einem bestimmten Referenzrahmen trennen, der als Zeit 0 festgelegt ist. Normalerweise ist der Zeitrahmen 0 (null) der Anfang der Datei, und ein bestimmter SMPTE-Zeitcodewert stellt die seit dem Start der Datei verstrichene Zeit dar.

Der Zeitcode **String** liegt im Format \[  \] *hh*:*mm*:*ss*.*ff,* \[ *wobei range* \] den Bereich darstellt, *hh* stunden, *mm* minuten, *ss* sekunden und *ff Frames* darstellt. Wenn Sie einen Wert mit **currentPositionTimecode angeben,** müssen Sie alle acht Ziffern mit Nullen als Platzhalter angeben.

Der \[  \] Bereichsspezifizierer entspricht dem **wRange-Member** der Windows Media Format **WMT \_ TIMECODE \_ EXTENSION \_ DATA-Struktur.** Weitere Informationen zu Zeitcodebereichen finden Sie im Windows Media Format SDK.

Das Angeben und Abrufen von **currentPositionTimecode** wird nur für Dateien unterstützt, die SMPTE-Zeitcodeinformationen enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **currentPositionTimecode** als 1 Stunde, null Minuten, 30 Sekunden und 5 Frames angegeben. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 





