---
description: Die findcard-Methode sucht nach der Smartcard und öffnet eine gültige Verbindung.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'Iscardlocate:: findcard-Methode (scardmgr. h)'
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
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360517"
---
# <a name="iscardlocatefindcard-method"></a>Iscardlocate:: findcard-Methode

\[Die **findcard** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **findcard** -Methode sucht nach der [*Smartcard*](../secgloss/s-gly.md) und öffnet eine gültige Verbindung.

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

*Share Mode* \[ in\]
</dt> <dd>

Der Modus, in dem die Smartcard gemeinsam genutzt oder nicht freigegeben werden soll, wenn eine Verbindung damit geöffnet ist.



| Wert                                                                                                                                            | Bedeutung                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Ausschließliche**</dt> </dl> | Diese Verbindung wird von keiner anderen Person mit der Smartcard verwendet.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**Genu**</dt> </dl>          | Diese Verbindung kann von anderen Anwendungen verwendet werden.<br/>        |



 

</dd> <dt>

*Protokolle* \[ in\]
</dt> <dd>

Protokoll, das beim Herstellen einer Verbindung mit der Karte verwendet werden soll.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[ in\]
</dt> <dd>

Gibt an, wann die [*Benutzeroberfläche*](../secgloss/u-gly.md) angezeigt wird:



| Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**SC \_ DLG \_ minimale \_ Benutzeroberfläche**</dt> </dl> | Zeigt das Dialogfeld nur an, wenn die Karte, die von der aufrufenden Anwendung gesucht wird, nicht gefunden wurde und für die Verwendung in einem Reader verfügbar ist. Dadurch kann die Karte gefunden und verbunden werden (entweder über einen internen Dialogfeld Mechanismus oder mithilfe der Benutzer Rückruf Funktionen) und an die aufrufende Anwendung zurückgegeben werden.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ keine \_ Benutzeroberfläche**</dt> </dl>                | Bewirkt, dass unabhängig vom Suchergebnis keine Anzeige auf der Benutzeroberfläche angezeigt wird.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**SC \_ DLG \_ Force \_ UI**</dt> </dl>       | Bewirkt, dass die Benutzeroberfläche unabhängig vom Suchergebnis angezeigt wird.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppcardinfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine Datenstruktur, die Informationen über die geöffnete [*Smartcard*](../secgloss/s-gly.md)enthält oder zurückgibt, wenn erfolgreich. Ist **null** , wenn der Vorgang fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                        |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppcardinfo* übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Um die Suchkriterien für die Suche festzulegen, geben Sie " [**konfigurierter Name**](iscardlocate-configurecardnamesearch.md) der Smartcard" an.

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

[**Konfigurieren von "Konfigurations namesearch"**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**Iscardsuche**](iscardlocate.md)
</dt> </dl>

 

 
