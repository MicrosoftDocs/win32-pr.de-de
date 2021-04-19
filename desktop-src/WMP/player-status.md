---
title: Player. Status
description: Die Status-Eigenschaft ruft einen Wert ab, der den Status von Windows Media Player angibt.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player. Status-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370523"
---
# <a name="playerstatus"></a>Player. Status

Die **Status** -Eigenschaft ruft einen Wert ab, der den Status von Windows Media Player angibt.

## <a name="syntax"></a>Syntax

*Player* . **Status**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte Zeichenfolge.

## <a name="remarks"></a>Bemerkungen

Die in dieser Eigenschaft enthaltenen Werte können jederzeit geändert werden und sollten nur zu Anzeige Zwecken verwendet werden.

Das **statusChange** -Ereignis wird ausgelöst, wenn diese Eigenschaft den Wert ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 7,0 oder höher.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. statusChange-Ereignis**](player-player-statuschange.md)
</dt> </dl>

 

 





