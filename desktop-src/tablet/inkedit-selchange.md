---
description: Tritt ein, wenn sich die aktuelle Textauswahl im InkEdit-Steuerelement geändert hat oder die Einfügemarke verschoben wurde.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: InkEdit.SelChange-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9677aafa254de3d834e9b947ad1b858b893d6a42e53336dd11ad5c54157c13dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712650"
---
# <a name="inkeditselchange-event"></a>InkEdit.SelChange-Ereignis

Tritt ein, wenn sich die aktuelle Textauswahl im [InkEdit-Steuerelement](inkedit-control-reference.md) geändert hat oder die Einfügemarke verschoben wurde.

## <a name="syntax"></a>Syntax


```C++
void SelChange();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sie können das **SelChange-Ereignis** verwenden, um die verschiedenen Eigenschaften zu überprüfen, die Informationen zur aktuellen Auswahl (z. B. [**SelBold)**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)enthalten, sodass Sie z. B. Schaltflächen in einer Symbolleiste aktualisieren können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> </dl>

 

 




