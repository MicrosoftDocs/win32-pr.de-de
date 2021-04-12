---
title: LVM_SUBITEMHITTEST Meldung (kommstrg. h)
description: Bestimmt, welches Listen Ansichts Element oder Unterelement an einer bestimmten Position liegt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ subitemhittest-Makros senden.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Windows-Steuerelemente für LVM_SUBITEMHITTEST Meldung
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475366"
---
# <a name="lvm_subitemhittest-message"></a>LVM \_ subitemhittest-Meldung

Bestimmt, welches Listen Ansichts Element oder Unterelement an einer bestimmten Position liegt. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ subitemhittest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss den Wert 0 (null) haben. **Windows Vista.** Sollte-1 sein, wenn das **igroup** -Mitglied von *LPARAM* abgerufen werden soll.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) -Struktur. Die [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur innerhalb von " **lvhittestinfo** " sollte auf die Client Koordinaten festgelegt werden, damit Sie als Treffer getestet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ggf. den Index des getesteten Elements oder des unter Elements zurück, andernfalls-1. Wenn ein Element oder Unterelement an den angegebenen Koordinaten steht, werden die Felder der Struktur " [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) " mit den entsprechenden Treffer Informationen aufgefüllt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

