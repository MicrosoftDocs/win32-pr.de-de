---
description: Die AppendRecord-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der entweder einen Datensatz an das Ende einer linear strukturierten elementaren Datei (EF) anfügt oder datensatznummer 1 in eine zyklische, strukturierte elementare Datei schreibt.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: ISCardISO7816::AppendRecord-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: de2b6ac4bfded1612713272111f3ef21f21cf4b7b8ac9cedae769531fee26c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923061"
---
# <a name="iscardiso7816appendrecord-method"></a>ISCardISO7816::AppendRecord-Methode

\[Die **AppendRecord-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **AppendRecord-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der entweder einen Datensatz an das Ende einer linear strukturierten elementaren Datei (EF) anfügt oder datensatznummer 1 in eine zyklische, strukturierte elementare Datei schreibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byRefCtrl* \[ In\]
</dt> <dd>

Identifiziert die anzufügende elementare Datei.



| Wert                                                                                                                                                                                | Bedeutung                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**Aktuelles EF**</dt> </dl>     | Bitposition: 00000000<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Kurze EF-ID**</dt> </dl> | Bitposition: xxxxx000<br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Reserviert**</dt> </dl>             | Bitposition: xxxxxxxx<br/> |



 

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Ein Zeiger auf die Daten, die an die Datei angefügt werden sollen.



| Wert                                                                                                                                                | Bedeutung                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <dt>**Tn**</dt> </dl>     | 1 Byte<br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <dt>**Ln**</dt> </dl> | 1 oder 3 Bytes<br/> |
| <span id="data"></span><span id="DATA"></span><dl> <dt>**Daten**</dt> </dl>                    | Ln Bytes<br/>     |



 

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem APDU-Befehl gefüllt, der von diesem Vorgang erstellt wurde. Wenn *ppCmd* auf **NULL** festgelegt wurde, wird intern ein [**ISCardCmd-Smartcardobjekt**](iscardcmd.md) erstellt und mithilfe des *ppCmd-Zeigers* zurückgegeben. [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde übergeben.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheitsattributen des elementaren Dateilesediensts entspricht.

Wenn zum Zeitpunkt der Ausgabe dieses Befehls eine andere elementare Datei ausgewählt wird, kann sie ohne Identifikation der aktuell ausgewählten Datei verarbeitet werden.

Elementare Dateien ohne Datensatzstruktur können nicht gelesen werden. Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Datensatzstruktur angewendet wird.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardISO7816**](iscardiso7816.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53B6AA68-3F56-11D0-916B-00AA00C18068 definiert.<br/>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
