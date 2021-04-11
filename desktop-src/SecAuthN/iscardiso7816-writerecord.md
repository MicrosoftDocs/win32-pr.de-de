---
description: Erstellt einen APDU-Befehl, der einen der aufgelisteten Vorgänge initiiert.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'ISCardISO7816:: beschreiterecord-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128292"
---
# <a name="iscardiso7816writerecord-method"></a>ISCardISO7816:: beschreiterecord-Methode

\[Die Methode " **beschreiterecord** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **beschreiterecord** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der einen der folgenden Vorgänge initiiert:

-   Der einmal Schreibvorgang eines Datensatzes.
-   Das logische **or** der Daten Bytes eines Datensatzes, der bereits in der Karte vorhanden ist, mit den Daten Bytes des Datensatzes, der im Befehl APDU angegeben ist.
-   Das logische und der Daten Bytes eines Datensatzes, die bereits in der Karte vorhanden sind, mit den Daten Bytes des Datensatzes, der im Befehl APDU angegeben ist.

Wenn im Daten Codierungs Byte keine Angabe angegeben ist, gilt das logische OR-Verhalten.

> [!Note]  
> Bei der Verwendung der aktuellen Daten Satz Adressierung legt der Befehl den Datensatz-Zeiger auf den erfolgreich aktualisierten Datensatz fest.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byrecordid* \[ in\]
</dt> <dd>

Datensatz-ID. Dies ist der P1-Wert:

P1 = ' 00 ' gibt den aktuellen Datensatz an.

P1! = ' 00 ' ist die Nummer des angegebenen Datensatzes.

</dd> <dt>

*ByRef STRG* \[ in\]
</dt> <dd>

Codieren des Verweis Steuer Elements P2.



| Wert                                                                                                                                                                                                | Bedeutung                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**Aktuelles EF**</dt> </dl>                     | Bitposition: 00000---<br/> Aktuell ausgewähltes EF.<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Kurze EF-ID**</dt> </dl>                 | Bitposition: XXXXX---<br/> Kurzer EF-Bezeichner.<br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <dt>**Erster Datensatz**</dt> </dl>             | Bitposition:-----000<br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <dt>**Letzter Datensatz**</dt> </dl>                 | Bitposition:-----001<br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <dt>**Nächster Datensatz**</dt> </dl>                 | Bitposition:-----010<br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <dt>**Vorheriger Datensatz**</dt> </dl> | Bitposition:-----011<br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <dt>**Datensatz \# in P1**</dt> </dl>    | Bitposition:-----100<br/>                                   |



 

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Zeiger auf den zu schreibenden Datensatz.

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

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt. Wenn derzeit eine andere elementare Datei zum Zeitpunkt der Ausgabe dieses Befehls ausgewählt ist, kann dieser Befehl ohne Identifikation der aktuell ausgewählten Datei verarbeitet werden.

Wenn der gekapselte Befehl für eine lineare oder zyklische strukturierte elementare Datei gilt, wird er abgebrochen, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht. Wenn Sie sich auf eine strukturierte elementare Datei für eine lineare Variable bezieht, wird Sie möglicherweise ausgeführt, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht.

Wenn P2 = xxxxx011 und die elementare Datei zyklisch sind, weist dieser Befehl das gleiche Verhalten auf wie bei einem mit [**appendrecord**](iscardiso7816-appendrecord.md)erstellten Befehl.

Auf elementare Dateien ohne eine Daten Satzstruktur kann nicht geschrieben werden. Der konstruierte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Daten Satzstruktur angewendet wird.

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

[**Daten Satz**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
