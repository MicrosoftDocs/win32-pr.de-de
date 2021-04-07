---
description: Die GetData-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der je nach ausgewähltem Dateityp entweder ein einzelnes Primitives Datenobjekt oder einen Satz von Datenobjekten (in einem konstruierten Datenobjekt enthalten) abruft.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'ISCardISO7816:: GetData-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758095"
---
# <a name="iscardiso7816getdata-method"></a>ISCardISO7816:: GetData-Methode

\[Die **GetData** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **GetData** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der je nach ausgewähltem Dateityp entweder ein einzelnes Primitives Datenobjekt oder einen Satz von Datenobjekten (in einem konstruierten Datenobjekt enthalten) abruft.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP1* \[ in\]
</dt> <dd>

Parameter.



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

Parameter.



| Wert                                                                                  | Bedeutung                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040 Uhr</dt> </dl> | BER-TLV-Tag (1 Byte) in P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Anwendungsdaten (proprietäre Codierung)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Simple-TLV-Tag in P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV-Tag (2 Bytes) in P1-P2<br/>        |



 

</dd> <dt>

*lbytestoget* \[ in\]
</dt> <dd>

Anzahl von Bytes, die in der Antwort erwartet werden.

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

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu lesenden elementaren Datei entspricht. Sicherheitsbedingungen sind von der Richtlinie der Karte abhängig und können durch [**externalauthenticate**](iscardiso7816-externalauthenticate.md), [**internalauthenticate**](iscardiso7816-internalauthenticate.md), [**iscardauth**](iscardauth.md)usw. manipuliert werden.

Um eine Datei auszuwählen, wählen Sie [**selectfile**](iscardiso7816-selectfile.md)aus.

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

[**Externalauthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**Internalauthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**Iscardauth**](iscardauth.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**Putdata**](iscardiso7816-putdata.md)
</dt> <dt>

[**Selectfile**](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
