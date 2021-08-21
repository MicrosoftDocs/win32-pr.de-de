---
title: XTYP_MONITOR Transaktion (Ddeml.h)
description: Die DDE-Rückruffunktion (DdeCallback) eines dynamische Daten Exchange-Debuggers (DDE) empfängt immer dann die XTYP MONITOR-Transaktion, wenn ein DDE-Ereignis im \_ System auftritt.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR der Exchange
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
ms.openlocfilehash: 11a86235c2964bbd09d51ce3adc2e602e23fed09597df14721e92e76c0cd8109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047258"
---
# <a name="xtyp_monitor-transaction"></a>XTYP \_ MONITOR-Transaktion

Die DDE-Rückruffunktion [*(DdeCallback)*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)eines DDE-Debuggers (dynamische Daten Exchange) empfängt immer dann die **XTYP \_ MONITOR-Transaktion,** wenn ein DDE-Ereignis im System auftritt. Um diese Transaktion zu empfangen, muss eine Anwendung den **APPCLASS \_ MONITOR-Wert** angeben, wenn sie die [**DdeInitialize-Funktion aufruft.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)


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

Wird nicht verwendet.

</dd> <dt>

*hsz2* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*hdata* 
</dt> <dd>

Ein Handle für ein DDE-Objekt, das Informationen zum DDE-Ereignis enthält. Die Anwendung sollte die [**DdeAccessData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) verwenden, um einen Zeiger auf das Objekt zu erhalten.

</dd> <dt>

*dwData1* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Das DDE-Ereignis. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ RÜCKRUFE**</dt> <dt>0x08000000</dt> </dl> | Das System hat eine Transaktion an eine DDE-Rückruffunktion gesendet. Das DDE-Objekt enthält eine [**MONCBSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) die Informationen zur Transaktion enthält.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_ CONV-0x40000000**</dt> <dt></dt> </dl>                | Eine DDE-Konversation wurde eingerichtet oder beendet. Das DDE-Objekt enthält eine [**MONCONVSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) die Informationen zur Konversation enthält.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ FEHLER**</dt> <dt>0x10000000</dt> </dl>          | DDE-Fehler. Das DDE-Objekt enthält eine [**MONERRSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) die Informationen zum Fehler enthält.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ HSZ \_ INFO**</dt> <dt>0x01000000</dt> </dl>   | Eine DDE-Anwendung hat die Nutzungsanzahl eines Zeichenfolgenhandpunkts erstellt, freigibt oder erhöht, oder ein Zeichenfolgenhand handle wurde als Ergebnis eines Aufrufs der [**DdeUninitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) frei. Das DDE-Objekt enthält eine [**MONHSZSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) die Informationen zum Zeichenfolgenhandl enthält.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_ LINKS**</dt> <dt>0x20000000</dt> </dl>             | Eine DDE-Anwendung hat eine Advise-Schleife gestartet oder beendet. Das DDE-Objekt enthält eine [**MONLINKSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) die Informationen zur Advise-Schleife enthält.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_ POSTMSGS-0x04000000**</dt> <dt></dt> </dl>    | Das System oder eine Anwendung hat eine DDE-Nachricht gesendet. Das DDE-Objekt enthält eine [**MONMSGSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) die Informationen über die Nachricht enthält.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_ SENDMSGS-0x02000000**</dt> <dt></dt> </dl>    | Das System oder eine Anwendung hat eine DDE-Nachricht gesendet. Das DDE-Objekt enthält eine [**MONMSGSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) die Informationen über die Nachricht enthält.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Rückruffunktion diese Transaktion verarbeitet, sollte sie 0 zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

