---
title: XTYP_ADVREQ Transaktion (Ddeml.h)
description: Die XTYP ADPROTOKOLLQ-Transaktion informiert den Server darüber, dass eine Advise-Transaktion für das angegebene Themennamen- und Elementnamenpaar aus steht und dass sich die Daten für das Themennamen- und Elementnamenpaar \_ geändert haben.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ Der Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e751f17fb8634b0a105a36af5036f07d0212532349c267e5526d5d41f09367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544885"
---
# <a name="xtyp_advreq-transaction"></a>XTYP \_ ADPROTOKOLLQ-Transaktion

Die **XTYP \_ ADPROTOKOLLQ-Transaktion** informiert den Server darüber, dass eine Advise-Transaktion für das angegebene Themennamen- und Elementnamenpaar aus steht und dass sich die Daten für das Themennamen- und Elementnamenpaar geändert haben. Das System sendet diese Transaktion an die DDE-Rückruffunktion (dynamische Daten Exchange), [*DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)nachdem der Server die [**DdePostAdvise-Funktion aufruft.**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Das Format, in dem die Daten an den Client übermittelt werden sollen.

</dd> <dt>

*hconv* 
</dt> <dd>

Ein Handle für die Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themennamen.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Elementnamen, der geändert wurde.

</dd> <dt>

*hdata* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Die Anzahl der **XTYP \_ ADTYPQ-Transaktionen,** die im Kontext des aktuellen Aufrufs der [**DdePostAdvise-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) für dasselbe Thema, Element und den gleichen Formatnamen verarbeitet werden müssen, im niedrig geordneten Wort. Die Anzahl ist 0 (null), wenn die **aktuelle XTYP \_ ADPROTOKOLLQ-Transaktion** die letzte ist. Ein Server kann diese Anzahl verwenden, um zu bestimmen, ob ein **HDATA \_ APPOWNED-Datenhand** handle für die Advise-Daten erstellt werden soll.

Das Wort in niedriger Reihenfolge wird auf **CADV \_ LATEACK** festgelegt, wenn die DDEML die **XTYP \_ ADDIZQ-Transaktion** ausgegeben hat, weil eine zu spät eintreffende DDE-ACK-Nachricht von einem Client ausgegeben wurde, der vom Server nicht ausgeführt \_ wird.

Das hochgeordnete Wort wird nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Server sollte zuerst die [**DdeCreateDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) aufrufen, um ein Datenhandle zu erstellen, das die geänderten Daten identifiziert, und dann das Handle zurückgeben. Der Server sollte NULL **zurückgeben,** wenn die Transaktion nicht abgeschlossen werden kann.

## <a name="remarks"></a>Hinweise

Ein Server kann diesen Transaktionstyp nicht blockieren. Der **CBR \_ BLOCK-Rückgabecode** wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

