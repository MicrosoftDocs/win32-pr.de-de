---
title: Player.windowlessVideo
description: Die windowlessVideo-Eigenschaft gibt einen Wert an, der angibt, ob das Windows Media Player Video im fensterlosen Modus rendert, oder ruft einen Wert ab.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player.windowlessVideo Windows Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733f8488d1d45f4c7e9794e64e2b3a70b41722048eac82d5d8eb6eb2f1d91cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572077"
---
# <a name="playerwindowlessvideo"></a>Player.windowlessVideo

Die **windowlessVideo-Eigenschaft** gibt einen Wert an, der angibt, ob das Windows Media Player Video im fensterlosen Modus rendert, oder ruft einen Wert ab.

## <a name="syntax"></a>Syntax

*Player*. **windowlessVideo**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher Wert,** der zur Entwurfszeit angegeben wird und danach schreibgeschützt ist.



| Wert | BESCHREIBUNG                                      |
|-------|--------------------------------------------------|
| true  | Das Video wird im fensterlosen Modus gerendert.        |
| false | Standard. Das Video wird im Fenstermodus gerendert. |



 

## <a name="remarks"></a>Hinweise

Standardmäßig rendert ein eingebettetes Windows Media Player-Steuerelement Videos in einem eigenen Fenster innerhalb des Clientbereichs. Wenn **windowlessVideo** auf TRUE festgelegt ist, rendert das Player-Steuerelement Videos direkt im Clientbereich, sodass Sie Sondereffekte anwenden oder das Video mit Text über ebenen können.

In Windows Vista kann das Rendern von Videos im fensterlosen Modus die Leistung beeinträchtigen.

Die **windowlessVideo-Eigenschaft** wird für die Netscape Navigator. Das Festlegen eines Werts für diese Eigenschaft im Navigator kann zu unerwarteten Ergebnissen führen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





