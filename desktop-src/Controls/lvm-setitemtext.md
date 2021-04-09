---
title: LVM_SETITEMTEXT Meldung (kommstrg. h)
description: Ändert den Text eines Listen Ansichts Elements oder unter Elements. Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" mit dem Text "ListView" senden \_ .
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- Windows-Steuerelemente für LVM_SETITEMTEXT Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858940"
---
# <a name="lvm_setitemtext-message"></a>LVM- \_ Nachricht

Ändert den Text eines Listen Ansichts Elements oder unter Elements. Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" mit dem [**\_ Text "ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Listen Ansichts Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur. Der **iSubItem** -Member ist der Index des unter Elements, oder er kann NULL sein, um die Element Bezeichnung festzulegen. Der **pszText** -Member ist die Adresse einer null-terminierten Zeichenfolge, die den neuen Text enthält. Er kann auch **null** sein. Der **pszText** -Member kann auch LPSTR \_ textcallback sein, um ein Rückruf Element anzugeben, für das das übergeordnete Fenster den Text speichert. In diesem Fall sendet das Listenansicht-Steuerelement einen [**LVN \_ getdispinfo**](lvn-getdispinfo.md) -Benachrichtigungs Code, wenn er den Text benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie diese Meldung explizit senden, wird **true** zurückgegeben, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_** "S" (Unicode) und " **LVM" \_** (ANSI)<br/>           |



 

 





