---
title: TBN_WRAPHOTITEM Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt eine Anwendung mit zwei oder mehr Symbolleisten, dass das heiße Element gerade geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- Windows-Steuerelemente für TBN_WRAPHOTITEM Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476299"
---
# <a name="tbn_wraphotitem-notification-code"></a>TBN- \_ wraphotitem-Benachrichtigungs Code

Benachrichtigt eine Anwendung mit zwei oder mehr Symbolleisten, dass das heiße Element gerade geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die das alte Hot-Element (**iStart**) enthält, und ob das neue heiße Element vor dem Element (**Idir** =-1) oder danach (**Idir** = 1) ist. Außerdem wird ein Grund dafür angezeigt, warum das heiße Element geändert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True** , wenn die Anwendung die Änderung des aktiven Elements selbst verarbeitet. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Die **nmtbwraphotitem** -Struktur muss von der Anwendung wie folgt definiert werden:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





