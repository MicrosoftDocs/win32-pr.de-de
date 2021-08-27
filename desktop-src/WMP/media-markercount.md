---
title: Media.markerCount
description: Die markerCount-Eigenschaft ruft die Anzahl der Marker im Medienelement ab.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media.markerCount Windows Media Player
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
ms.openlocfilehash: 00206991f81c6a445648a063a37bcc45bf91f647b60317772478142eefd1b20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123350"
---
# <a name="mediamarkercount"></a>Media.markerCount

Die **markerCount-Eigenschaft** ruft die Anzahl der Marker im Medienelement ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **markerCount**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**), die die Anzahl der Marker in der Datei angibt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt 0 (null) zurück, wenn eine Datei über keine Marker verfügt oder wenn das Medienelement nicht mit *player* identisch ist. **currentMedia**.

Markernummern beginnen bei 1.

Um den Wert dieser Eigenschaft abzurufen, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Media verwendet.* **markerCount,** um die Anzahl der Marker im aktuellen Medienelement abzurufen. Dieser Wert wird dann als obere Grenze für eine Schleifenstruktur verwendet, die die Markerliste durchläuft, um jeden Markernamen abzurufen. Ein HTML TEXTAREA-Element mit dem Namen MNAMES zeigt die Namen der Marker im aktuellen Medienelement an. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





