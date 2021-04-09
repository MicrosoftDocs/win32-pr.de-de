---
title: EM_FORMATRANGE Meldung (RichEdit. h)
description: Formatiert einen Textbereich in einem Rich-Edit-Steuerelement für ein bestimmtes Gerät.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- Windows-Steuerelemente für EM_FORMATRANGE Meldung
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
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858964"
---
# <a name="em_formatrange-message"></a>EM \_ FormatRange-Nachricht

Formatiert einen Textbereich in einem Rich-Edit-Steuerelement für ein bestimmtes Gerät.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der Text dargestellt werden soll. Wenn dieser Parameter nicht 0 (null) ist, wird der Text gerendert. Andernfalls wird der Text direkt gemessen.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**Format Bereichs**](/windows/desktop/api/Richedit/ns-richedit-formatrange) Struktur, die Informationen über das Ausgabegerät enthält, oder **null** , um vom-Steuerelement zwischengespeicherte Informationen freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den Index des letzten Zeichens zurück, das in den Bereich passt, plus 1.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird normalerweise verwendet, um den Inhalt eines Rich-Edit-Steuer Elements für ein Ausgabegerät wie einen Drucker zu formatieren.

Nachdem Sie diese Meldung verwendet haben, um einen Textbereich zu formatieren, ist es wichtig, dass Sie die zwischengespeicherten Informationen freigeben, indem Sie **EM \_ FormatRange** erneut senden, wobei *LPARAM* jedoch auf **null** festgelegt ist. andernfalls tritt ein Speicherfehler auf. Außerdem müssen Sie nach der Verwendung dieser Nachricht für ein Gerät zwischengespeicherte Informationen freigeben, bevor Sie es für ein anderes Gerät wieder verwenden.

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

[**EM \_ DisplayBand**](em-displayband.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Drucken von Rich Edit-Steuerelementen](printing-rich-edit-controls.md)
</dt> </dl>

 

 





