---
title: XTYP_CONNECT Transaktion (Ddeml. h)
description: Ein Client verwendet die xtipp \_ Connect-Transaktion zum Einrichten einer Konversation.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT Transaktionsdaten Austausch
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
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104078"
---
# <a name="xtyp_connect-transaction"></a>XYP \_ Connect-Transaktion

Ein Client verwendet die **xtipp \_ Connect** -Transaktion zum Einrichten einer Konversation. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client einen Dienstnamen angibt, der vom Server unterstützt wird (und einen Themen Namen, der nicht **null** ist), wenn die [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -Funktion aufgerufen wird.


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

Ein Handle für den Themen Namen.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Dienstnamen.

</dd> <dt>

*hdata* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Ein Zeiger auf eine [**konvcontext**](/windows/win32/api/ddeml/ns-ddeml-convcontext) -Struktur, die Kontextinformationen für die Konversation enthält. Wenn der Client keine Ddeml-Anwendung ist, ist dieser Parameter 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Gibt an, ob es sich bei dem Client um dieselbe Anwendungs Instanz wie der Server handelt. Wenn der-Parameter 1 ist, ist der Client dieselbe Instanz. Wenn der-Parameter 0 ist, ist der Client eine andere-Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Server Rückruffunktion sollte " **true** " zurückgeben, damit der Client eine Konversation für das angegebene Paar aus Dienst Name und Themenname einrichten kann. andernfalls sollte die Funktion " **false** " zurückgeben, um die Konversation abzulehnen. Wenn die Rückruffunktion " **true** " zurückgibt und eine Konversation erfolgreich eingerichtet wurde, übergibt das System das Konversations Handle an den Server, indem eine [**xtipp Connect-Transaktion zum \_ \_ bestätigen**](xtyp-connect-confirm.md) an die Rückruffunktion des Servers ausgegeben wird (es sei denn, der Server hat das Flag " **CBF \_ Skip \_ Connect \_ bestätigt** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_ Connections** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.

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

[**Konvcontext**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DDE Connect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

