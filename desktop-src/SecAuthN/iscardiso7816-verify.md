---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der den Vergleich (in der Karte) der Überprüfungs Daten initiiert, die vom Schnittstellen Gerät mit den Verweis Daten, die auf der Karte gespeichert sind (z. b. Password), gesendet werden.
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816:: Verify-Methode (scardssp. h)'
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
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348083"
---
# <a name="iscardiso7816verify-method"></a>ISCardISO7816:: Verify-Methode

\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Verify** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der den Vergleich (auf der Karte) der Überprüfungs Daten initiiert, die vom Schnittstellen Gerät mit den Verweis Daten, die auf der Karte gespeichert sind (z. b. Password), gesendet werden.

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

*ByRef STRG* \[ in\]
</dt> <dd>

Ein Quantifizierer der Verweis Daten. Das Codieren des Verweis Steuer Elements P2 folgt.

Wenn der Text leer ist, kann der Befehl entweder zum Abrufen der Zahl "X" der weiteren zulässigen Wiederholungen (SW1-SW2 = 63CX) oder zum Überprüfen, ob die Überprüfung nicht erforderlich ist (SW1-SW2 = 9000), verwendet werden.



| Wert                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Keine Informationen**</dt> </dl>                     | Bitposition: 00000000<br/> P2 = 00 gibt an, dass kein bestimmter Qualifizierer auf den Karten verwendet wird, an denen der Verify-Befehl eindeutig auf die geheimen Daten verweist.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Globaler Verweis**</dt> </dl>         | Bitposition: 0-------<br/> Ein Beispiel für einen globalen Verweis wäre ein Kennwort.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Spezifischer Verweis**</dt> </dl> | Bitposition: 1-------<br/> Ein Beispiel für einen bestimmten Verweis ist ein DF-spezifisches Kennwort.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Bitposition:-XX-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Verweis Daten \#**</dt> </dl>        | Bitposition:---XXXXX<br/> Die Verweis Daten Nummer kann z. b. eine Kenn Wort Nummer oder eine kurze EF-ID sein.<br/>                                                           |



 

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Ein Zeiger auf die Überprüfungs Daten. Dieser Parameter kann **NULL** sein. Der Standardwert ist **NULL**.

</dd> <dt>

*ppcmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.

Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt. Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mithilfe des *ppcmd* -Zeigers zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Es wurde ein ungültiger Parameter verwendet.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>            |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Der Sicherheitsstatus kann aufgrund eines Vergleichs geändert werden. Nicht erfolgreiche Vergleiche können auf der Karte aufgezeichnet werden (z. b. um die Anzahl der weiteren Versuche der Verwendung der Verweis Daten einzuschränken).

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
