---
description: Die PutData-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der je nach ausgewählter Datei ein einzelnes primitives Datenobjekt oder einen Satz von Datenobjekten speichert, die in einem konstruierten Datenobjekt enthalten sind.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: ISCardISO7816::P utData-Methode (Scardssp.h)
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
ms.openlocfilehash: 66698db3c15223071167441fc37437bfa299baa100c58943a41cb4d774a8e17c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141113"
---
# <a name="iscardiso7816putdata-method"></a>ISCardISO7816::P utData-Methode

\[Die **PutData-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **PutData-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der je nach ausgewählter Datei ein einzelnes primitives Datenobjekt oder einen Satz von Datenobjekten speichert, die in einem konstruierten Datenobjekt enthalten sind.

Wie die Objekte gespeichert werden (einmaliges Schreiben und/oder Aktualisieren und/oder Anfügen), hängt von der Definition oder der Art der Datenobjekte ab.

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

*byP1* \[ In\]
</dt> <dd>

Codierung von P1-P2.



| Wert                                                                                  | Bedeutung                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | BER-TLV-Tag (1 Byte) in P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Anwendungsdaten (proprietäre Codierung)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | SIMPLE-TLV-Tag in P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV-Tag (2 Bytes) in P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ In\]
</dt> <dd>

Codierung von P1-P2.



| Wert                                                                                  | Bedeutung                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | BER-TLV-Tag (1 Byte) in P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Anwendungsdaten (proprietäre Codierung)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | SIMPLE-TLV-Tag in P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV-Tag (2 Bytes) in P1-P2<br/>        |



 

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Zeiger auf einen Bytepuffer, der die zu schreibenden Parameter und Daten enthält.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem APDU-Befehl gefüllt, der von diesem Vorgang erstellt wurde. Wenn *ppCmd* auf **NULL** festgelegt wurde, wird intern ein [**ISCardCmd-Smartcardobjekt**](iscardcmd.md) erstellt und mit dem *ppCmd-Zeiger* zurückgegeben. [](../secgloss/s-gly.md)

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

Der Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus die von der Anwendung im [*Kontext*](../secgloss/c-gly.md) für die Funktion definierten Sicherheitsbedingungen erfüllt.

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Anwendungsdaten
</dt> <dd>

Wenn der Wert von P1-P2 im Bereich von 0100 bis 01FF liegt, muss der Wert von P1-P2 ein Bezeichner sein, der für interne Kartentests und proprietäre Dienste reserviert ist, die innerhalb eines bestimmten Anwendungskontexts sinnvoll sind.

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Datenobjekte
</dt> <dd>

Wenn der Wert P1-P2 im Bereich von 0040 bis 00FF liegt, muss der Wert von P2 ein BER-TLV-Tag für ein einzelnes Byte sein. Der Wert 00FF ist für den Hinweis reserviert, dass das Datenfeld BER-TLV-Datenobjekte enthält.

Wenn der Wert von P1-P2 im Bereich von 0200 bis 02FF liegt, muss der Wert von P2 ein SIMPLE-TLV-Tag sein. Der Wert 0200 ist RFU. Der Wert 02FF ist für den Hinweis reserviert, dass das Datenfeld SIMPLE-TLV-Datenobjekte enthält.

Wenn der Wert von P1-P2 im Bereich von 4000 bis FFFF liegt, muss der Wert von P1-P2 ein BER-TLV-Tag mit zwei Bytes sein. Die Werte 4000 bis FFFF sind RFU.

Wenn ein primitives Datenobjekt bereitgestellt wird, muss das Datenfeld der Befehlsmeldung den Wert des entsprechenden primitiven Datenobjekts enthalten.

Wenn ein konstruiertes Datenobjekt bereitgestellt wird, muss das Datenfeld der Befehlsmeldung den Wert des konstruierten Datenobjekts enthalten (d. b. Datenobjekte einschließlich Tag, Länge und Wert).

</dd> </dl>

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

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
