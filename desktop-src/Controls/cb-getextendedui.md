---
title: CB_GETEXTENDEDUI Meldung (Winuser. h)
description: Bestimmt, ob ein Kombinations Feld über die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche verfügt.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- Windows-Steuerelemente für CB_GETEXTENDEDUI Meldung
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
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476656"
---
# <a name="cb_getextendedui-message"></a>CB \_ getextendedui-Nachricht

Bestimmt, ob ein Kombinations Feld über die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche verfügt.

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

Wenn das Kombinations Feld über die erweiterte Benutzeroberfläche verfügt, ist der Rückgabewert " **true**". Andernfalls ist Sie **false**.

## <a name="remarks"></a>Bemerkungen

Standardmäßig wird die Liste mit dem F4-Schlüssel geöffnet oder geschlossen, und der nach-unten-Pfeil ändert die aktuelle Auswahl. In einem Kombinations Feld mit der erweiterten Benutzeroberfläche ist die F4-Taste deaktiviert. durch Drücken der nach-unten-Taste wird die Dropdown Liste geöffnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB- \_ textendedui**](cb-setextendedui.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Kombinations Feld-Features](combo-box-features.md)
</dt> </dl>

 

 





