---
title: Media.sourceURL
description: Die sourceURL-Eigenschaft ruft die URL des Medienelements ab.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media.sourceURL-Windows Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2f99aeb64a73bcf36e2cbd472aedfa8f509a5073e70792e7b47343a1b37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415950"
---
# <a name="mediasourceurl"></a>Media.sourceURL

Die **sourceURL-Eigenschaft** ruft die URL des Medienelements ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*.sourceURL

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge.**

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **sourceURL** zum Abrufen der URL des ersten Medienelements in der Beispielwiedergabeliste; Die URL des Medienelements wird dann der Url-Eigenschaft des **Playerobjekts** zugewiesen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> </dl>

 

 





