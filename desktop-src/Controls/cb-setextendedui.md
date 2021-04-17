---
title: CB_SETEXTENDEDUI Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ setextendedui-Nachricht, um entweder die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche für ein Kombinations Feld mit dem Format CBS \_ Dropdown oder CBS \_ DropDownList auszuwählen.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- Windows-Steuerelemente für CB_SETEXTENDEDUI Meldung
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476635"
---
# <a name="cb_setextendedui-message"></a>CB- \_ messagetendedui-Nachricht

Eine Anwendung sendet eine **CB \_ setextendedui** -Nachricht, um entweder die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche für ein Kombinations Feld mit dem Format [**CBS \_ Dropdown**](combo-box-styles.md) oder [**CBS \_ DropDownList**](combo-box-styles.md) auszuwählen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **boolescher** Wert, der angibt, ob für das Kombinations Feld die erweiterte Benutzeroberfläche (**true**) oder die Standardbenutzer Oberfläche (**false**) verwendet wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert CB \_ okay. Wenn ein Fehler auftritt, ist es CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Standardmäßig wird die Liste mit dem F4-Schlüssel geöffnet oder geschlossen, und der nach-unten-Pfeil ändert die aktuelle Auswahl. In der erweiterten Benutzeroberfläche ist die F4-Taste deaktiviert, und die nach-unten-Taste öffnet die Dropdown Liste. Das Mausrad, das normalerweise durch die Elemente in der Liste führt, hat keine Auswirkung, wenn die erweiterte Benutzeroberfläche festgelegt ist.

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

[**CB \_ getextendedui**](cb-getextendedui.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Kombinations Feld-Features](combo-box-features.md)
</dt> </dl>

 

 





