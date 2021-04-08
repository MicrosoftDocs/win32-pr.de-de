---
title: LVM_GETCOLUMNWIDTH Meldung (kommstrg. h)
description: Ruft die Breite einer Spalte in der Berichts-oder Listenansicht ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getColumnWidth-Makros senden.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Windows-Steuerelemente für LVM_GETCOLUMNWIDTH Meldung
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102899"
---
# <a name="lvm_getcolumnwidth-message"></a>LVM \_ getColumnWidth-Nachricht

Ruft die Breite einer Spalte in der Berichts-oder Listenansicht ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der Spalte. Dieser Parameter wird in der Listenansicht ignoriert.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Spaltenbreite zurück, wenn erfolgreich, andernfalls 0 (null). Wenn diese Nachricht an ein Listenansicht-Steuerelement mit dem [**LVS- \_ Berichts**](list-view-window-styles.md) Stil gesendet wird und die angegebene Spalte nicht vorhanden ist, ist der Rückgabewert nicht definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





