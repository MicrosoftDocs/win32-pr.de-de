---
description: Die ConfigureCardNameSearch-Methode gibt die Kartennamen an, die bei der Suche nach der Smartcard verwendet werden sollen.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: ISCardLocate::ConfigureCardNameSearch-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e49b7653a434f54bfa706aea0bde63048d6b511e5143ade34f0b4e8225a6042b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014266"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>ISCardLocate::ConfigureCardNameSearch-Methode

\[Die **ConfigureCardNameSearch-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ConfigureCardNameSearch-Methode** gibt die Kartennamen an, die bei der Suche nach der [*Smartcard*](../secgloss/s-gly.md)verwendet werden sollen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCardNames* \[ In\]
</dt> <dd>

Ein Zeiger auf ein sicheres Automation-Array von Kartennamen im BSTR-Format.

</dd> <dt>

*pGroupNames* \[ In\]
</dt> <dd>

Ein Zeiger auf ein sicheres Automation-Array von Namen von Karten-/Lesergruppen im BSTR-Formular, das der Suche hinzugefügt werden soll.

</dd> <dt>

*bstrTitle* \[ In\]
</dt> <dd>

Der Titel des Dialogfelds für das allgemeine Suchsteuerelement.

</dd> <dt>

*lFlags* \[ In\]
</dt> <dd>

Gibt an, wann [*die Benutzeroberfläche*](../secgloss/u-gly.md) angezeigt wird.



| Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**SC \_ DLG \_ MINIMAL \_ UI**</dt> </dl> | Zeigt das Dialogfeld nur an, wenn sich die karte, die von der aufrufenden Anwendung gesucht wird, nicht befindet und für die Verwendung in einem Reader verfügbar ist. Dadurch kann die Karte gefunden, verbunden (entweder über einen internen Dialogfeldmechanismus oder mithilfe der Benutzerrückruffunktionen) und an die aufrufende Anwendung zurückgegeben werden.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ NO \_ UI**</dt> </dl>                | Bewirkt unabhängig vom Suchergebnis keine Anzeige der Benutzeroberfläche.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**SC \_ DLG \_ FORCE \_ UI**</dt> </dl>       | Bewirkt, dass die Benutzeroberfläche unabhängig vom Suchergebnis angezeigt wird.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                                         |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde in *pCardNames* oder *pGroupNames* übergeben.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                             |



 

## <a name="remarks"></a>Hinweise

Um die [*Smartcard*](../secgloss/s-gly.md)zu suchen, rufen [**Sie FindCard**](iscardlocate-findcard.md)auf.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardLocate.**](iscardlocate.md)

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate ist als 1461AACD-6810-11D0-918F-00AA00C18068 definiert.<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FindCard**](iscardlocate-findcard.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
