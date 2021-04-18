---
title: XTYP_WILDCONNECT Transaktion (Ddeml. h)
description: Ermöglicht einem Client, eine Konversation für alle Dienstnamen-und Themen Namen Paare des Servers einzurichten, die dem angegebenen Dienstnamen und Themen Namen entsprechen.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT Transaktionsdaten Austausch
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
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340788"
---
# <a name="xtyp_wildconnect-transaction"></a>XYP- \_ wildconnect-Transaktion

Ermöglicht einem Client, eine Konversation für alle Dienstnamen-und Themen Namen Paare des Servers einzurichten, die dem angegebenen Dienstnamen und Themen Namen entsprechen. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion [*(ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client einen **null** -Dienstnamen, einen **null** -Themen Namen oder beides in einem Aufrufs der [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -oder [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) -Funktion angibt.


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

Ein Handle für den Themen Namen. Wenn dieser Parameter **null** ist, fordert der Client eine Konversation für alle Themen Namen an, die der Server unterstützt.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Dienstnamen. Wenn dieser Parameter **null** ist, fordert der Client eine Konversation für alle Dienstnamen an, die der Server unterstützt.

</dd> <dt>

*hdata* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Ein Zeiger auf eine [**konvcontext**](/windows/win32/api/ddeml/ns-ddeml-convcontext) -Struktur, die Kontextinformationen für die Konversation enthält. Wenn der Client keine Ddeml-Anwendung ist, wird dieser Parameter auf 0 festgelegt.

</dd> <dt>

*dwData2* 
</dt> <dd>

Gibt an, ob es sich bei dem Client um dieselbe Anwendungs Instanz wie der Server handelt. Wenn der-Parameter 1 ist, ist der Client dieselbe Instanz. Wenn der-Parameter 0 ist, ist der Client eine andere-Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Server sollte ein Daten Handle zurückgeben, das ein Array von [**hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair) -Strukturen identifiziert. Das Array sollte eine Struktur für jedes Paar aus Dienst Name und Themenname enthalten, das mit dem vom Client angeforderten Dienstnamen und Topic-Name-Paar übereinstimmt. Das Array muss von einem **null** -Zeichen folgen handle beendet werden. Das System sendet die [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion an den Server, um die einzelnen Konversation zu bestätigen und die Konversations Handles an den Server zu übergeben. Der Server empfängt diese Bestätigungen nicht, wenn er das Flag **CBF \_ Skip \_ Connect \_ Bestätigungen** in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.

Der Server sollte **null** zurückgeben, um die **XYP \_ wildconnect** -Transaktion abzulehnen.

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_ Connections** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.

Ein Server kann diesen Transaktionstyp nicht blockieren. der Rückgabecode des CBR- \_ Blocks wird ignoriert.

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

[**Hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

