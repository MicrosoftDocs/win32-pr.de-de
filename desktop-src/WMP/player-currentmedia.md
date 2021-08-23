---
title: Player.currentMedia
description: Die currentMedia-Eigenschaft gibt das aktuelle Media-Objekt an oder ruft es ab.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player.currentMedia-Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5e8cd2032d772cbd781d0b45794e86cc19eff7c730a6a963778d54a6f283d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054398"
---
# <a name="playercurrentmedia"></a>Player.currentMedia

Die **currentMedia-Eigenschaft** gibt das aktuelle Media-Objekt an oder ruft es ab.

## <a name="syntax"></a>Syntax

*Player* . **currentMedia**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Medienobjekt mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Wenn der *Einstellungen.* **Die autoStart-Eigenschaft** ist true. Die Wiedergabe beginnt automatisch, wenn Sie **currentMedia festlegen.**

Diese Eigenschaft nimmt ein Media-Objekt an, das mithilfe der Wiedergabeliste *erworben werden kann.* **Item**. Um ein **Medienelement mithilfe** eines Dateinamens zu laden, legen Sie die URL-Eigenschaft fest, oder verwenden **Sie newMedia**.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird das erste Medienelement in der Bibliothek abgerufen. Anschließend wird **currentMedia verwendet,** um das abgerufene Medienelement zum aktuellen Medienelement zu machen und dann den Namen des aktuellen Medienelements anzuzeigen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
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

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Einstellungen.autoStart**](settings-autostart.md)
</dt> </dl>

 

 





