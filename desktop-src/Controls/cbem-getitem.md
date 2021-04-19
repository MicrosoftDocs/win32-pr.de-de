---
title: CBEM_GETITEM Meldung (kommstrg. h)
description: Ruft Element Informationen für ein bestimmtes ComboBoxEx-Element ab.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- Windows-Steuerelemente für CBEM_GETITEM Meldung
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342870"
---
# <a name="cbem_getitem-message"></a>CBEM \_ GetItem-Meldung

Ruft Element Informationen für ein bestimmtes ComboBoxEx-Element ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur, die die Element Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Wenn die Nachricht gesendet wird, müssen die Member **iItem** und **Mask** der Struktur festgelegt werden, um den Index des Ziel Elements und den Typ der abzurufenden Informationen anzugeben. Andere Mitglieder werden nach Bedarf festgelegt. Zum Abrufen von Text müssen Sie z. b. das cbeif \_ -textflag in **Mask** festlegen und **cchtextmax** einen Wert zuweisen. Wenn Sie den **iItem** -Member auf-1 festlegen, wird das im Bearbeitungs Steuerelement angezeigte Element abgerufen.

Wenn das cbeif- \_ textflag im **Mask** -Member der [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur festgelegt ist, kann das Steuerelement den **pszText** -Member der Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text zu füllen. Anwendungen sollten nicht davon ausgehen, dass der Text immer in den angeforderten Puffer eingefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEM \_ Getitemw** (Unicode) und **CBEM \_ getitema** (ANSI)<br/>                 |



 

 





