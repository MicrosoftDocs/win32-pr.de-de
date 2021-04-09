---
description: Die putdata-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), mit dem ein einzelnes Primitives Datenobjekt oder der Satz von Datenobjekten, die in einem konstruierten Datenobjekt enthalten sind, abhängig von der ausgewählten Datei gespeichert wird.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: ISCardISO7816::P utdata-Methode (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866996"
---
# <a name="iscardiso7816putdata-method"></a>ISCardISO7816::P utdata-Methode

\[Die **putdata** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **putdata** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), mit dem ein einzelnes Primitives Datenobjekt oder der Satz von Datenobjekten, die in einem konstruierten Datenobjekt enthalten sind, abhängig von der ausgewählten Datei gespeichert wird.

Wie die Objekte gespeichert werden (das einmalige schreiben und/oder aktualisieren und/oder Anhängen), hängt von der Definition oder der Art der Datenobjekte ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP1* \[ in\]
</dt> <dd>

Codieren von P1-P2.



| Wert                                                                                  | Bedeutung                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040 Uhr</dt> </dl> | BER-TLV-Tag (1 Byte) in P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Anwendungsdaten (proprietäre Codierung)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Simple-TLV-Tag in P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV-Tag (2 Bytes) in P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Codieren von P1-P2.



| Wert                                                                                  | Bedeutung                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040 Uhr</dt> </dl> | BER-TLV-Tag (1 Byte) in P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Anwendungsdaten (proprietäre Codierung)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Simple-TLV-Tag in P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV-Tag (2 Bytes) in P1-P2<br/>        |



 

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Zeiger auf einen Byte Puffer, der die zu schreibenden Parameter und Daten enthält.

</dd> <dt>

*ppcmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.

Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt. Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mit dem *ppcmd* -Zeiger zurückgegeben.

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

Der Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus den Sicherheitsbedingungen entspricht, die von der Anwendung innerhalb des [*Kontexts*](../secgloss/c-gly.md) für die Funktion definiert werden.

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Speichern von Anwendungsdaten
</dt> <dd>

Liegt der Wert von P1-P2 im Bereich von 0100 bis 01FF, muss der Wert von P1-P2 ein Bezeichnertyp sein, der für interne Karten Tests und für proprietäre Dienste reserviert ist, die innerhalb eines bestimmten Anwendungs Kontexts aussagekräftig sind.

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Speichern von Datenobjekten
</dt> <dd>

Wenn der Wert P1-P2 im Bereich von 0040 bis 00FF liegt, muss P2 ein ber-TLV-Tag in einem einzelnen Byte sein. Der Wert von 00FF ist dafür reserviert, anzugeben, dass das Datenfeld ber-TLV-Datenobjekte enthält.

Liegt der Wert von P1-P2 im Bereich von 0200 bis 02FF, muss P2 ein Simple-TLV-Tag sein. Der Wert 0200 ist RFU. Der Wert 02FF ist dafür reserviert, anzugeben, dass das Datenfeld einfache TLV-Datenobjekte enthält.

Liegt der Wert von P1-P2 im Bereich von 4000 bis FFFF, muss der Wert von P1-P2 ein ber-TLV-Tag mit zwei Bytes sein. Die Werte 4000 bis FFFF sind RFU.

Wenn ein Primitives Datenobjekt bereitgestellt wird, muss das Datenfeld der Befehls Meldung den Wert des entsprechenden primitiven Datenobjekts enthalten.

Wenn ein konstruiertes Datenobjekt bereitgestellt wird, muss das Datenfeld der Befehls Meldung den Wert des konstruierten Datenobjekts enthalten (d. h. Datenobjekte einschließlich Tag, Länge und Wert).

</dd> </dl>

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

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
