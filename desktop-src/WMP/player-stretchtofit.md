---
title: Player. stretchdefit
description: Mit der Eigenschaft stretchdefit wird ein Wert angegeben oder abgerufen, der angibt, ob das Video, das von der Windows-Media Player Steuerung angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds ist.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player. stretchdefit-Fenster Media Player
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
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368291"
---
# <a name="playerstretchtofit"></a>Player. stretchdefit

Mit der Eigenschaft **stretchdefit** wird ein Wert angegeben oder abgerufen, der angibt, ob das Video, das von der Windows-Media Player Steuerung angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds ist.

## <a name="syntax"></a>Syntax

*Player*. **stretchdefit**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                            |
|-------|--------------------------------------------------------|
| true  | Das Video wird so gestreckt, dass es an das Fenster angepasst wird.              |
| false | Standard. Das Video wird nicht so gestreckt, dass es an das Fenster angepasst wird. |



 

## <a name="remarks"></a>Bemerkungen

Wenn **stretchdefit** auf true festgelegt ist, wird das ursprüngliche Seitenverhältnis des Videos vom Windows Media Player-Steuerelement beibehalten. Wenn das Seitenverhältnis des Videos nicht mit dem Seitenverhältnis des Videofensters identisch ist, können schwarze Masken Bereiche entweder am oberen und unteren Rand des Video Bilds angezeigt werden.

Diese Eigenschaft gilt nur für das Windows Media Player-Steuerelement, wenn Sie in eine Webseite eingebettet ist.

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,1 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





