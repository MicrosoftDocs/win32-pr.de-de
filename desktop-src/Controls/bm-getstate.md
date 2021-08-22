---
title: BM_GETSTATE (Winuser.h)
description: Ruft den Zustand einer Schaltfläche oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das Button \_ GetState-Makro verwenden.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd44921c61477e26cd5570fcbaa6f96a4e61f96ee22ad1c705bf553788d8cfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674840"
---
# <a name="bm_getstate-message"></a>BM \_ GETSTATE-Nachricht

Ruft den Zustand einer Schaltfläche oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das [**Button \_ GetState-Makro**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) verwenden.

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

Der Rückgabewert gibt den aktuellen Zustand der Schaltfläche an. Es handelt sich um eine Kombination der folgenden Werte.



| Rückgabecode                                                                                        | Beschreibung                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>        | Die Schaltfläche ist überprüft.<br/>                                                                                                                                                                                        |
| <dl> <dt>**\_BST-DROPDOWNLISTEPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md). Die Schaltfläche befindet sich im Dropdownzustand. Gilt nur, wenn die Schaltfläche den [**\_ TBSTYLE-DROPDOWN-Stil**](toolbar-control-and-button-styles.md) auflistet.<br/> |
| <dl> <dt>**BST \_ FOCUS**</dt> </dl>          | Die Schaltfläche hat den Tastaturfokus.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ HOT**</dt> </dl>            | Die Schaltfläche ist heiß. Das bedeutet, dass die Maus daraufzeigert.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ UNBESTIMMT**</dt> </dl>  | Der Zustand der Schaltfläche ist unbestimmt. Gilt nur, wenn die Schaltfläche den [**Stil BS \_ 3STATE**](button-styles.md) oder [**BS \_ AUTO3STATE**](button-styles.md) hat.<br/>                    |
| <dl> <dt>**BST \_ PUSHED**</dt> </dl>         | Die Schaltfläche wird im Push-Zustand angezeigt.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>      | Kein besonderer Zustand. Entspricht 0 (null).<br/>                                                                                                                                                                         |



 

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

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





