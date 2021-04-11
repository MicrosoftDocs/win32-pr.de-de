---
title: BM_GETCHECK Meldung (Winuser. h)
description: Ruft den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das Schaltfläche \_ getcheck-Makro verwenden.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- Windows-Steuerelemente für BM_GETCHECK Meldung
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105770"
---
# <a name="bm_getcheck-message"></a>BM- \_ getcheck-Meldung

Ruft den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das [**Schaltfläche \_ getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) -Makro verwenden.

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

Der Rückgabewert einer Schaltfläche, die mit dem Format " [**\_ Auto Checkbox**](button-styles.md)", " [**SB \_ AUTORADIOBUTTON**](button-styles.md)", "SB [**\_ AUTO3STATE**](button-styles.md)", "SB [**", " \_**](button-styles.md) [**SB \_ RadioButton**](button-styles.md)" oder " [**SB \_ 3STATE**](button-styles.md) " erstellt wurde, kann eines der folgenden sein.



| Rückgabecode                                                                                       | Beschreibung                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ aktiviert**</dt> </dl>       | Die Schaltfläche ist aktiviert.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ unbestimmt**</dt> </dl> | Die Schaltfläche ist abgeblendet und zeigt einen unbestimmten Zustand an (gilt nur, wenn die Schaltfläche den Typ " [**\_ 3STATE**](button-styles.md) " oder " [**SB \_ AUTO3STATE**](button-styles.md) " aufweist).<br/> |
| <dl> <dt>**BST \_ deaktiviert**</dt> </dl>     | Schaltfläche ist deaktiviert<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Schaltfläche einen anderen Stil als die aufgeführten hat, ist der Rückgabewert 0 (null).

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

[**BM \_ GetState**](bm-getstate.md)
</dt> <dt>

[**BM- \_ setcheck**](bm-setcheck.md)
</dt> </dl>

 

 





