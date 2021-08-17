---
title: XTYP_WILDCONNECT Transaktion (Ddeml.h)
description: Ermöglicht es einem Client, eine Konversation für jedes der Paare aus Dienstname und Themenname des Servers herzustellen, die mit dem angegebenen Dienst- und Themennamen übereinstimmen.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT von Transaktionsdaten Exchange
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b2b170a8d2362dec6311f935a5bc0bb92fa16a9b04270afc59d8fe5ad5c19f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914730"
---
# <a name="xtyp_wildconnect-transaction"></a>XTYP \_ WILDCONNECT-Transaktion

Ermöglicht es einem Client, eine Konversation für jedes der Paare aus Dienstname und Themenname des Servers herzustellen, die mit dem angegebenen Dienst- und Themennamen übereinstimmen. Eine DDE-Serverrückruffunktion [*(dynamische Daten Exchange), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt diese Transaktion, wenn ein Client einen NULL-Dienstnamen, einen **NULL-Themennamen** oder beides in einem Aufruf der [**DdeConnect-**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) oder [**DdeConnectList-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) angibt. 


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
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

Wird nicht verwendet.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themennamen. Wenn dieser Parameter **NULL ist,** fordert der Client eine Konversation für alle Vom Server unterstützten Themennamen an.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Dienstnamen. Wenn dieser Parameter **NULL ist,** fordert der Client eine Konversation für alle Vom Server unterstützten Dienstnamen an.

</dd> <dt>

*hdata* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Ein Zeiger auf eine [**CONVCONTEXT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-convcontext) die Kontextinformationen für die Konversation enthält. Wenn der Client keine DDEML-Anwendung ist, wird dieser Parameter auf 0 festgelegt.

</dd> <dt>

*dwData2* 
</dt> <dd>

Gibt an, ob der Client die gleiche Anwendungsinstanz wie der Server ist. Wenn der Parameter 1 ist, ist der Client dieselbe Instanz. Wenn der Parameter 0 ist, ist der Client eine andere Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Server sollte ein Datenhandl zurückgeben, das ein Array von [**HSZPAIR-Strukturen**](/windows/win32/api/ddeml/ns-ddeml-hszpair) identifiziert. Das Array sollte eine Struktur für jedes Dienstnamen- und Themennamenpaar enthalten, das dem vom Client angeforderten Dienstnamen- und Themennamenpaar entspricht. Das Array muss durch  ein NULL-Zeichenfolgenhand handle beendet werden. Das System sendet die [**XTYP \_ CONNECT \_ CONFIRM-Transaktion**](xtyp-connect-confirm.md) an den Server, um jede Konversation zu bestätigen und die Konversationshandles an den Server zu übergeben. Der Server erhält diese Bestätigungen nicht, wenn er das **CBF \_ SKIP CONNECT \_ \_ CONFIRMS-Flag** in der [**DdeInitialize-Funktion angegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) hat.

Der Server sollte NULL **zurückgeben,** um die **XTYP \_ WILDCONNECT-Transaktion** abzulehnen.

## <a name="remarks"></a>Hinweise

Diese Transaktion wird gefiltert, wenn die Serveranwendung das **CBF \_ FAIL \_ CONNECTIONS-Flag** in der [**DdeInitialize-Funktion angegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) hat.

Ein Server kann diesen Transaktionstyp nicht blockieren. Der CBR \_ BLOCK-Rückgabecode wird ignoriert.

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

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

