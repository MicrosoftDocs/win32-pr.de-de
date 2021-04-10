---
title: LVM_SETITEM Meldung (kommstrg. h)
description: Legt einige oder alle Attribute eines Listen Ansichts Elements fest. Sie können auch LVM \_ SetItem senden, um den Text eines unter Elements festzulegen. Sie können diese Nachricht explizit oder mithilfe des ListView-Elements "ListView" senden \_ .
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- Windows-Steuerelemente für LVM_SETITEM Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040371"
---
# <a name="lvm_setitem-message"></a>LVM- \_ Nachricht

Legt einige oder alle Attribute eines Listen Ansichts Elements fest. Sie können auch LVM \_ SetItem senden, um den Text eines unter Elements festzulegen. Sie können diese Nachricht explizit oder mithilfe des [**ListView-Elements \_ "ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die die neuen Element Attribute enthält. Die Member **iItem** und **iSubItem** identifizieren das Element oder das Unterelement, und das **Masken** Element gibt an, welche Attribute festgelegt werden sollen. Wenn das **Masken** Element den lvif \_ -Textwert angibt, ist der **pszText** -Member die Adresse einer auf NULL endenden Zeichenfolge, und das **cchtextmax** -Element wird ignoriert. Wenn das **Masken** Element den lvif- \_ Zustandswert angibt, gibt der **statemask** -Member an, welche Element Zustände  geändert werden sollen und ob das statusmember die Werte für diese Zustände enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Um die Attribute eines Listen Ansichts Elements festzulegen, legen Sie den **iItem** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur auf den Index des Elements fest, und legen Sie den **iSubItem** -Member auf NULL fest. Für ein Element können Sie die Member **State**, **pszText**, **iImage** und **LPARAM** der **lvitem** -Struktur festlegen.

Um den Text eines unter Elements festzulegen, legen Sie die Member **iItem** und **iSubItem** auf das jeweilige Unterelement fest, und verwenden Sie den Member **pszText** , um den Text anzugeben. Alternativ können Sie das [**ListView \_ setitemtext**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) -Makro verwenden, um den Text eines unter Elements festzulegen. Sie können die **State** -oder **LPARAM** -Member nicht für unter Elemente festlegen, da unter Elemente nicht über diese Attribute verfügen. In Version 4,70 und höher können Sie den **iImage** -Member für unter Elemente festlegen. Das Unterelement-Bild wird angezeigt, wenn das Listenansicht-Steuerelement das erweiterte LVS-Format "from [**\_ \_ subitemimages**](extended-list-view-styles.md) " aufweist. In früheren Versionen wird das Unterelement-Bild ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_** "S" (Unicode) und " **LVM \_** " (ANSI)<br/>                   |



 

 





