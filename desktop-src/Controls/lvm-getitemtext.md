---
title: LVM_GETITEMTEXT Meldung (kommstrg. h)
description: Ruft den Text eines Listen Ansichts Elements oder unter Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemText-Makros senden.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Windows-Steuerelemente für LVM_GETITEMTEXT Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105501"
---
# <a name="lvm_getitemtext-message"></a>LVM- \_ GetItemText-Nachricht

Ruft den Text eines Listen Ansichts Elements oder unter Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur. Um den Element Text abzurufen, legen Sie **iSubItem** auf NULL fest. Um den Text eines unter Elements abzurufen, legen Sie **iSubItem** auf den Index des unter Elements fest. Der **pszText** -Member verweist auf einen Puffer, der den Text empfängt. Der **cchtextmax** -Member gibt die Anzahl der Zeichen im Puffer an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie diese Meldung explizit senden, wird die Anzahl der Zeichen im **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Sie können diese Nachricht auch senden, indem Sie das [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) -Makro aufrufen. Dieses Makro gibt jedoch nicht die Länge der Zeichenfolge zurück.

**LVM \_ GetItemText** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Getitemtextw** (Unicode) und **LVM \_ getitemtexta** (ANSI)<br/>           |



 

 





