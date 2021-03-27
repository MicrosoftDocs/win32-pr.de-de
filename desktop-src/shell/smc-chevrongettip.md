---
description: Fordert den Titel und den Text für ein Chevron-Infotipp für das von der zugehörigen smdata-Struktur angegebene Element an.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: SMC_CHEVRONGETTIP Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980176"
---
# <a name="smc_chevrongettip-message"></a>SMC \_ chevrongettip-Nachricht

Fordert den Titel und den Text für ein Chevron-Infotipp für das von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebene Element an.


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwsztiptitle* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine **null**-terminierte Unicode-Zeichenfolge mit dem Titel des infotip empfängt. Diese Zeichenfolge darf nicht länger sein als \_ die maximale Länge von Pfad Zeichen, einschließlich des abschließenden **null** -Zeichens.

</dd> <dt>

*pwsztiptext* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine **null**-terminierte Unicode-Zeichenfolge empfängt, die den Text des infotip enthält. Diese Zeichenfolge darf nicht länger sein als \_ die maximale Länge von Pfad Zeichen, einschließlich des abschließenden **null** -Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "S OK" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




