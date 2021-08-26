---
title: BM_GETCHECK-Nachricht (Winuser.h)
description: Ruft den Kontrollkästchenzustand eines Optionsfelds oder Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das \_ Schaltflächenmakro GetCheck verwenden.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: e5eb87d98752bd0cd447d48c648bc4a55e93c3f8eb418a81a07e04113a86633a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921290"
---
# <a name="bm_getcheck-message"></a>BM \_ GETCHECK-Nachricht

Ruft den Kontrollkästchenzustand eines Optionsfelds oder Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das [**Schaltflächenmakro \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) verwenden.

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

Der Rückgabewert einer Schaltfläche, die mit dem Format [**BS \_ AUTOCHECKBOX,**](button-styles.md) [**BS \_ AUTORADIOBUTTON,**](button-styles.md) [**BS \_ AUTO3STATE,**](button-styles.md) [**BS \_ CHECKBOX,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)oder [**BS \_ 3STATE**](button-styles.md) erstellt wurde, kann einer der folgenden Sein.



| Rückgabecode                                                                                       | Beschreibung                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>       | Die Schaltfläche ist aktiviert.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ INDETERMINATE**</dt> </dl> | Die Schaltfläche ist grau und gibt einen unbestimmten Zustand an (gilt nur, wenn die Schaltfläche den [**Stil BS \_ 3STATE**](button-styles.md) oder [**BS \_ AUTO3STATE auf hat).**](button-styles.md)<br/> |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>     | Schaltfläche wird gelöscht<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Wenn die Schaltfläche über einen anderen Stil als die aufgeführten verfügt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





