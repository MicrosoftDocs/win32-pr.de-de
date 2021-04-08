---
title: BM_GETSTATE Meldung (Winuser. h)
description: Ruft den Zustand einer Schaltfläche oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das GetState-Makro der Schaltfläche verwenden \_ .
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- Windows-Steuerelemente für BM_GETSTATE Meldung
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
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949471"
---
# <a name="bm_getstate-message"></a>BM \_ GetState-Nachricht

Ruft den Zustand einer Schaltfläche oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das [**\_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) -Makro der Schaltfläche verwenden.

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
| <dl> <dt>**BST \_ aktiviert**</dt> </dl>        | Die Schaltfläche ist aktiviert.<br/>                                                                                                                                                                                        |
| <dl> <dt>**BST \_ dropdownpushübertragung**</dt> </dl> | [Windows Vista](common-control-versions.md). Die Schaltfläche befindet sich im Dropdown Zustand. Gilt nur, wenn die Schaltfläche den [**tbstyle- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil aufweist.<br/> |
| <dl> <dt>**BST- \_ Fokus**</dt> </dl>          | Die Schaltfläche verfügt über den Tastaturfokus.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ heiß**</dt> </dl>            | Die Schaltfläche ist "Hot". Das heißt, dass der Mauszeiger darüber bewegt wird.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ unbestimmt**</dt> </dl>  | Der Status der Schaltfläche ist unbestimmt. Gilt nur, wenn die Schaltfläche den Stil " [**\_ 3STATE**](button-styles.md) " oder " [**SB \_ AUTO3STATE**](button-styles.md) " aufweist.<br/>                    |
| <dl> <dt>**BST per \_ pushübertragung**</dt> </dl>         | Die Schaltfläche wird im gedrückten Zustand angezeigt.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ deaktiviert**</dt> </dl>      | Kein spezieller Zustand. Entspricht 0 (null).<br/>                                                                                                                                                                         |



 

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

[**BM \_ SetState**](bm-setstate.md)
</dt> </dl>

 

 





