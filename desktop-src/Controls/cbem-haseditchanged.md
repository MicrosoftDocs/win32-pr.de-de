---
title: CBEM_HASEDITCHANGED (Commctrl.h)
description: Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungssteuerfelds geändert hat.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5949827dbabf962ec9a9e9bd9d3b6d27d09a3b7e62f7fc71f2c4343e8ce370
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528040"
---
# <a name="cbem_haseditchanged-message"></a>CBEM \_ HASEDITCHANGED-Nachricht

Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungssteuerfelds geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn der Text im Bearbeitungsfeld des Steuerelements geändert wurde, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld-Steuerelement, wenn es auf den [**CBS-DROPDOWN-Stil \_ festgelegt**](combo-box-styles.md) ist. Sie können das Fensterhand handle des Bearbeitungsfeld-Steuerelements abrufen, indem Sie eine [**CBEM \_ GETEDITCONTROL-Nachricht**](cbem-geteditcontrol.md) senden.

Wenn der Benutzer mit der Bearbeitung beginnt, erhalten Sie eine [CBEN \_ BEGINEDIT-Benachrichtigung.](cben-beginedit.md) Wenn die Bearbeitung abgeschlossen ist oder sich der Fokus ändert, erhalten Sie eine [CBEN \_ ENDEDIT-Benachrichtigung.](cben-endedit.md) Die **CBEM \_ HASEDITCHANGED-Nachricht** ist nur nützlich, um zu bestimmen, ob der Text geändert wurde, wenn er vor der CBEN \_ ENDEDIT-Benachrichtigung gesendet wird. Wenn die Nachricht anschließend gesendet wird, wird FALSE **zurückgegeben.** Angenommen, der Benutzer beginnt, den Text im Bearbeitungsfeld zu bearbeiten, ändert jedoch den Fokus und generiert eine CBEN \_ ENDEDIT-Benachrichtigung. Wenn Sie dann eine **CBEM \_ HASEDITCHANGED-Nachricht** senden, wird **FALSE** zurückgegeben, obwohl der Text geändert wurde.

Der [**CBS \_ SIMPLE-Stil**](combo-box-styles.md) funktioniert nicht ordnungsgemäß mit **CBEM \_ HASEDITCHANGED**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





