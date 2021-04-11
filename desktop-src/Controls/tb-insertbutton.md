---
title: TB_INSERTBUTTON Meldung (kommstrg. h)
description: Fügt eine Schaltfläche in eine Symbolleiste ein.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- Windows-Steuerelemente für TB_INSERTBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103342"
---
# <a name="tb_insertbutton-message"></a>TB \_ InsertButton-Meldung

Fügt eine Schaltfläche in eine Symbolleiste ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index einer Schaltfläche. Die Meldung fügt die Schaltfläche "neu" auf der linken Seite dieser Schaltfläche ein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur, die Informationen über die einzufügende Schaltfläche enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Insertbuttonw** (Unicode) und **TB \_ insertbuttona** (ANSI)<br/>           |



 

 





