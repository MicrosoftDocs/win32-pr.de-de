---
title: XTYP_UNREGISTER Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Rückruffunktion (ddecallback) empfängt die \_ xttunregister-Transaktion, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion "DDENameService" verwendet, um die Registrierung eines Dienst namens aufzuheben, oder wenn eine nicht-Ddeml-Anwendung, die das System Thema unterstützt, beendet wird.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- XTYP_UNREGISTER Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742872"
---
# <a name="xtyp_unregister-transaction"></a>\_Xttunregister Transaktion

Eine dynamischer Datenaustausch (DDE)-Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **\_ xttunregister** -Transaktion, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " verwendet, um die Registrierung eines Dienst namens aufzuheben, oder wenn eine nicht-Ddeml-Anwendung, die das System Thema unterstützt, beendet wird.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Nicht verwendet.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Basis Dienstnamen, bei dem die Registrierung aufgehoben wird.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den instanzspezifischen Dienstnamen, bei dem die Registrierung aufgehoben wird.

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

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn die Anwendung das Flag " **CBF \_ Skip \_ Registrierungen** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.

Eine-Anwendung kann diesen Transaktionstyp nicht blockieren; der Rückgabecode des CBR- \_ Blocks wird ignoriert.

Eine Anwendung sollte den *hsz1* -Parameter verwenden, um den Dienstnamen aus der Liste der für den Benutzer verfügbaren Server zu entfernen. Eine Anwendung sollte den *hsz2* -Parameter verwenden, um zu ermitteln, welche Anwendungs Instanz beendet wurde.

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

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

