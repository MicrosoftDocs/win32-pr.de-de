---
title: CBEM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in einem ComboBoxEx-Steuerelement ein.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Windows-Steuerelemente für CBEM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345521"
---
# <a name="cbem_insertitem-message"></a>CBEM \_ InsertItem-Meldung

Fügt ein neues Element in einem ComboBoxEx-Steuerelement ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur, die Informationen über das einzufügende Element enthält. Wenn die Nachricht gesendet wird, muss der **iItem** -Member so festgelegt werden, dass er den NULL basierten Index angibt, an dem das Element eingefügt werden soll. Wenn Sie ein Element am Ende der Liste einfügen möchten, legen Sie den **iItem** -Member auf-1 fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index zurück, bei dem das neue Element eingefügt wurde, andernfalls-1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEM \_ Insertitemw** (Unicode) und **CBEM \_ insertitema** (ANSI)<br/>           |



 

 





