---
title: XTYP_MONITOR Transaktion (Ddeml. h)
description: Die DDE-Rückruffunktion (ddecallback) eines dynamischer Datenaustausch (DDE) empfängt die xD- \_ Monitor Transaktion, wenn ein DDE-Ereignis im System auftritt.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391800"
---
# <a name="xtyp_monitor-transaction"></a>XYP- \_ Monitor Transaktion

Die DDE-Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) eines dynamischer Datenaustausch (DDE) empfängt die **xD- \_ Monitor** Transaktion, wenn ein DDE-Ereignis im System auftritt. Um diese Transaktion zu erhalten, muss eine Anwendung den **appclass- \_ Monitor** Wert angeben, wenn Sie die [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion aufruft.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Nicht verwendet.

</dd> <dt>

*hsz2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*hdata* 
</dt> <dd>

Ein Handle für ein DDE-Objekt, das Informationen über das DDE-Ereignis enthält. Die Anwendung sollte die [**DDEBUG Data**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) -Funktion verwenden, um einen Zeiger auf das Objekt zu erhalten.

</dd> <dt>

*dwData1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Das DDE-Ereignis. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ Rückrufe**</dt> <dt>0x08000000</dt> </dl> | Das System hat eine Transaktion an eine DDE-Rückruffunktion gesendet. Das DDE-Objekt enthält eine [**moncbstruct**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) -Struktur, die Informationen über die Transaktion bereitstellt.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_**</dt>Verbindung mit " <dt>0x40000000</dt> " </dl>                | Eine DDE-Konversation wurde eingerichtet oder beendet. Das DDE-Objekt enthält eine [**monkonvstruct**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) -Struktur, die Informationen über die Konversation bereitstellt.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ Fehler**</dt> <dt>0x10000000</dt> </dl>          | DDE-Fehler. Das DDE-Objekt enthält eine [**monerrstruct**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) -Struktur, die Informationen über den Fehler bereitstellt.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ Hsz- \_ Info**</dt> <dt>0x01000000</dt> </dl>   | Eine DDE-Anwendung, die den Verwendungs Zähler eines Zeichen folgen Handles erstellt, freigegeben oder inkrementiert hat, oder ein Zeichen folgen Handle wurde als Ergebnis eines Aufrufes der [**DDE Uninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) -Funktion freigegeben. Das DDE-Objekt enthält eine [**monhszstruct**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) -Struktur, die Informationen über das Zeichen folgen handle bereitstellt.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_ Links**</dt> <dt>0x20000000</dt> </dl>             | Eine DDE-Anwendung hat eine Empfehlung-Schleife gestartet oder angehalten. Das DDE-Objekt enthält eine [**monlinkstruct**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) -Struktur, die Informationen über die Empfehlung-Schleife bereitstellt.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_ Postmsgs**</dt> <dt>0x04000000</dt> </dl>    | Das System oder eine Anwendung hat eine DDE-Nachricht gepostet. Das DDE-Objekt enthält eine [**monmsgstruct**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) -Struktur, die Informationen über die Meldung bereitstellt.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_ Sendmsgs**</dt> <dt>0x02000000</dt> </dl>    | Das System oder eine Anwendung hat eine DDE-Nachricht gesendet. Das DDE-Objekt enthält eine [**monmsgstruct**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) -Struktur, die Informationen über die Meldung bereitstellt.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Rückruffunktion diese Transaktion verarbeitet, sollte Sie 0 (null) zurückgeben.

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

[**DDE Access Data**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DDE-Initialisierung**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**Moncbstruct**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**Mon-vstruct**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**Monerrstruct**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**Monhszstruct**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**Monlinkstruct**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**Monmsgstruct**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

