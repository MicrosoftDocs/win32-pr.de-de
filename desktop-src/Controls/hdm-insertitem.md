---
title: HDM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in ein Header Steuerelement ein. Sie können diese Nachricht explizit senden oder das-Header \_ InsertItem-Makro verwenden.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Windows-Steuerelemente für HDM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476818"
---
# <a name="hdm_insertitem-message"></a>HDM- \_ InsertItem-Meldung

Fügt ein neues Element in ein Header Steuerelement ein. Sie können diese Nachricht explizit senden oder das- [**Header \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, nach dem das neue Element eingefügt werden soll. Das neue Element wird am Ende des Header Steuer Elements eingefügt, wenn *wParam* größer oder gleich der Anzahl der Elemente im Steuerelement ist. Wenn *wParam* gleich 0 (null) ist, wird das neue Element am Anfang des Header Steuer Elements eingefügt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur, die Informationen über das neue Element enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des neuen Elements zurück, wenn erfolgreich, andernfalls-1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDM \_ Insertitemw** (Unicode) und **HDM \_ insertitema** (ANSI)<br/>             |



 

 





