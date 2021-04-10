---
title: BM_SETCHECK Meldung (Winuser. h)
description: Legt den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens fest. Sie können diese Nachricht explizit oder mithilfe des Schaltflächen \_ setcheck-Makros senden.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- Windows-Steuerelemente für BM_SETCHECK Meldung
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040188"
---
# <a name="bm_setcheck-message"></a>BM- \_ setcheck-Meldung

Legt den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens fest. Sie können diese Nachricht explizit oder mithilfe des Schaltflächen [**\_ setcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Status der Überprüfung. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**BST \_ aktiviert**</dt> </dl>                   | Legt den Schaltflächen Zustand auf aktiviert fest.<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ unbestimmt**</dt> </dl> | Legt den Zustand der Schaltfläche auf abgeblendet fest und gibt einen unbestimmten Zustand an. Verwenden Sie diesen Wert nur, wenn die Schaltfläche den Stil " [**\_ 3STATE**](button-styles.md) " oder " [**SB \_ AUTO3STATE**](button-styles.md) " aufweist.<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**BST \_ deaktiviert**</dt> </dl>             | Legt den Schaltflächen Zustand auf "deaktiviert" fest.<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Die **BM- \_ setcheck** -Nachricht hat keine Auswirkung auf die pushschaltflächen.

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

[**BM \_ getcheck**](bm-getcheck.md)
</dt> <dt>

[**BM \_ GetState**](bm-getstate.md)
</dt> <dt>

[**BM \_ SetState**](bm-setstate.md)
</dt> </dl>

 

 





