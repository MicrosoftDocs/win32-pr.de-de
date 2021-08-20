---
title: EM_GETTEXTRANGE Nachricht (Richedit.h)
description: Ruft einen angegebenen Zeichenbereich aus einem Rich-Edit-Steuerelement ab.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12282b970c38164e5b28a31ed778a3320f88bbdf16b6d182586e492e5e699eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006575"
---
# <a name="em_gettextrange-message"></a>EM \_ GETTEXTRANGE-Nachricht

Ruft einen angegebenen Zeichenbereich aus einem Rich-Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TEXTRANGE-Struktur,**](/windows/win32/api/richedit/ns-richedit-textrangea) die den Bereich der abzurufenden Zeichen und einen Puffer angibt, in den die Zeichen kopiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Nachricht gibt die Anzahl der kopierten Zeichen zurück, ohne das abschließende NULL-Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Textrange**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





