---
title: TBN_DUPACCELERATOR Benachrichtigungs Code (kommctrl. h)
description: Gibt an, ob eine Zugriffstaste auf zwei oder mehr aktiven Symbolleisten verwendet werden kann. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- Windows-Steuerelemente für TBN_DUPACCELERATOR Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040837"
---
# <a name="tbn_dupaccelerator-notification-code"></a>TBN- \_ dupaccelerators-Benachrichtigungs Code

Gibt an, ob eine Zugriffstaste auf zwei oder mehr aktiven Symbolleisten verwendet werden kann. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die eine Zugriffstaste bietet und einen Wert empfängt, der angibt, ob mehrere Symbolleisten auf dasselbe Zeichen reagieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss die **nmtbdupaccelerator** -Struktur wie folgt deklarieren:

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





