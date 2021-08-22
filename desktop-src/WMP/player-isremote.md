---
title: Player.isRemote
description: Die isRemote-Eigenschaft ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement im Remotemodus ausgeführt wird.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Player.isRemote Windows Media Player
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afa0caf615563f4829f1a337f31521b1fb7dafd5ef6e2722f1d50c01dda1ba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616690"
---
# <a name="playerisremote"></a>Player.isRemote

Die **isRemote-Eigenschaft** ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement im Remotemodus ausgeführt wird.

## <a name="syntax"></a>Syntax

*Player* . **isRemote**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein schreibgeschützter **boolescher Wert.**



| Wert | BESCHREIBUNG                                   |
|-------|-----------------------------------------------|
| true  | Das Player-Steuerelement wird im Remotemodus ausgeführt. |
| false | Das Player-Steuerelement wird im lokalen Modus ausgeführt.  |



 

## <a name="remarks"></a>Hinweise

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer false zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





