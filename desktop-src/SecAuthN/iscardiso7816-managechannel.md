---
description: Die managechannel-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der logische Kanäle öffnet und schließt.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816:: managechannel-Methode (scardssp. h)'
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
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042066"
---
# <a name="iscardiso7816managechannel-method"></a>ISCardISO7816:: managechannel-Methode

\[Die **managechannel** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **managechannel** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der logische Kanäle öffnet und schließt.

Die Open-Funktion öffnet einen neuen logischen Channel, der nicht der grundlegende ist. Optionen werden für die Karte bereitgestellt, um eine logische Channelnummer zuzuweisen, oder, wenn die Nummer des logischen Kanals an die Karte übergeben werden soll.

Die Close-Funktion schließt explizit einen logischen Channel, der nicht der grundlegende ist. Nach dem erfolgreichen Abschluss des Vorgangs sollte der logische Kanal zur erneuten Verwendung verfügbar sein.

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

*bychannelstate* \[ in\]
</dt> <dd>

Die Bit-B8 von P1 wird verwendet, um die Open-Funktion oder die Close-Funktion anzugeben. Wenn die "B8" den Wert "0" hat, öffnet "Channel verwalten" einen logischen Kanal

P1 = ' 00 ' zum Öffnen

P1 = ' 80 ' zum Schließen

Weitere Werte sind RFU.

</dd> <dt>

*bychannel* \[ in\]
</dt> <dd>

Für die Open-Funktion (P1 = ' 00 ') werden die Bits B1 und B2 von P2 verwendet, um die logische Channelnummer auf die gleiche Weise wie im-Klassen-Byte zu codieren, die anderen Bits von P2 sind RFU.

Wenn B1 und B2 von P2 **null** sind, weist die Karte eine logische Channelnummer zu, die in Bits B1 und B2 des Datenfelds zurückgegeben wird.

Wenn B1 und/oder B2 von P2 nicht **null** sind, codieren Sie eine andere logische Kanalnummer als die Basis. dann öffnet die Karte die extern zugewiesene logische Kanalnummer.

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

Wenn die Open-Funktion erfolgreich vom logischen Standard Kanal ausgeführt wird, muss der MF implizit als aktuelle DF ausgewählt werden, und der Sicherheitsstatus des neuen logischen Kanals sollte mit dem logischen Standard Kanal nach ATR übereinstimmen. Der Sicherheitsstatus des neuen logischen Kanals sollte von dem eines beliebigen anderen logischen Kanals getrennt sein.

Wenn die Open-Funktion erfolgreich von einem logischen Kanal ausgeführt wird, der nicht der Basis ist, wird die aktuelle DF des logischen Kanals, der den Befehl ausgegeben hat, als aktuelle DF ausgewählt. Außerdem sollte der Sicherheitsstatus für den neuen logischen Kanal mit dem Sicherheitsstatus des logischen Kanals identisch sein, von dem die Open-Funktion ausgeführt wurde.

Nach einer erfolgreichen Schließfunktion geht der Sicherheitsstatus, der sich auf diesen logischen Kanal bezieht, verloren.

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

 

 
