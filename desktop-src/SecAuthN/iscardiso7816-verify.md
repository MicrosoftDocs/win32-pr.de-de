---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der den Vergleich (auf der Karte) der vom Schnittstellengerät gesendeten Überprüfungsdaten mit den auf der Karte gespeicherten Verweisdaten (z. B. Kennwort) initiiert.
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: ISCardISO7816::Verify-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0d01fe47133ddeaf7bba32a91711d76783bdfbb0a28762d7ddb7f9054d0108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014440"
---
# <a name="iscardiso7816verify-method"></a>ISCardISO7816::Verify-Methode

\[Die **Verify-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Verify-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der den Vergleich (auf der Karte) der vom Schnittstellengerät gesendeten Überprüfungsdaten mit den auf der Karte gespeicherten Verweisdaten (z. B. Kennwort) initiiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byRefCtrl* \[ In\]
</dt> <dd>

Ein Quantifizierer der Verweisdaten. Es folgt die Codierung des Verweissteuer steuerelements P2.

Wenn der Text leer ist, kann der Befehl entweder verwendet werden, um die Zahl "X" weiterer zulässiger Retries abzurufen (SW1-SW2=63CX) oder um zu überprüfen, ob die Überprüfung nicht erforderlich ist (SW1-SW2=9000).



| Wert                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Keine Informationen**</dt> </dl>                     | Bitposition: 00000000<br/> P2=00 ist reserviert, um anzugeben, dass kein bestimmter Qualifizierer in den Karten verwendet wird, bei denen der Befehl verify eindeutig auf die geheimen Daten verweist.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Globaler Verweis**</dt> </dl>         | Bitposition: 0-------<br/> Ein Beispiel für einen globalen Verweis wäre ein Kennwort.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Spezifischer Verweis**</dt> </dl> | Bitposition: 1-------<br/> Ein Beispiel für Specific Ref ist DF-spezifisches Kennwort.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                           | Bitposition: -xx-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Verweisdaten \#**</dt> </dl>        | Bitposition: ---xxxxx<br/> Die Verweisdatennummer kann beispielsweise eine Kennwortnummer oder ein kurzer EF-Bezeichner sein.<br/>                                                           |



 

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Ein Zeiger auf die Überprüfungsdaten. Dieser Parameter kann **NULL** sein. Der Standardwert ist **NULL**.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem von diesem Vorgang erstellten APDU-Befehl gefüllt. Wenn *ppCmd auf* **NULL** festgelegt wurde, wird intern ein [**SMARTCARD-ISCardCmd-Objekt**](iscardcmd.md) erstellt und mithilfe des *ppCmd-Zeigers* zurückgegeben. [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ein ungültiger Parameter wurde verwendet.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde übergeben.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                          |



 

## <a name="remarks"></a>Hinweise

Der Sicherheitsstatus kann als Ergebnis eines Vergleichs geändert werden. Nicht erfolgreiche Vergleiche können auf der Karte aufgezeichnet werden (z. B. um die Anzahl weiterer Versuche der Verwendung der Verweisdaten zu begrenzen).

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
