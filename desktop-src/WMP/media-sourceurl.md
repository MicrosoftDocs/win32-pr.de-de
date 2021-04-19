---
title: Media. SourceUrl
description: Die SourceUrl-Eigenschaft ruft die URL des Medien Elements ab.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. SourceUrl-Windows-Media Player
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
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359666"
---
# <a name="mediasourceurl"></a>Media. SourceUrl

Die **SourceUrl** -Eigenschaft ruft die URL des Medien Elements ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. SourceUrl

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **SourceUrl** zum Abrufen der URL des ersten Medien Elements in der Beispiel Wiedergabeliste die URL des Medien Elements wird dann der Eigenschaft "Player Object **URL** " zugewiesen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> </dl>

 

 





