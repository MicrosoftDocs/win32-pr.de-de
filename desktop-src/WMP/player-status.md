---
title: Player.status
description: Die status-Eigenschaft ruft einen Wert ab, der den Status von Windows Media Player angibt.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player.status Windows Media Player
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
ms.openlocfilehash: a03ef010bfcb5ee936183724331e97fac5d6f5912d87c5281a55106519c104e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572049"
---
# <a name="playerstatus"></a>Player.status

Die **status-Eigenschaft** ruft einen Wert ab, der den Status von Windows Media Player angibt.

## <a name="syntax"></a>Syntax

*Player* . **status**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte Zeichenfolge.

## <a name="remarks"></a>Hinweise

Die in dieser Eigenschaft enthaltenen Werte können jederzeit geändert werden und sollten nur für Anzeigezwecke verwendet werden.

Das **StatusChange-Ereignis** wird immer dann ausgelöst, wenn sich der Wert dieser Eigenschaft ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 7.0 oder höher.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.StatusChange-Ereignis**](player-player-statuschange.md)
</dt> </dl>

 

 





