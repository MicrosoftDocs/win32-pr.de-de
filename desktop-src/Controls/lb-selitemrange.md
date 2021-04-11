---
title: LB_SELITEMRANGE Meldung (Winuser. h)
description: Aktiviert oder deaktiviert ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Windows-Steuerelemente für LB_SELITEMRANGE Meldung
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
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040896"
---
# <a name="lb_selitemrange-message"></a>LB- \_ selitemrange-Nachricht

Aktiviert oder deaktiviert ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

" **True** ", um den Bereich von Elementen auszuwählen, oder " **false** ", um die Auswahl zu deaktivieren.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den NULL basierten Index des ersten Elements an, das ausgewählt werden soll. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den NULL basierten Index des letzten Elements an, das ausgewählt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung nur für Listenfelder mit Mehrfachauswahl.

Diese Meldung kann einen Bereich nur innerhalb der ersten 65.536 Elemente auswählen.

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

[**LB- \_ selitemrangeex**](lb-selitemrangeex.md)
</dt> <dt>

[**LB- \_ Sekunden**](lb-setsel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makelparam**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

