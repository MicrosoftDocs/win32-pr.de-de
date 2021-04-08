---
title: XTYP_DISCONNECT Transaktion (Ddeml. h)
description: Die DDE Dynamischer Datenaustausch-Rückruffunktion (DDE Callback) einer Anwendung empfängt die XYP \_ Disconnect-Transaktion, wenn der Partner der Anwendung in einer Konversation die DDE Disconnect-Funktion verwendet, um die Konversation zu beenden.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- XTYP_DISCONNECT Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740329"
---
# <a name="xtyp_disconnect-transaction"></a>XYP- \_ Disconnect-Transaktion

Die DDE Dynamischer Datenaustausch-Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) einer Anwendung empfängt die **XYP \_ Disconnect** -Transaktion, wenn der Partner der Anwendung in einer Konversation die [**DDE Disconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) -Funktion verwendet, um die Konversation zu beenden.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Ein Handle für die Beendigung der Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*hsz2* 
</dt> <dd>

Nicht verwendet.

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

Gibt an, ob es sich bei den Partnern in der Konversation um dieselbe Anwendungs Instanz handelt. Wenn dieser Parameter 1 ist, handelt es sich bei den Partnern um dieselbe Instanz. Wenn dieser Parameter 0 ist, sind die Partner unterschiedliche Instanzen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn die Anwendung das Flag " **CBF \_ Skip \_ Disconnects** " in der Funktion " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) " angegeben hat.

Die Anwendung kann den Status der beendeten Konversation abrufen, indem die [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) -Funktion aufgerufen wird, während diese Transaktion verarbeitet wird. Das Konversations Handle wird ungültig, nachdem die Rückruffunktion zurückgegeben hat.

Der Transaktionstyp kann von einer Anwendung nicht blockiert werden. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.

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

[**DDE Disconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**Dabqueryüberzeugungs Info**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

