---
title: Player. windowlessvideo
description: Mit der windowlessvideo-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player. windowlessvideo-Fenster Media Player
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
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359324"
---
# <a name="playerwindowlessvideo"></a>Player. windowlessvideo

Mit der **windowlessvideo** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.

## <a name="syntax"></a>Syntax

*Player*. **windowlessvideo**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher** Wert, der zur Entwurfszeit angegeben wird und danach schreibgeschützt ist.



| Wert | BESCHREIBUNG                                      |
|-------|--------------------------------------------------|
| true  | Das Video wird im fensterlosen Modus gerendert.        |
| false | Standard. Das Video wird im Fenstermodus gerendert. |



 

## <a name="remarks"></a>Bemerkungen

Standardmäßig rendert ein eingebettetes Windows-Media Player-Steuerelement Videos in einem eigenen Fenster innerhalb des Client Bereichs. Wenn **windowlessvideo** auf "true" festgelegt ist, rendert das Player-Steuerelement Videos direkt im Client Bereich, sodass Sie besondere Effekte anwenden oder das Video mit Text übertragen können.

In Windows Vista kann das Rendern von Videos im fensterlosen Modus die Leistung beeinträchtigen.

Die **windowlessvideo** -Eigenschaft wird für den Netscape-Navigator nicht unterstützt. Wenn Sie einen Wert für diese Eigenschaft im Navigator festlegen, kann dies zu unerwarteten Ergebnissen führen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





