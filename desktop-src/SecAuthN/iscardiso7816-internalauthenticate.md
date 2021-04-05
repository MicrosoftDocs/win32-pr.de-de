---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der die Berechnung der Authentifizierungsdaten durch die Karte mit den vom Schnittstellen Gerät gesendeten Abfrage Daten und einem relevanten geheimen Schlüssel (z. b. einem Schlüssel) initiiert, der in der Karte gespeichert ist.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'ISCardISO7816:: internalauthenticate-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042067"
---
# <a name="iscardiso7816internalauthenticate-method"></a>ISCardISO7816:: internalauthenticate-Methode

\[Die **internalauthenticate** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **internalauthenticate** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der die Berechnung der Authentifizierungsdaten durch die Karte initiiert, indem die vom Schnittstellen Gerät gesendeten Anforderungs Daten und ein relevanter geheimer Schlüssel (z. b. ein Schlüssel) auf der Karte gespeichert werden.

Wenn das relevante Geheimnis an das MF angehängt ist, kann der Befehl verwendet werden, um die Karte als Ganzes zu authentifizieren.

Wenn das relevante Geheimnis an eine andere DF angefügt ist, kann der Befehl zum Authentifizieren der DF verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byalgorithmref* \[ in\]
</dt> <dd>

Verweis auf den Algorithmus in der Karte.

Wenn dieser Wert 0 (null) ist, bedeutet dies, dass keine Informationen angegeben werden. Der Verweis auf den Algorithmus ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.

</dd> <dt>

*bysecretref* \[ in\]
</dt> <dd>

Verweis auf den geheimen Schlüssel.



| Wert                                                                                                                                                                                    | Bedeutung                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Keine Informationen**</dt> </dl>                     | Bitposition: 00000000 <br/> Es werden keine Informationen angegeben. Der Verweis auf das Geheimnis ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Globaler Verweis**</dt> </dl>         | Bitposition: 0------- <br/> Globale Verweis Daten (ein für die MF spezifischer Schlüssel).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Spezifischer Verweis**</dt> </dl> | Bitposition: 1-------<br/> Bestimmte Verweis Daten (ein DF-spezifischer Schlüssel).<br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Bitposition:-XX-----<br/> 00 (andere Werte sind RFU).<br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Geheimen**</dt> </dl>                         | Bitposition:---XXXXX<br/> Die Nummer des Geheimnisses.<br/>                                                                                                              |



 

</dd> <dt>

*pchallenge* \[ in\]
</dt> <dd>

Zeiger auf die Authentifizierungs bezogenen Daten (z. b. "Challenge").

</dd> <dt>

*lreplybytes* \[ in\]
</dt> <dd>

Maximale Anzahl von Bytes, die als Antwort erwartet werden.

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

Die erfolgreiche Ausführung des Befehls kann dem erfolgreichen Abschluss vorheriger Befehle (z. b. überprüfen oder auswählen der Datei) oder der Auswahl (z. b. des relevanten Geheimnisses) unterliegen.

Wenn beim Ausgeben des Befehls eine Taste und ein Algorithmus ausgewählt sind, verwendet der Befehl möglicherweise implizit den Schlüssel und den Algorithmus.

Die Häufigkeit, mit der der Befehl ausgegeben wird, kann in der Karte aufgezeichnet werden, um die Anzahl der weiteren Versuche der Verwendung des relevanten Geheimnisses oder des Algorithmus einzuschränken.

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
