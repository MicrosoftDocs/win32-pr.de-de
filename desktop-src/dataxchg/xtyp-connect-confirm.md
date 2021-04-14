---
title: XTYP_CONNECT_CONFIRM Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt die xtipp \_ Connect \_ -Bestätigungs Transaktion, um zu bestätigen, dass eine Konversation mit einem Client hergestellt wurde, und um dem Server das Konversations handle bereitzustellen.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM Transaktionsdaten Austausch
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
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391972"
---
# <a name="xtyp_connect_confirm-transaction"></a>Xtipp \_ Connect- \_ Transaktion bestätigen

Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **xtipp \_ Connect- \_ Bestätigungs** Transaktion, um zu bestätigen, dass eine Konversation mit einem Client hergestellt wurde, und um dem Server das Konversations handle bereitzustellen. Das System sendet diese Transaktion als Ergebnis einer vorherigen [**xtipp \_ Connect**](xtyp-connect.md) -oder [**XYP \_ wildconnect**](xtyp-wildconnect.md) -Transaktion.


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

*UF* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*has* 
</dt> <dd>

Ein Handle für die neue Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themen Namen, für den die Konversation eingerichtet wurde.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Dienstnamen, für den die Konversation eingerichtet wurde.

</dd> <dt>

*hdata* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Gibt an, ob es sich bei dem Client um dieselbe Anwendungs Instanz wie der Server handelt. Wenn der-Parameter 1 ist, ist der Client dieselbe Instanz. Wenn der-Parameter 0 ist, ist der Client eine andere-Instanz.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag **CBF \_ Skip \_ Connect \_ bestätigt** in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.

Ein Server kann diesen Transaktionstyp nicht blockieren. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DDE Connect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

