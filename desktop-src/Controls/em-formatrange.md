---
title: EM_FORMATRANGE Nachricht (Richedit.h)
description: Formatiert einen Textbereich in einem Rich Edit-Steuerelement für ein bestimmtes Gerät.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941aceb8c8f91657c7f78aba3d83a627fc413ed20d71217c933c6fba9b6f39e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049350"
---
# <a name="em_formatrange-message"></a>EM \_ FORMATRANGE-Meldung

Formatiert einen Textbereich in einem Rich Edit-Steuerelement für ein bestimmtes Gerät.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der Text gerendert werden soll. Wenn dieser Parameter nicht 0 (null) ist, wird der Text gerendert. Andernfalls wird der Text nur gemessen.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**FORMATRANGE-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-formatrange) die Informationen über das Ausgabegerät enthält, oder **NULL,** um vom Steuerelement zwischengespeicherte Informationen freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den Index des letzten Zeichens zurück, das in den Bereich passt, plus 1.

## <a name="remarks"></a>Hinweise

Diese Meldung wird in der Regel verwendet, um den Inhalt des Rich-Edit-Steuerelements für ein Ausgabegerät wie einen Drucker zu formatieren.

Nachdem Sie diese Nachricht zum Formatieren eines Textbereichs verwendet haben, ist es wichtig, zwischengespeicherte Informationen freizugeben, indem Sie **EM \_ FORMATRANGE** erneut senden, aber *wenn lParam* auf **NULL** festgelegt ist, tritt andernfalls ein Speicherverlust auf. Nachdem Sie diese Nachricht für ein Gerät verwendet haben, müssen Sie zwischengespeicherte Informationen freigeben, bevor Sie sie erneut für ein anderes Gerät verwenden.

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

[**EM \_ DISPLAYBAND**](em-displayband.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Drucken von Rich Edit-Steuerelementen](printing-rich-edit-controls.md)
</dt> </dl>

 

 





