---
title: Stiftflags
description: Werte, die im PenFlags-Feld der -Struktur POINTER_PEN_INFO werden können.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: acc1afb1d490a1831fdb1ecd5a090e457bae77ae2f08a1b94cabc81d12dbde9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482405"
---
# <a name="pen-flags"></a>Stiftflags

Werte, die im **PenFlags-Feld** der -Struktur POINTER_PEN_INFO [**werden**](/previous-versions/windows/desktop/api) können.

<dl> <dt>

<span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Es gibt kein Stiftflag. Dies ist die Standardoption.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Die Schaltfläche "Knopf" wird gedrückt.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Der Stift ist invertiert.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Die Radiererschaltfläche wird gedrückt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Konstanten](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





