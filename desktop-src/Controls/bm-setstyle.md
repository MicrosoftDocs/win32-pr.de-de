---
title: BM_SETSTYLE Meldung (Winuser. h)
description: Legt den Stil einer Schaltfläche fest. Sie können diese Nachricht explizit senden oder das SetStyle-Makro der Schaltfläche verwenden \_ .
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Windows-Steuerelemente für BM_SETSTYLE Meldung
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949601"
---
# <a name="bm_setstyle-message"></a>BM- \_ SetStyle-Nachricht

Legt den Stil einer Schaltfläche fest. Sie können diese Nachricht explizit senden oder das [**\_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) -Makro der Schaltfläche verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Stil der Schaltfläche. Dieser Parameter kann eine Kombination von Schaltflächen Stilen sein. Eine Tabelle mit Schaltflächen Formaten finden Sie unter [Button Styles](button-styles.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) von *LPARAM* ist ein **boolescher** Wert, der angibt, ob die Schaltfläche neu gezeichnet werden soll. Mit dem Wert **true** wird die Schaltfläche neu gezeichnet. bei einem Wert von **false** wird die Schaltfläche nicht neu gezeichnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

