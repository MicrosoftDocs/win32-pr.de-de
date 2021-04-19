---
description: Tritt auf, wenn sich die aktuelle Auswahl von Text im InkEdit-Steuerelement geändert hat oder die Einfügemarke verschoben wurde.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: InkEdit. selChange-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349315"
---
# <a name="inkeditselchange-event"></a>InkEdit. selChange-Ereignis

Tritt auf, wenn sich die aktuelle Auswahl von Text im [InkEdit](inkedit-control-reference.md) -Steuerelement geändert hat oder die Einfügemarke verschoben wurde.

## <a name="syntax"></a>Syntax


```C++
void SelChange();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sie können das **selChange** -Ereignis verwenden, um die verschiedenen Eigenschaften zu überprüfen, die Informationen über die aktuelle Auswahl (z. [**b. SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) geben, damit Sie z. b. Schaltflächen in einer Symbolleiste aktualisieren können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




