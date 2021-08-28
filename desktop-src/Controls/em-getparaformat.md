---
title: EM_GETPARAFORMAT (Richedit.h)
description: Ruft die Absatzformatierung der aktuellen Auswahl in einem Rich-Edit-Steuerelement ab.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda99d1fefc0e2a13cc989726c86588103b7f94d7042b98393709cf4a2cd5f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048850"
---
# <a name="em_getparaformat-message"></a>EM \_ GETPARAFORMAT-Nachricht

Ruft die Absatzformatierung der aktuellen Auswahl in einem Rich-Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PARAFORMAT-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-paraformat) die die Absatzformatierungsattribute der aktuellen Auswahl empfängt.

Wenn mehr als ein Absatz ausgewählt ist, empfängt die Struktur die Attribute des ersten Absatzes, und das **dwMask-Element** gibt an, welche Attribute während der gesamten Auswahl konsistent sind.

Microsoft Rich Edit 2.0 und höher: Dieser Parameter kann ein Zeiger auf eine [**PARAFORMAT2-Struktur**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) sein, die eine Erweiterung der [**PARAFORMAT-Struktur**](/windows/desktop/api/Richedit/ns-richedit-paraformat) ist. Legen Sie vor dem **Senden der \_ EM GETPARAFORMAT-Nachricht** das **cbSize-Member** der -Struktur fest, um die Version der -Struktur anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den Wert des **dwMask-Members** der [**PARAFORMAT-Struktur**](/windows/desktop/api/Richedit/ns-richedit-paraformat) zurück.

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

 

 





