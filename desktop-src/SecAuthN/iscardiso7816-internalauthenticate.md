---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der die Berechnung der Authentifizierungsdaten durch die Karte initiiert, indem die vom Schnittstellengerät gesendeten Abfragedaten und ein relevantes Geheimnis (z. B. ein Schlüssel) auf der Karte verwendet werden.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: ISCardISO7816::InternalAuthenticate-Methode (Scardssp.h)
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
ms.openlocfilehash: d4c3385313fb5b9c9c7ba72957244bd81757b0cd1e79bcec906e740c69b66292
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922990"
---
# <a name="iscardiso7816internalauthenticate-method"></a>ISCardISO7816::InternalAuthenticate-Methode

\[Die **InternalAuthenticate-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **InternalAuthenticate-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der die Berechnung der Authentifizierungsdaten durch die Karte mithilfe der vom Schnittstellengerät gesendeten Abfragedaten und eines relevanten Geheimnisses (z. B. eines Schlüssels) initiiert, der auf der Karte gespeichert ist.

Wenn das relevante Geheimnis an den MF angefügt ist, kann der Befehl verwendet werden, um die Karte als Ganzes zu authentifizieren.

Wenn das relevante Geheimnis an einen anderen DF angefügt ist, kann der Befehl verwendet werden, um diesen DF zu authentifizieren.

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

*byAlgorithmRef* \[ In\]
</dt> <dd>

Verweis auf den Algorithmus auf der Karte.

Wenn dieser Wert 0 (null) ist, bedeutet dies, dass keine Informationen angegeben werden. Der Verweis auf den Algorithmus ist entweder vor dem Ausgeben des Befehls bekannt oder wird im Datenfeld bereitgestellt.

</dd> <dt>

*bySecretRef* \[ In\]
</dt> <dd>

Verweis auf das Geheimnis.



| Wert                                                                                                                                                                                    | Bedeutung                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Keine Informationen**</dt> </dl>                     | Bitposition: 00000000 <br/> Es werden keine Informationen angegeben. Der Verweis auf das Geheimnis ist entweder vor dem Ausführen des Befehls bekannt oder wird im Datenfeld bereitgestellt.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Globaler Verweis**</dt> </dl>         | Bitposition: 0------- <br/> Globale Verweisdaten (ein MF-spezifischer Schlüssel).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Spezifische Referenz**</dt> </dl> | Bitposition: 1-------<br/> Spezifische Verweisdaten (ein DF-spezifischer Schlüssel).<br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                           | Bitposition: -xx-----<br/> 00 (andere Werte sind RFU).<br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**`Secret`**</dt> </dl>                         | Bitposition: ---xxxxx<br/> Die Nummer des Geheimnisses.<br/>                                                                                                              |



 

</dd> <dt>

*pChallenge* \[ In\]
</dt> <dd>

Zeiger auf die authentifizierungsbezogenen Daten (z. B. Abfrage).

</dd> <dt>

*lReplyBytes* \[ In\]
</dt> <dd>

Maximale Anzahl von Bytes, die als Antwort erwartet werden.

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

Die erfolgreiche Ausführung des Befehls kann davon abhängig sein, dass vorherige Befehle (z. B. VERIFY oder SELECT FILE) oder Auswahlmöglichkeiten (z. B. das relevante Geheimnis) erfolgreich abgeschlossen wurden.

Wenn beim Ausgeben des Befehls derzeit ein Schlüssel und ein Algorithmus ausgewählt sind, kann der Befehl implizit den Schlüssel und den Algorithmus verwenden.

Wie oft der Befehl ausgegeben wird, kann auf der Karte aufgezeichnet werden, um die Anzahl weiterer Versuche, das entsprechende Geheimnis oder den Algorithmus zu verwenden, einzuschränken.

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

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
