---
title: Media. getmarkername-Methode
description: Die getmarkername-Methode ruft den Namen des Markers am angegebenen Index ab.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- getmarkername-Methode, Windows Media Player
- getmarkername-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getmarkername-Methode
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361695"
---
# <a name="mediagetmarkername-method"></a>Media. getmarkername-Methode

Die **getmarkername** -Methode ruft den Namen des Markers am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*markernum* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die einen MarkerIndex angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt **null** zurück, wenn der angegebene Marker nicht vorhanden ist.

Einige digitale Medienelemente enthalten keine Marker. Verwenden Sie **markercount** , um herauszufinden, wie viele Marker im aktuellen Clip angezeigt werden.

Markerindexnummern beginnen bei 1.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. " **getmarkername** ", um ein HTML-TEXTAREA-Element mit dem Namen "mNames" mit den Namen der Marker im aktuellen Medien Element auszufüllen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
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

[**Media. getmarkertime**](media-getmarkertime.md)
</dt> <dt>

[**Media. markercount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





