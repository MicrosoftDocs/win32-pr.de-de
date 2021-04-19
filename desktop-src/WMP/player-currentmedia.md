---
title: Player. currentMedia
description: Die currentMedia-Eigenschaft gibt das aktuelle Medienobjekt an oder ruft es ab.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player. currentMedia-Fenster Media Player
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
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366696"
---
# <a name="playercurrentmedia"></a>Player. currentMedia

Die **currentMedia** -Eigenschaft gibt das aktuelle Medienobjekt an oder ruft es ab.

## <a name="syntax"></a>Syntax

*Player* . **currentMedia**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Medienobjekt mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Bemerkungen

Wenn die *Einstellungen*. die **Autostart** -Eigenschaft ist "true". die Wiedergabe beginnt automatisch, wenn Sie **currentMedia** festlegen.

Diese Eigenschaft nimmt ein Medienobjekt an, das über die *Wiedergabeliste* abgerufen werden kann. **Element**. Wenn Sie ein **Medien** Element mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest, oder verwenden Sie **newmedia**.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird das erste Medien Element in der Bibliothek abgerufen. Anschließend wird **currentMedia** verwendet, um das abgerufene Medien Element zum aktuellen Medien Element zu machen, und dann den Namen des aktuellen Medien Elements anzuzeigen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. newmedia**](player-newmedia.md)
</dt> <dt>

[**Wiedergabeliste. Element**](playlist-item.md)
</dt> <dt>

[**Einstellungen. Autostart**](settings-autostart.md)
</dt> </dl>

 

 





