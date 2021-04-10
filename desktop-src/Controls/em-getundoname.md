---
title: EM_GETUNDONAME Meldung (RichEdit. h)
description: Microsoft Rich Edit 2,0 und höher ruft ggf. den Typ der nächsten Rückgängig-Aktion ab. Microsoft Rich Edit 1,0 diese Meldung wird nicht unterstützt.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Windows-Steuerelemente für EM_GETUNDONAME Meldung
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
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956900"
---
# <a name="em_getundoname-message"></a>EM \_ getundoname-Meldung

Microsoft Rich Edit 2,0 und höher: Ruft den Typ der nächsten Rückgängig-Aktion ab, sofern vorhanden.

Microsoft Rich Edit 1,0: Diese Meldung wird nicht unterstützt.

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

Wenn eine Rückgängig-Aktion vorliegt, ist der zurückgegebene Wert ein [**undonameid**](/windows/desktop/api/Richedit/ne-richedit-undonameid) -Enumerationswert, der den Typ der nächsten Aktion in der Rückgängig-Warteschlange des Steuer Elements angibt.

Wenn keine Aktionen vorhanden sind, die rückgängig gemacht werden können, oder der Typ der nächsten Rückgängig-Aktion unbekannt ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Die Typen von Aktionen, die rückgängig gemacht oder wiederholt werden können, sind das eingeben, löschen, ziehen, ablegen, Ausschneiden und einfügen. Diese Informationen können für Anwendungen nützlich sein, die eine erweiterte Benutzeroberfläche für Rückgängigvorgänge und Wiederholungs Vorgänge bereitstellen, z. b. ein Dropdown-Listenfeld mit Aktionen, die rückgängig gemacht werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ getredoname**](em-getredoname.md)
</dt> <dt>

[**EM- \_ Wiederholung**](em-redo.md)
</dt> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> <dt>

[**Undonameid**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





