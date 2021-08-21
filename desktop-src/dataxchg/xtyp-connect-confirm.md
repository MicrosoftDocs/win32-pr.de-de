---
title: XTYP_CONNECT_CONFIRM Transaktion (Ddeml.h)
description: Eine dynamische Daten Exchange-Serverrückruffunktion (DDE), DdeCallback, empfängt die XTYP CONNECT CONFIRM-Transaktion, um zu bestätigen, dass eine Konversation mit einem Client hergestellt wurde, und um dem Server das Konversationshandge zur Verfügung zu \_ \_ stellen.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM von Transaktionsdaten Exchange
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0259540801a49bc631dc60e33979a8730b46bdfc06ac81142098e851b8a51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499080"
---
# <a name="xtyp_connect_confirm-transaction"></a>XTYP \_ CONNECT \_ CONFIRM-Transaktion

Die Rückruffunktion des dynamische Daten Exchange-Servers [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt die **XTYP \_ CONNECT \_ CONFIRM-Transaktion,** um zu bestätigen, dass eine Konversation mit einem Client hergestellt wurde, und um dem Server das Konversationshandge zur Verfügung zu stellen. Das System sendet diese Transaktion als Ergebnis einer vorherigen [**XTYP \_ CONNECT-**](xtyp-connect.md) oder [**XTYP \_ WILDCONNECT-Transaktion.**](xtyp-wildconnect.md)


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*hconv* 
</dt> <dd>

Ein Handle für die neue Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themennamen, für den die Konversation eingerichtet wurde.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Dienstnamen, für den die Konversation eingerichtet wurde.

</dd> <dt>

*hdata* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Gibt an, ob der Client die gleiche Anwendungsinstanz wie der Server ist. Wenn der Parameter 1 ist, ist der Client dieselbe Instanz. Wenn der Parameter 0 ist, ist der Client eine andere Instanz.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Transaktion wird gefiltert, wenn die Serveranwendung das **CBF \_ SKIP CONNECT \_ \_ CONFIRMS-Flag** in der [**DdeInitialize-Funktion angegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) hat.

Ein Server kann diesen Transaktionstyp nicht blockieren. Der **CBR \_ BLOCK-Rückgabecode** wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

