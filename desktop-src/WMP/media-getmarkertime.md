---
title: Media.getMarkerTime-Methode
description: Die getMarkerTime-Methode ruft die Zeit des Markers am angegebenen Index ab.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- getMarkerTime-Windows Media Player
- getMarkerTime-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , getMarkerTime-Methode
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f90d1382302e4a053a6dee4dac911d2cc0c0aa67066469c8143f6f38b3bd889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508410"
---
# <a name="mediagetmarkertime-method"></a>Media.getMarkerTime-Methode

Die **getMarkerTime-Methode** ruft die Zeit des Markers am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*markerNum* \[ In\]
</dt> <dd>

**Number** (**long**) gibt den Markerindex an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** **(double)** zurück, die die Position des Markers in Sekunden ab dem Anfang des Clips angibt.

## <a name="remarks"></a>Hinweise

Diese Methode gibt **NULL zurück,** wenn der angegebene Marker nicht vorhanden ist.

Einige digitale Medienelemente enthalten keine Marker. Verwenden **Sie markerCount,** um herauszufinden, wie viele Marker sich im aktuellen Clip befinden.

Markerindexnummern beginnen bei 1.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **getMarkerTime,** um ein HTML-TEXTAREA-Element namens MTIMES mit der Position der einzelnen Marker zu füllen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media.getMarkerName**](media-getmarkername.md)
</dt> <dt>

[**Media.markerCount**](media-markercount.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





