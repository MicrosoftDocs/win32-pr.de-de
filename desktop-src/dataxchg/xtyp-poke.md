---
title: XTYP_POKE Transaktion (Ddeml. h)
description: Ein Client verwendet die XYP \_ Poke-Transaktion, um nicht angeforderte Daten an den Server zu senden. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt diese Transaktion, wenn ein Client xType \_ poke in der DDE clienttransaction-Funktion angibt.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949789"
---
# <a name="xtyp_poke-transaction"></a>XYP- \_ Poke-Transaktion

Ein Client verwendet die **XYP \_ Poke** -Transaktion, um nicht angeforderte Daten an den Server zu senden. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client **xType \_ Poke** in der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*UF* 
</dt> <dd>

Das Format der vom Server gesendeten Daten.

</dd> <dt>

*has* 
</dt> <dd>

Ein Handle für die Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themen Namen.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Elementnamen.

</dd> <dt>

*hdata* 
</dt> <dd>

Ein Handle für die Daten, die vom Client an den Server gesendet werden.

</dd> <dt>

*dwData1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Server Rückruffunktion sollte das **DDE- \_ faktorflag** zurückgeben, wenn diese Transaktion verarbeitet wird, das **DDE \_ fbusy** -Flag, wenn es zu stark ausgelastet ist, um diese Transaktion zu verarbeiten, oder das **DDE \_ fnotverarbeitete** -Flag, wenn es diese Transaktion ablehnt.

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_ Pokes** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.

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

[**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

