---
description: Die UpdateRecord-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der einen bestimmten Datensatz mit den Bits aktualisiert, die im APDU-Befehl angegeben sind.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'ISCardISO7816:: UpdateRecord-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216212"
---
# <a name="iscardiso7816updaterecord-method"></a>ISCardISO7816:: UpdateRecord-Methode

\[Die **UpdateRecord** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **UpdateRecord** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der einen bestimmten Datensatz mit den Bits aktualisiert, die im APDU-Befehl angegeben sind.

> [!Note]  
> Bei der Verwendung der aktuellen Daten Satz Adressierung legt der Befehl den Datensatz-Zeiger auf den erfolgreich aktualisierten Datensatz fest.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateRecord(
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

P1-Wert:

P1 = 00 legt den aktuellen Datensatz fest.

P1! = ' 00 ' ist die Nummer des angegebenen Datensatzes

</dd> <dt>

*ByRef STRG* \[ in\]
</dt> <dd>

Codieren des Verweis Steuer Elements P2:



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

Zeiger auf den zu aktualisierenden Datensatz.

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

Wenn der konstruierte Befehl für eine lineare oder zyklische strukturierte elementare Datei gilt, wird er abgebrochen, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht.

Wenn der Befehl auf eine strukturierte elementare Datei für eine lineare Variable angewendet wird, kann er ausgeführt werden, wenn die Daten Satz Länge von der Länge des vorhandenen Datensatzes abweicht.

Die "Previous"-Option des Befehls (P2 = xxxxx011), der auf eine zyklische Datei angewendet wird, hat das gleiche Verhalten wie ein Befehl, der von [**appendrecord**](iscardiso7816-appendrecord.md)erstellt wurde.

Elementare Dateien ohne Daten Satzstruktur können nicht gelesen werden. Der konstruierte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Daten Satzstruktur angewendet wird.

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

[**Beschreibecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
