---
title: Media. getmarkertime-Methode
description: Die getmarkertime-Methode ruft die Zeit des Markers am angegebenen Index ab.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- getmarkertime-Methode, Windows-Media Player
- getmarkertime-Methode, Windows Media Player, Medienklasse
- Medienklasse Windows Media Player, getmarkertime-Methode
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
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358726"
---
# <a name="mediagetmarkertime-method"></a>Media. getmarkertime-Methode

Die **getmarkertime** -Methode ruft die Zeit des Markers am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*markernum* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den MarkerIndex angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Double**) zurück, die den Speicherort der Markierung in Sekunden ab dem Anfang des Clips angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt **null** zurück, wenn der angegebene Marker nicht vorhanden ist.

Einige digitale Medienelemente enthalten keine Marker. Verwenden Sie **markercount** , um herauszufinden, wie viele Marker im aktuellen Clip angezeigt werden.

Markerindexnummern beginnen bei 1.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **getmarkertime** zum Ausfüllen eines HTML-TEXTAREA-Elements mit dem Namen "mtimes" mit dem Speicherort der einzelnen Marker. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. getmarkername**](media-getmarkername.md)
</dt> <dt>

[**Media. markercount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





