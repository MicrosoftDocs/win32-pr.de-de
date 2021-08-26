---
title: EM_SETPARAFORMAT (Richedit.h)
description: Legt die Absatzformatierung für die aktuelle Auswahl in einem Rich-Edit-Steuerelement fest.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db0ba4e4bf505c5fb1b746b84cae71dcc621635a0a33b4a533ce8551486fe6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062910"
---
# <a name="em_setparaformat-message"></a>EM \_ SETPARAFORMAT-Nachricht

Legt die Absatzformatierung für die aktuelle Auswahl in einem Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PARAFORMAT-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-paraformat) in der die neuen Absatzformatierungsattribute angegeben werden. Nur die vom **dwMask-Member angegebenen** Attribute werden geändert.

Microsoft Rich Edit 2.0 und höher: Dieser Parameter kann ein Zeiger auf eine [**PARAFORMAT2-Struktur**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) sein, die eine Erweiterung der [**PARAFORMAT-Struktur**](/windows/desktop/api/Richedit/ns-richedit-paraformat) ist. Legen Sie vor dem **Senden der EM \_ SETPARAFORMAT-Nachricht** das **cbSize-Member** der -Struktur fest, um die Version der -Struktur anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





