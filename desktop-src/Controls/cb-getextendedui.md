---
title: CB_GETEXTENDEDUI Meldung (Winuser.h)
description: Bestimmt, ob ein Kombinationsfeld über die Standardbenutzerschnittstelle oder die erweiterte Benutzeroberfläche verfügt.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05201b0986b114e97523716edacc6fe391908d3ed2841d36bf7578a6455f42a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089220"
---
# <a name="cb_getextendedui-message"></a>CB \_ GETEXTENDEDUI-Nachricht

Bestimmt, ob ein Kombinationsfeld über die Standardbenutzerschnittstelle oder die erweiterte Benutzeroberfläche verfügt.

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

Wenn das Kombinationsfeld über die erweiterte Benutzeroberfläche verfügt, ist der Rückgabewert **TRUE.** Andernfalls ist es **FALSE.**

## <a name="remarks"></a>Hinweise

Standardmäßig wird die Liste mit der Taste F4 geöffnet oder geschlossen, und der NACH-UNTEN-PFEIL ändert die aktuelle Auswahl. In einem Kombinationsfeld mit der erweiterten Benutzeroberfläche ist die F4-Taste deaktiviert, und durch Drücken der NACH-UNTEN-TASTE wird die Dropdownliste geöffnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Kombinationsfeldfeatures](combo-box-features.md)
</dt> </dl>

 

 





