---
title: Media. markercount
description: Die markercount-Eigenschaft ruft die Anzahl der Marker im Medien Element ab.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media. markercount-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354227"
---
# <a name="mediamarkercount"></a>Media. markercount

Die **markercount** -Eigenschaft ruft die Anzahl der Marker im Medien Element ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **markercount**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**), die die Anzahl der Marker in der Datei angibt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt 0 (null) zurück, wenn eine Datei keine Marker enthält, oder wenn das Medien Element nicht mit dem *Player* übereinstimmt. **currentMedia**.

Markernummern beginnen bei 1.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **markercount** , um die Anzahl der Marker im aktuellen Medien Element abzurufen. Dieser Wert wird dann als obere Grenze für eine Schleifen Struktur verwendet, die die markerliste durchläuft, um die einzelnen Markernamen abzurufen. Ein HTML-TEXTAREA-Element mit dem Namen mNames zeigt die Namen der Marker im aktuellen Medien Element an. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
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

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





