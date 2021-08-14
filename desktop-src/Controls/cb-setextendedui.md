---
title: CB_SETEXTENDEDUI Meldung (Winuser.h)
description: Eine Anwendung sendet eine CB \_ SETEXTENDEDUI-Nachricht, um entweder die Standard-Benutzeroberfläche oder die erweiterte Benutzeroberfläche für ein Kombinationsfeld auszuwählen, das den \_ CBS-DROPDOWN- oder \_ CBS-DROPDOWNLIST-Stil auflistet.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 36b77e67e555628475b9e40e78b7b0391d0b631fd77e6ff7f549700a553fa507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414222"
---
# <a name="cb_setextendedui-message"></a>CB \_ SETEXTENDEDUI-Meldung

Eine Anwendung sendet eine **CB \_ SETEXTENDEDUI-Nachricht,** um entweder die Standard-Benutzeroberfläche oder die erweiterte Benutzeroberfläche für ein Kombinationsfeld auszuwählen, das den [**\_ CBS-DROPDOWN-**](combo-box-styles.md) oder [**\_ CBS-DROPDOWNLIST-Stil**](combo-box-styles.md) auflistet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine **BOOL,** die angibt, ob das Kombinationsfeld die erweiterte Benutzeroberfläche **(TRUE)** oder die Standardbenutzeroberfläche **(FALSE)** verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, lautet der Rückgabewert CB \_ OK. Wenn ein Fehler auftritt, handelt es sich um CB \_ ERR.

## <a name="remarks"></a>Hinweise

Standardmäßig wird die Liste mit der Taste F4 geöffnet oder geschlossen, und der NACH-UNTEN-PFEIL ändert die aktuelle Auswahl. Auf der erweiterten Benutzeroberfläche ist die Taste F4 deaktiviert, und die NACH-UNTEN-TASTE öffnet die Dropdownliste. Das Mausrad, das normalerweise durch die Elemente in der Liste scrollt, hat keine Auswirkungen, wenn die erweiterte Benutzeroberfläche festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Kombinationsfeldfeatures](combo-box-features.md)
</dt> </dl>

 

 





