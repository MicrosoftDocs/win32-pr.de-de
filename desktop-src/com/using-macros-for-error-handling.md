---
title: Verwenden von Makros für die Fehlerbehandlung
description: COM definiert eine Reihe von Makros, die die Arbeit mit HRESULT-Werten vereinfachen.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f31280ec2076f8ece1fcf15dd6e27629a3016e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480536"
---
# <a name="using-macros-for-error-handling"></a>Verwenden von Makros für die Fehlerbehandlung

COM definiert eine Reihe von Makros, die die Arbeit mit **HRESULT-Werten** vereinfachen.

Die Fehlerbehandlungsmakros werden in der folgenden Tabelle beschrieben.




| Makro | Beschreibung | 
|-------|-------------|
| <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br /> | Gibt ein <strong>HRESULT zurück,</strong> wenn das Schweregradbit, der Einrichtungscode und der Fehlercode angegeben werden, aus dem <strong>das HRESULT besteht.</strong><br /><blockquote>[!Note]<br />Das <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> für S_OK überprüfung führt zu Leistungssentspricht. Sie sollten nicht routinemäßig <strong>die</strong> MAKE_HRESULT für erfolgreiche Ergebnisse verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br /> | Gibt einen <strong>SCODE zurück,</strong> wenn das Schweregradbit, der Einrichtungscode und der Fehlercode angegeben werden, aus dem <strong>der SCODE besteht.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br /> | Extrahiert den Fehlercodeteil von <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br /> | Extrahiert den Einrichtungscode von <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br /> | Extrahiert das Schweregradbit von <strong>HRESULT.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br /> | Extrahiert den Fehlercodeteil von <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br /> | Extrahiert den Einrichtungscode von <strong>SCODE.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br /> | Extrahiert das Schweregradfeld von <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>GELUNGEN</strong></a><br /> | Testet das Schweregradbit von <strong>SCODE</strong> oder <strong>HRESULT.</strong> gibt <strong>TRUE zurück,</strong> wenn der Schweregrad 0 (null) ist, und <strong>FALSE,</strong> wenn er eins ist.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FEHLGESCHLAGEN</strong></a><br /> | Testet das Schweregradbit von <strong>SCODE</strong> oder <strong>HRESULT.</strong> gibt <strong>TRUE zurück,</strong> wenn der Schweregrad 1 ist, und <strong>FALSE,</strong> wenn er 0 (null) ist.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br /> | Stellt einen generischen Test auf Fehler für einen beliebigen Statuswert zur Seite. <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br /> | Karten einen <a href="/windows/desktop/Debug/system-error-codes">Systemfehlercode in</a> einen <strong>HRESULT-Wert.</strong> <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br /> | Karten einen NT-Statuswert in einen <strong>HRESULT-Wert.</strong><br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in COM](error-handling-in-com.md)
</dt> </dl>

 

