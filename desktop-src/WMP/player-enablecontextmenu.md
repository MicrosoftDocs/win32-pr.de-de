---
title: Player. enablecontextmenu
description: Mit der enablecontextmenu-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Player. enablecontextmenu-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371995"
---
# <a name="playerenablecontextmenu"></a>Player. enablecontextmenu

Mit der **enablecontextmenu** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird.

## <a name="syntax"></a>Syntax

*Player*. **enablecontextmenu**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein boolescher Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                       |
|-------|-----------------------------------|
| true  | Standard. Aktivieren Sie das Kontextmenü. |
| false | Aktivieren Sie nicht das Kontextmenü.   |



 

## <a name="remarks"></a>Bemerkungen

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





