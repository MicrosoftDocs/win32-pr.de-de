---
description: Die ReadRecord-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der entweder den Inhalt der angegebenen Datensätze oder den Anfang eines Datensatzes einer elementaren Datei liest.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: ISCardISO7816::ReadRecord-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 16edb529cb5a1cf6e2badd19c3ac37f1e7ec69649fb854f98ff0b515c573f874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141083"
---
# <a name="iscardiso7816readrecord-method"></a>ISCardISO7816::ReadRecord-Methode

\[Die **ReadRecord-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ReadRecord-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der entweder den Inhalt der angegebenen Datensätze oder den Anfang eines Datensatzes einer elementaren Datei liest.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byRecordId* \[ In\]
</dt> <dd>

Datensatznummer oder ID des ersten zu lesenden Datensatzes (00 gibt den aktuellen Datensatz an).

</dd> <dt>

*byRefCtrl* \[ In\]
</dt> <dd>

Codierung des Verweissteuerelements.



| Wert                                                                                                                                                                                | Bedeutung                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**Aktuelles EF**</dt> </dl>     | Bitposition: 00000---<br/> Derzeit ausgewählte EF.<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Kurze EF-ID**</dt> </dl> | Bitposition: xxxxx---<br/> Kurzer EF-Bezeichner.<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                       | Bitposition: 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**Aufzeichnung \#**</dt> </dl>            | Bitposition: -----1xx<br/> Verwendung der Datensatznummer in P1.<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**Datensatz lesen**</dt> </dl> | Bitposition: -----100<br/> Liest den Datensatz P1.<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**Bis zuletzt**</dt> </dl>     | Bitposition: -----101<br/> Liest alle Datensätze von P1 bis zum letzten. <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**Bis zu P1**</dt> </dl>             | Bitposition: -----110<br/> Liest alle Datensätze vom letzten bis P1. <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                       | Bitposition: -----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**Datensatz-ID**</dt> </dl>         | Bitposition: -----0xx<br/> Verwendung der Datensatznummer in P1.<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**First Occur**</dt> </dl> | Bitposition: -----000<br/> Lesen des ersten Vorkommens. <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**Letztes Auftreten**</dt> </dl>     | Bitposition: -----001<br/> Letztes Vorkommen lesen. <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**Nächstes Auftreten**</dt> </dl>     | Bitposition: -----010<br/> Nächstes Vorkommen lesen. <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**Vorherige**</dt> </dl>             | Bitposition: -----011<br/> Vorheriges Vorkommen lesen. <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**`Secret`**</dt> </dl>                     | Bitposition: ---xxxxx<br/>                                                      |



 

</dd> <dt>

*lBytesToRead* \[ In\]
</dt> <dd>

Anzahl der Bytes, die aus dem transparenten EF gelesen werden sollen.

Wenn das Feld Le nur Nullen enthält, sollte der Befehl abhängig von b3b2b1 von P2 und innerhalb des Grenzwerts von 256 für kurze Länge oder 65536 für längere Länge den einzelnen angeforderten Datensatz oder die angeforderte Sequenz von Datensätzen vollständig lesen.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem APDU-Befehl gefüllt, der von diesem Vorgang erstellt wurde. Wenn *ppCmd* auf **NULL** festgelegt wurde, wird intern ein [**ISCardCmd-Smartcardobjekt**](iscardcmd.md) erstellt und über den *ppCmd-Zeiger* zurückgegeben. [](../secgloss/s-gly.md)

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

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) die Sicherheitsattribute der zu lesenden elementaren Datei erfüllt.

Wenn zum Zeitpunkt der Ausgabe dieses Befehls derzeit eine andere elementare Datei ausgewählt ist, kann sie ohne Identifikation der aktuell ausgewählten Datei verarbeitet werden.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.

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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
