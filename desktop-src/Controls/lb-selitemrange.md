---
title: LB_SELITEMRANGE Meldung (Winuser.h)
description: Wählt ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit mehrfacher Auswahl aus oder deaktiviert sie.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a08019f3d60e6c9bfe841067b48220b8fcfe75891c9bcc8db64bf28d219b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958599"
---
# <a name="lb_selitemrange-message"></a>LB \_ SELITEMRANGE-Nachricht

Wählt ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit mehrfacher Auswahl aus oder deaktiviert sie.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**TRUE,** um den Elementbereich auszuwählen, oder **FALSE,** um die Auswahl aufzuheben.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den nullbasierten Index des ersten auszuwählenden Elements an. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den nullbasierten Index des letzten auszuwählenden Elements an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, lautet der Rückgabewert LB \_ ERR.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Meldung nur mit Listenfeldern mit mehrfacher Auswahl.

Diese Nachricht kann einen Bereich nur innerhalb der ersten 65.536 Elemente auswählen.

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

[**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

