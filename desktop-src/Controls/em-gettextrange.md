---
title: EM_GETTEXTRANGE Meldung (RichEdit. h)
description: Ruft einen angegebenen Zeichenbereich von einem Rich-Edit-Steuerelement ab.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- Windows-Steuerelemente für EM_GETTEXTRANGE Meldung
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
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956901"
---
# <a name="em_gettextrange-message"></a>EM \_ GetTextRange-Nachricht

Ruft einen angegebenen Zeichenbereich von einem Rich-Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**TextRange**](/windows/win32/api/richedit/ns-richedit-textrangea) -Struktur, die den Bereich der abzurufenden Zeichen und einen Puffer angibt, in den die Zeichen kopiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt die Anzahl der kopierten Zeichen zurück, ohne das abschließende Null Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





