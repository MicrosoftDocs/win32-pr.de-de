---
title: TBN_WRAPACCELERATOR Benachrichtigungs Code (kommctrl. h)
description: Fordert den Index der Schaltfläche in einem oder mehreren Symbolleisten an, der dem angegebenen Zugriffstasten Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- Windows-Steuerelemente für TBN_WRAPACCELERATOR Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340983"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>TBN- \_ wrapaccelerator-Benachrichtigungs Code

Fordert den Index der Schaltfläche in einem oder mehreren Symbolleisten an, der dem angegebenen Zugriffstasten Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die das Tastenkombination-Zeichen enthält und den Index der entsprechenden Schaltfläche empfängt. Der Index ist-1, wenn die Zugriffstaste keinem Befehl entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True** , wenn ein Index zurückgegeben wird, andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Anwendungen mit einem oder mehreren Symbolleisten können diesen Benachrichtigungs Code erhalten.

Die **nmtbwrapaccelerator** -Struktur muss von der Anwendung wie folgt definiert werden:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





