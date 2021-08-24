---
title: EM_GETUNDONAME Nachricht (Richedit.h)
description: Microsoft Rich Edit 2.0 und höher Ruft ggf. den Typ der nächsten Rückgängigaktion ab. Microsoft Rich Edit 1.0 Diese Meldung wird nicht unterstützt.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d133038c0adad2fe7eaa1ae98cf638fe6bd13fad82df3b3d2d1ac384a30e1a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576640"
---
# <a name="em_getundoname-message"></a>EM \_ GETUNDONAME-Nachricht

Microsoft Rich Edit 2.0 und höher: Ruft ggf. den Typ der nächsten Rückgängigaktion ab.

Microsoft Rich Edit 1.0: Diese Meldung wird nicht unterstützt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Rückgängigaktion vorhanden ist, ist der zurückgegebene Wert ein [**UNDONAMEID-Enumerationswert,**](/windows/desktop/api/Richedit/ne-richedit-undonameid) der den Typ der nächsten Aktion in der Rückgängig-Warteschlange des Steuerelements angibt.

Wenn keine Aktionen rückgängig werden können oder der Typ der nächsten Rückgängigaktion unbekannt ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Zu den Aktionstypen, die rückgängig machen oder wieder rückgängig machen können, gehören Eingabe-, Lösch-, Drag&drop-, Ausschneide- und Einfügevorgänge. Diese Informationen können für Anwendungen nützlich sein, die eine erweiterte Benutzeroberfläche für Rückgängig- und Wiederholungsvorgänge bereitstellen, z. B. ein Dropdownlistenfeld mit Aktionen, die rückgängig gemacht werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





