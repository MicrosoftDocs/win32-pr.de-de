---
title: BM_SETCHECK (Winuser.h)
description: Legt den Häkchenzustand eines Optionsfelds oder Kontrollkästchens fest. Sie können diese Nachricht explizit oder mithilfe des Button \_ SetCheck-Makros senden.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK von Windows-Steuerelementen
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
ms.openlocfilehash: 171515cb3c8498537bd0f9cc6d8c06017ff9d5d00f5505e193862f6cf9ebff76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674803"
---
# <a name="bm_setcheck-message"></a>BM \_ SETCHECK-Meldung

Legt den Häkchenzustand eines Optionsfelds oder Kontrollkästchens fest. Sie können diese Nachricht explizit oder mithilfe des [**Button \_ SetCheck-Makros**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Überprüfungszustand. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**BST \_ CHECKED**</dt> </dl>                   | Legt den Schaltflächenzustand auf "Überprüft" fest.<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ UNBESTIMMT**</dt> </dl> | Legt den Schaltflächenzustand auf grau fest und gibt einen unbestimmten Zustand an. Verwenden Sie diesen Wert nur, wenn die Schaltfläche den [**Stil BS \_ 3STATE**](button-styles.md) oder [**BS \_ AUTO3STATE**](button-styles.md) hat.<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**BST \_ UNCHECKED**</dt> </dl>             | Legt den Schaltflächenzustand auf "Cleared" fest.<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die **BM \_ SETCHECK-Meldung** hat keine Auswirkungen auf Schaltflächen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[**BM \_ GETCHECK**](bm-getcheck.md)
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





