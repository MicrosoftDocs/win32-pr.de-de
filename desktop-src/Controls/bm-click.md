---
title: BM_CLICK Meldung (Winuser. h)
description: Simuliert den Benutzer, der auf eine Schaltfläche klickt. Diese Meldung bewirkt, dass die Schaltfläche die \_ lbuttondown-und die WM \_ -lbuttonup-Meldungen empfängt \_
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- Windows-Steuerelemente für BM_CLICK Meldung
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040314"
---
# <a name="bm_click-message"></a>BM- \_ Click-Nachricht

Simuliert den Benutzer, der auf eine Schaltfläche klickt. Diese Meldung bewirkt, dass die Schaltfläche [**die \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -und die [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldungen empfängt [ \_](bn-clicked.md)

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

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn sich die Schaltfläche in einem Dialogfeld befindet und das Dialogfeld nicht aktiv ist, kann die **BM- \_ Click** -Nachricht fehlschlagen. Um den Erfolg in dieser Situation zu gewährleisten, müssen **\_ Sie** [**die Funktion "" in der Funktion**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) "" von "".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

