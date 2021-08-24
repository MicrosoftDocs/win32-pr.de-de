---
title: XTYP_CONNECT Transaktion (Ddeml.h)
description: Ein Client verwendet die XTYP \_ CONNECT-Transaktion, um eine Konversation herzustellen.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT der Exchange
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1ff7a7a79d8b61deef6b5f19b829e5c8dd8f4603c5f60c3b47d0a84b0603736
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793420"
---
# <a name="xtyp_connect-transaction"></a>XTYP \_ CONNECT-Transaktion

Ein Client verwendet die **XTYP \_ CONNECT-Transaktion,** um eine Konversation herzustellen. Eine dynamische Daten Exchange-Serverrückruffunktion [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt diese Transaktion, wenn ein Client einen Dienstnamen angibt, den der Server unterstützt (und einen Themennamen, der nicht **NULL** ist) in einem Aufruf der [**DdeConnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) angibt.


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
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

Ein Handle für den Themennamen.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Dienstnamen.

</dd> <dt>

*hdata* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Ein Zeiger auf eine [**CONVCONTEXT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-convcontext) die Kontextinformationen für die Konversation enthält. Wenn der Client keine DDEML-Anwendung ist, ist dieser Parameter 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Gibt an, ob der Client die gleiche Anwendungsinstanz wie der Server ist. Wenn der Parameter 1 ist, ist der Client dieselbe Instanz. Wenn der Parameter 0 ist, ist der Client eine andere Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Serverrückruffunktion sollte **TRUE** zurückgeben, damit der Client eine Konversation mit dem angegebenen Dienstnamen- und Themennamenpaar herstellen kann, oder die Funktion sollte **FALSE** zurückgeben, um die Konversation zu verweigern. Wenn die Rückruffunktion **TRUE** zurückgibt und eine Konversation erfolgreich hergestellt wurde, übergibt das System das Konversationshand handle an den Server, indem es eine [**XTYP \_ CONNECT \_ CONFIRM-Transaktion**](xtyp-connect-confirm.md) an die Rückruffunktion des Servers ausgibt (es sei denn, der Server hat das **CBF SKIP CONNECT \_ \_ \_ CONFIRMS-Flag** in der [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angegeben).

## <a name="remarks"></a>Hinweise

Diese Transaktion wird gefiltert, wenn die Serveranwendung das **CBF \_ FAIL \_ CONNECTIONS-Flag** in der [**DdeInitialize-Funktion angegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) hat.

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

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

