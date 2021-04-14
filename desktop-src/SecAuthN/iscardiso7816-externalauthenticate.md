---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der den Sicherheitsstatus bedingt aktualisiert und die Identität des Computers überprüft, wenn Sie von der Smartcard nicht als vertrauenswürdig eingestuft wird.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816:: externalauthenticate-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393550"
---
# <a name="iscardiso7816externalauthenticate-method"></a>ISCardISO7816:: externalauthenticate-Methode

\[Die **externalauthenticate** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **externalauthenticate** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der den Sicherheitsstatus bedingt aktualisiert und die Identität des Computers überprüft, wenn Sie von der [*Smartcard*](../secgloss/s-gly.md) nicht als vertrauenswürdig eingestuft wird.

Der Befehl verwendet das Ergebnis (ja oder Nein) der Berechnung durch die Karte (basierend auf einer Herausforderung, die zuvor von der Karte ausgegeben wurde, z. b. mit dem Befehl "in \_ get \_ Challenge"), einem Schlüssel (möglicherweise geheimer Schlüssel), der auf der Karte gespeichert ist, und vom Schnittstellen Gerät übertragene Authentifizierungsdaten.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byalgorithmref* \[ in\]
</dt> <dd>

Der Verweis auf den Algorithmus in der Karte.

Wenn dieser Wert 0 (null) ist, bedeutet dies, dass keine Informationen angegeben werden. Der Verweis auf den Algorithmus ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.

</dd> <dt>

*bysecretref* \[ in\]
</dt> <dd>

Der Verweis auf das Geheimnis.



| Wert                                                                                                                                                                                    | Bedeutung                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Keine Informationen**</dt> </dl>                     | Bitposition: 00000000<br/> Es werden keine Informationen angegeben. Der Verweis auf das Geheimnis ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Globaler Verweis**</dt> </dl>         | Bitposition: 0-------<br/> Globale Verweis Daten (ein für die MF spezifischer Schlüssel).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Spezifischer Verweis**</dt> </dl> | Bitposition: 1-------<br/> Bestimmte Verweis Daten (ein DF-spezifischer Schlüssel).<br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Bitposition:-XX-----<br/> 00 (andere Werte sind RFU).<br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Geheimen**</dt> </dl>                         | Bitposition:---XXXXX<br/> Die Nummer des Geheimnisses.<br/>                                                                                                             |



 

</dd> <dt>

*pchallenge* \[ in\]
</dt> <dd>

Ein Zeiger auf die Authentifizierungs bezogenen Daten. Dieser Parameter kann **null** sein.

</dd> <dt>

*ppcmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.

Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt. Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mithilfe des *ppcmd* -Zeigers zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ein ungültiger Parameter wurde übergeben.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>              |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Damit der gekapselte Befehl erfolgreich ausgeführt werden kann, muss die letzte von der Karte erhaltene Abfrage gültig sein.

Nicht erfolgreiche Vergleiche können auf der Karte aufgezeichnet werden (z. b. um die Anzahl der weiteren Versuche der Verwendung der Verweis Daten einzuschränken).

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

[**Internalauthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
