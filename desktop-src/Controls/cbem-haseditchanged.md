---
title: CBEM_HASEDITCHANGED Meldung (kommstrg. h)
description: Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungs Steuer Elements geändert hat.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- Windows-Steuerelemente für CBEM_HASEDITCHANGED Meldung
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
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957192"
---
# <a name="cbem_haseditchanged-message"></a>CBEM \_ haseditchanged-Meldung

Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungs Steuer Elements geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn der Text im Bearbeitungsfeld des Steuer Elements geändert wurde, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld-Steuerelement, wenn es auf den [**CBS- \_ Dropdown**](combo-box-styles.md) Stil festgelegt ist. Sie können das Fenster Handle des Bearbeitungsfeld Steuer Elements abrufen, indem Sie eine [**CBEM \_ geteditcontrol**](cbem-geteditcontrol.md) -Nachricht senden.

Wenn der Benutzer mit der Bearbeitung beginnt, erhalten Sie eine [cben \_ BeginEdit](cben-beginedit.md) -Benachrichtigung. Wenn die Bearbeitung oder der Fokus geändert wird, erhalten Sie eine [cben \_ EndEdit](cben-endedit.md) -Benachrichtigung. Die Meldung " **CBEM \_ haseditchanged** " ist nur hilfreich, um zu bestimmen, ob der Text geändert wurde, wenn er vor der cben- \_ EndEdit-Benachrichtigung gesendet wird. Wenn die Nachricht später gesendet wird, wird **false** zurückgegeben. Angenommen, der Benutzer beginnt, den Text im Bearbeitungsfeld zu bearbeiten, ändert jedoch den Fokus und erzeugt eine cben \_ EndEdit-Benachrichtigung. Wenn Sie dann eine **CBEM \_ haseditchanged** -Nachricht senden, wird **false** zurückgegeben, auch wenn der Text geändert wurde.

Der [**\_ einfache CBS**](combo-box-styles.md) -Stil funktioniert mit **CBEM \_ haseditchanged** nicht ordnungsgemäß.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





