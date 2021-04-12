---
description: Die Methode "konfigurrecardnamesearch" gibt die Kartennamen an, die bei der Suche nach der Smartcard verwendet werden sollen.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'Iscardlocate:: konfiguriert recardnamesearch-Methode (scardmgr. h)'
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
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216534"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>Iscardlocate:: konfiguriert recardnamesearch-Methode

\[Die Methode " **konfigurrecardnamesearch** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Methode " **konfigurrecardnamesearch** " gibt die Kartennamen an, die bei der Suche nach der [*Smartcard*](../secgloss/s-gly.md)verwendet werden sollen.

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

*pcardnames* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Automatisierungs sicheres Array von Kartennamen in BSTR-Form.

</dd> <dt>

*pgroupnames* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Automation-sicheres Array mit Namen von Karten-/Lesegruppen in BSTR-Form, die der Suche hinzugefügt werden sollen.

</dd> <dt>

*bstrintitle* \[ in\]
</dt> <dd>

Dialog Feld Titel für das allgemeine Steuerelement für die Suche.

</dd> <dt>

*lFlags* \[ in\]
</dt> <dd>

Gibt an, wann die [*Benutzeroberfläche*](../secgloss/u-gly.md) angezeigt wird.



| Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**SC \_ DLG \_ minimale \_ Benutzeroberfläche**</dt> </dl> | Zeigt das Dialogfeld nur an, wenn die Karte, die von der aufrufenden Anwendung gesucht wird, nicht gefunden wurde und für die Verwendung in einem Reader verfügbar ist. Dadurch kann die Karte gefunden und verbunden werden (entweder über einen internen Dialogfeld Mechanismus oder mithilfe der Benutzer Rückruf Funktionen) und an die aufrufende Anwendung zurückgegeben werden.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ keine \_ Benutzeroberfläche**</dt> </dl>                | Bewirkt, dass unabhängig vom Suchergebnis keine Anzeige auf der Benutzeroberfläche angezeigt wird.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**SC \_ DLG \_ Force \_ UI**</dt> </dl>       | Bewirkt, dass die Benutzeroberfläche unabhängig vom Suchergebnis angezeigt wird.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>                          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                                         |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in " *pcardnames* " oder " *pgroupnames*" übergeben.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

Um die [*Smartcard*](../secgloss/s-gly.md)zu suchen, wenden Sie [**findcard**](iscardlocate-findcard.md)an.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardlocate**](iscardlocate.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardmgr. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardlocate ist als 1461aacd-6810-11D0-918f -00aa00c18068 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Findcard**](iscardlocate-findcard.md)
</dt> <dt>

[**Iscardsuche**](iscardlocate.md)
</dt> </dl>

 

 
