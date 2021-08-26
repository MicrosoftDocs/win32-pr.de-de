---
title: TVM_GETITEM (Commctrl.h)
description: Ruft einige oder alle Attribute eines Strukturansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItem-Makros senden.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425b0200df62b1cfcbc18556ad12513e43cebadf6e5742b36880464fad195fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984890"
---
# <a name="tvm_getitem-message"></a>TVM \_ GETITEM-Nachricht

Ruft einige oder alle Attribute eines Strukturansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die die Informationen zum Abrufen und Empfangen von Informationen über das Element angibt. Ab [Version 4.71](common-control-versions.md) können Sie stattdessen eine [**TVITEMEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Wenn die Nachricht gesendet wird, identifiziert das **hItem-Element** der [**TVITEM-**](/windows/win32/api/commctrl/ns-commctrl-tvitema) oder [**TVITEMEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) das Element, über das Informationen abgerufen werden, und das Maskenelement gibt die abzurufenden Attribute an. 

Wenn das TVIF TEXT-Flag im Maskenmitglied der \_ [**TVITEM-**](/windows/win32/api/commctrl/ns-commctrl-tvitema) oder [**TVITEMEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) festgelegt ist, muss das  **pszText-Member** auf einen gültigen Puffer zeigen, und das **cchTextMax-Member** muss auf die Anzahl der Zeichen in diesem Puffer festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ GETITEMW** (Unicode) und **TVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





