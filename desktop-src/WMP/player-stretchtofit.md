---
title: Player.stretchToFit
description: Die stretchToFit-Eigenschaft gibt einen Wert an, der angibt, ob das vom Windows Media Player-Steuerelement angezeigte Video automatisch an das Videofenster passt, wenn das Videofenster größer als die Abmessungen des Videobilds ist, oder ruft einen Wert ab.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player.stretchToFit Windows Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570d0b9bf7e266af769944b675a85c0ac1518c321d11038ff94cab035dfb316c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995840"
---
# <a name="playerstretchtofit"></a>Player.stretchToFit

Die **stretchToFit-Eigenschaft** gibt einen Wert an oder ruft einen Wert ab, der angibt, ob das vom Windows Media Player-Steuerelement angezeigte Video automatisch an das Videofenster passt, wenn das Videofenster größer als die Abmessungen des Videobilds ist.

## <a name="syntax"></a>Syntax

*Player*. **stretchToFit**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                                            |
|-------|--------------------------------------------------------|
| true  | Das Video wird gestreckt, damit es in das Fenster passt.              |
| false | Standard. Das Video wird nicht so gestreckt, dass es in das Fenster passt. |



 

## <a name="remarks"></a>Hinweise

Wenn **stretchToFit** auf TRUE festgelegt ist, behält das Windows Media Player-Steuerelement das ursprüngliche Seitenverhältnis des Videos bei. Wenn das Seitenverhältnis des Videos nicht mit dem Seitenverhältnis des Videofensters überein passt, können schwarze Maskenbereiche entweder oben und unten oder links und rechts des Videobilds angezeigt werden.

Diese Eigenschaft gilt für das Windows Media Player Steuerelement nur, wenn es in eine Webseite eingebettet ist.

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.1 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





