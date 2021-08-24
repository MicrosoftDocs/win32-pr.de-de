---
description: Erstellt einen APDU-Befehl, der einen der aufgeführten Vorgänge initiiert.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: ISCardISO7816::WriteRecord-Methode (Scardssp.h)
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
ms.openlocfilehash: a023443f1121759872c4eba0743e5db5b01c8446403b312644e22c83559a527d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014380"
---
# <a name="iscardiso7816writerecord-method"></a>ISCardISO7816::WriteRecord-Methode

\[Die **WriteRecord-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **WriteRecord-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der einen der folgenden Vorgänge initiiert:

-   Das einmal geschriebene eines Datensatzes.
-   Das logische **OR** der Datenbytes eines Datensatzes, der bereits auf der Karte vorhanden ist, mit den Datenbytes des Datensatzes, der in der Befehls-APDU angegeben ist.
-   Das logische AND der Datenbytes eines Datensatzes, der bereits auf der Karte vorhanden ist, mit den Datenbytes des Datensatzes, der in der Befehls-APDU angegeben ist.

Wenn im Datencodierungs-Byte kein Hinweis angegeben wird, gilt das logische OR-Verhalten.

> [!Note]  
> Bei Verwendung der aktuellen Datensatz adressierung legt der Befehl den Datensatzzeiger für den erfolgreich aktualisierten Datensatz fest.

 

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

*byRecordId* \[ In\]
</dt> <dd>

Datensatzidentifikation. Dies ist der P1-Wert:

P1 = '00' bezeichnet den aktuellen Datensatz.

P1 != '00' ist die Nummer des angegebenen Datensatzes.

</dd> <dt>

*byRefCtrl* \[ In\]
</dt> <dd>

Codierung des Verweissteuersteuer steuerelements P2.



| Wert                                                                                                                                                                                                | Bedeutung                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**Aktuelles EF**</dt> </dl>                     | Bitposition: 00000---<br/> Derzeit ausgewähltes EF.<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Kurze EF-ID**</dt> </dl>                 | Bitposition: xxxxx---<br/> Kurzer EF-Bezeichner.<br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <dt>**Erster Datensatz**</dt> </dl>             | Bitposition: -----000<br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <dt>**Letzter Datensatz**</dt> </dl>                 | Bitposition: -----001<br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <dt>**Nächster Datensatz**</dt> </dl>                 | Bitposition: -----010<br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <dt>**Vorheriger Datensatz**</dt> </dl> | Bitposition: -----011<br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <dt>**Datensatz \# in P1**</dt> </dl>    | Bitposition: -----100<br/>                                   |



 

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Zeiger auf den zu schreibenden Datensatz.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem von diesem Vorgang erstellten APDU-Befehl gefüllt. Wenn *ppCmd auf* **NULL festgelegt** wurde, wird intern ein [**SMARTCARD-ISCardCmd-Objekt**](iscardcmd.md) erstellt und über den *ppCmd-Zeiger* zurückgegeben. [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde übergeben.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) die Sicherheitsattribute der elementaren Datei erfüllt, die verarbeitet wird.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, legt er die Datei als aktuelle elementare Datei fest. Wenn zum Zeitpunkt der Ausgabe dieses Befehls eine andere elementare Datei ausgewählt ist, kann dieser Befehl ohne Identifizierung der aktuell ausgewählten Datei verarbeitet werden.

Wenn der gekapselte Befehl für eine linear feste oder zyklische strukturierte elementare Datei gilt, wird er abgebrochen, wenn sich die Datensatzlänge von der Länge des vorhandenen Datensatzes unterscheiden. Wenn sie für eine linear-variable strukturierte elementare Datei gilt, kann sie ausgeführt werden, wenn sich die Datensatzlänge von der Länge des vorhandenen Datensatzes unterscheiden.

Wenn P2=xxxxx011 und die elementare Datei eine zyklische Datei ist, hat dieser Befehl das gleiche Verhalten wie ein Befehl, der mit [**AppendRecord erstellt wurde.**](iscardiso7816-appendrecord.md)

Elementare Dateien ohne Datensatzstruktur können nicht geschrieben werden. Der konstruierte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne Datensatzstruktur angewendet wird.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardISO7816**](iscardiso7816.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53B6AA68-3F56-11D0-916B-00AA00C18068 definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
