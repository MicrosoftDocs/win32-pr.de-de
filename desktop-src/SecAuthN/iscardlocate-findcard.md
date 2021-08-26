---
description: Die FindCard-Methode sucht nach der Smartcard und öffnet eine gültige Verbindung mit ihr.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: ISCardLocate::FindCard-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a0db06f9dcafd211f628eb7cd0be9ed2f800b6f1b980d8e2320cd82b2849d386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014240"
---
# <a name="iscardlocatefindcard-method"></a>ISCardLocate::FindCard-Methode

\[Die **FindCard-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **FindCard-Methode** sucht nach der [*Smartcard und*](../secgloss/s-gly.md) öffnet eine gültige Verbindung mit ihr.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShareMode* \[ In\]
</dt> <dd>

Modus, in dem die Smartcard beim Öffnen einer Verbindung gemeinsam verwendet oder nicht gemeinsam verwendet werden soll.



| Wert                                                                                                                                            | Bedeutung                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Exklusive**</dt> </dl> | Diese Verbindung mit der Smartcard wird von niemand anderem verwendet.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**geteilt**</dt> </dl>          | Andere Anwendungen können diese Verbindung verwenden.<br/>        |



 

</dd> <dt>

*Protokolle* \[ In\]
</dt> <dd>

Protokoll, das beim Herstellen einer Verbindung mit der Karte verwendet werden soll.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[ In\]
</dt> <dd>

Gibt an, [*wann die Benutzeroberfläche*](../secgloss/u-gly.md) angezeigt wird:



| Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**SC \_ DLG \_ MINIMAL \_ UI**</dt> </dl> | Zeigt das Dialogfeld nur an, wenn die von der aufrufenden Anwendung gesuchte Karte nicht gefunden wurde und für die Verwendung in einem Reader verfügbar ist. Dadurch kann die Karte gefunden, verbunden (entweder über einen internen Dialogfeldmechanismus oder mithilfe der Benutzerrückruffunktionen) und an die aufrufende Anwendung zurückgegeben werden.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ NO \_ UI**</dt> </dl>                | Bewirkt, dass unabhängig vom Suchergebnis keine Benutzeroberfläche angezeigt wird.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**SC \_ DLG \_ FORCE \_ UI**</dt> </dl>       | Bewirkt, dass die Benutzeroberfläche unabhängig vom Suchergebnis angezeigt wird.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[ out\]
</dt> <dd>

Zeiger auf einen Zeiger auf eine Datenstruktur, die Informationen über die geöffnete [*Smartcard*](../secgloss/s-gly.md)enthält oder zurückgibt, sofern erfolgreich. Ist **NULL,** wenn der Vorgang fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                        |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppCardInfo übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Um die Suchkriterien für die Suche festzulegen, rufen [**Sie ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) auf, um die Kartennamen einer Smartcard anzugeben.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardLocate**](iscardlocate.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate ist als 1461AACD-6810-11D0-918F-00AA00C18068 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
