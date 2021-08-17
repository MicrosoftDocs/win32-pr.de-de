---
description: Die ManageChannel-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der logische Kanäle öffnet und schließt.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: ISCardISO7816::ManageChannel-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92fb91c0630996938e247dbc244ac0c311c52531401367d5326bd197ffaabf9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481119"
---
# <a name="iscardiso7816managechannel-method"></a>ISCardISO7816::ManageChannel-Methode

\[Die **ManageChannel-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ManageChannel-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der logische Kanäle öffnet und schließt.

Die open-Funktion öffnet einen neuen logischen Kanal, der nicht der grundlegende Kanal ist. Optionen werden für die Karte bereitgestellt, um eine logische Kanalnummer zu zuweisen, oder für die logische Kanalnummer, die der Karte bereitgestellt werden soll.

Die close-Funktion schließt explizit einen anderen logischen Kanal als den grundlegenden Kanal. Nach dem erfolgreichen Schließen muss der logische Kanal zur erneuten Verwendung verfügbar sein.

## <a name="syntax"></a>Syntax


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byChannelState* \[ In\]
</dt> <dd>

Bit b8 von P1 wird verwendet, um die open-Funktion oder die close-Funktion anzugeben. Wenn b8 0 ist, dann öffnet MANAGE CHANNEL einen logischen Kanal, und wenn b8 1 ist, schließt MANAGE CHANNEL einen logischen Kanal:

P1 = '00' zum Öffnen

P1 = '80' zu schließen

Andere Werte sind RFU.

</dd> <dt>

*byChannel* \[ In\]
</dt> <dd>

Für die open-Funktion (P1 = '00') werden die Bits b1 und b2 von P2 verwendet, um die logische Kanalnummer auf die gleiche Weise wie im Klassen-Byte zu codieren, die anderen Bits von P2 sind RFU.

Wenn b1 und b2 von P2 **NULL** sind, weist die Karte eine logische Kanalnummer zu, die in den Bits b1 und b2 des Datenfelds zurückgegeben wird.

Wenn b1 und/oder b2 von P2 nicht **NULL** sind, codierung eine andere logische Kanalnummer als die einfache; Dann öffnet die Karte die extern zugewiesene logische Kanalnummer.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem von diesem Vorgang erstellten APDU-Befehl gefüllt. Wenn *ppCmd auf* **NULL festgelegt** wurde, wird intern ein [**SMARTCARD-ISCardCmd-Objekt**](iscardcmd.md) erstellt und mit dem *ppCmd-Zeiger* zurückgegeben. [](../secgloss/s-gly.md)

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

Wenn die open-Funktion erfolgreich über den grundlegenden logischen Kanal ausgeführt wird, muss die MF implizit als aktuelle DF ausgewählt werden, und der Sicherheitsstatus des neuen logischen Kanals sollte mit dem grundlegenden logischen Kanal nach ATR identisch sein. Der Sicherheitsstatus des neuen logischen Kanals sollte von dem eines anderen logischen Kanals getrennt sein.

Wenn die open-Funktion erfolgreich über einen logischen Kanal ausgeführt wird, der nicht der grundlegende Kanal ist, wird das aktuelle DF des logischen Kanals, der den Befehl ausgegeben hat, als aktuelles DF ausgewählt. Darüber hinaus sollte der Sicherheitsstatus für den neuen logischen Kanal mit dem Sicherheitsstatus des logischen Kanals identisch sein, über den die offene Funktion ausgeführt wurde.

Nach einer erfolgreichen Close-Funktion geht der Sicherheitsstatus im Zusammenhang mit diesem logischen Kanal verloren.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
