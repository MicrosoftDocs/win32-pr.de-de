---
title: LVN_COLUMNCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Spaltenheader geklickt wurde, während sich das Listenansicht-Steuerelement im Berichtsmodus befand. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- Windows-Steuerelemente für LVN_COLUMNCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040170"
---
# <a name="lvn_columnclick-notification-code"></a>LVN- \_ ColumnClick-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Spaltenheader geklickt wurde, während sich das Listenansicht-Steuerelement im Berichtsmodus befand. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur. Der **iItem** -Member ist-1, und der **iSubItem** -Member identifiziert die Spalte. Alle anderen Elemente sind 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

\_Wenn Sie das Format von Spalten Headern in einem Listenansicht-Steuerelement mithilfe von Header Steuerungs Formaten wie z. b. hdf ändern, sendet das Steuerelement beim Klicken auf ein Header Element den [ \_ itemstatueiconfiguration](hdn-itemstateiconclick.md) -Benachrichtigungs Code von Hdn anstelle von LVN \_ ColumnClick.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





