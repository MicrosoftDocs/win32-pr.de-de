---
description: Die Read Record-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der entweder den Inhalt der angegebenen Datensätze oder den Anfangsteil eines Datensatzes einer elementaren Datei liest.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816:: Read Record-Methode (scardssp. h)'
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
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042224"
---
# <a name="iscardiso7816readrecord-method"></a>ISCardISO7816:: Read Record-Methode

\[Die Methode "read **Record** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Read **Record** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der entweder den Inhalt der angegebenen Datensätze oder den Anfangsteil eines Datensatzes einer elementaren Datei liest.

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

*byrecordid* \[ in\]
</dt> <dd>

Datensatznummer oder ID des ersten zu lesenden Datensatzes (00 gibt den aktuellen Datensatz an).

</dd> <dt>

*ByRef STRG* \[ in\]
</dt> <dd>

Codieren des Verweis Steuer Elements.



| Wert                                                                                                                                                                                | Bedeutung                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**Aktuelles EF**</dt> </dl>     | Bitposition: 00000---<br/> Aktuell ausgewähltes EF.<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Kurze EF-ID**</dt> </dl> | Bitposition: XXXXX---<br/> Kurzer EF-Bezeichner.<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Bitposition: 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**Aufnahme \#**</dt> </dl>            | Bitposition:-----1xx<br/> Verwendung der Datensatznummer in P1.<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**Datensatz lesen**</dt> </dl> | Bitposition:-----100<br/> Lesen Sie den Datensatz P1.<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**Bis zum letzten**</dt> </dl>     | Bitposition:-----101<br/> Lesen Sie alle Datensätze von P1 bis zum letzten. <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**Bis zu P1**</dt> </dl>             | Bitposition:-----110<br/> Lesen Sie alle Datensätze von der letzten bis zu P1. <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Bitposition:-----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**Datensatz-ID**</dt> </dl>         | Bitposition:-----0xx<br/> Verwendung der Datensatznummer in P1.<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**Zuerst auftreten**</dt> </dl> | Bitposition:-----000<br/> Lesen Sie das erste Vorkommen. <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**Letztes vorkommen**</dt> </dl>     | Bitposition:-----001<br/> Letztes vorkommen lesen. <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**Nächstes Vorkommen**</dt> </dl>     | Bitposition:-----010<br/> Nächste Vorkommen lesen. <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**Vorherige**</dt> </dl>             | Bitposition:-----011<br/> Vorheriges Vorkommen lesen. <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Geheimen**</dt> </dl>                     | Bitposition:---XXXXX<br/>                                                      |



 

</dd> <dt>

*lbytestoread* \[ in\]
</dt> <dd>

Anzahl der Bytes, die aus dem transparenten EF gelesen werden sollen.

Wenn das Feld Le nur Nullen enthält, sollte der Befehl je nach b3b2b1 von P2 und innerhalb des Limits von 256 für kurze Länge oder 65536 für erweiterte Länge entweder den einzelnen angeforderten Datensatz oder die angeforderte Sequenz von Datensätzen vollständig lesen.

</dd> <dt>

*ppcmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.

Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt. Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu lesenden elementaren Datei entspricht.

Wenn derzeit eine andere elementare Datei zum Zeitpunkt der Ausgabe dieses Befehls ausgewählt ist, kann Sie ohne Identifikation der aktuell ausgewählten Datei verarbeitet werden.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.

Elementare Dateien ohne Daten Satzstruktur können nicht gelesen werden. Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Daten Satzstruktur angewendet wird.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Appenddatensatz**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**Beschreibecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
