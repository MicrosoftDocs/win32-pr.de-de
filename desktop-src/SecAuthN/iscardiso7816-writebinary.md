---
description: Die Methode "Write Binary" erstellt einen APDU-Befehl (Application Protocol Data Unit), der binäre Werte in eine elementare Datei schreibt.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816:: Beschreib tebinary-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958701"
---
# <a name="iscardiso7816writebinary-method"></a>ISCardISO7816:: Beschreib tebinary-Methode

\[Die Methode " **Write Binary** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Methode " **Write Binary** " erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der binäre Werte in eine elementare Datei schreibt.

Abhängig von den Dateiattributen führt der Befehl einen der folgenden Vorgänge aus:

-   Das logische OR der Bits, die bereits in der Karte vorhanden sind, mit den Bits, die im APDU-Befehl angegeben sind (logischer Lösch Zustand der Bits der Datei ist 0).
-   Das logische und der Bits, die bereits in der Karte vorhanden sind, mit den Bits, die im Befehl APDU angegeben sind (logischer Lösch Zustand der Bits der Datei ist 1).
-   Der einmalige Schreibvorgang in der Karte der Bits, die im Befehl APDU angegeben sind.

Wenn im Daten Codierungs Byte keine Angabe angegeben ist, gilt das logische OR-Verhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteBinary(
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

Offset am Schreib Speicherort vom Anfang der Binärdatei (EF). Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, die Größe von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll. Wenn "B8 = 0" in P1 \| \| ist, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Offset am Schreib Speicherort vom Anfang der Binärdatei (EF). Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, die Größe von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll. Wenn "B8 = 0" in P1 \| \| ist, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei geschrieben werden soll.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Ein Zeiger auf die Zeichenfolge der zu schreibenden Dateneinheiten.

</dd> <dt>

*ppcmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.

Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt. Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.

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

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.

Wenn ein Schreib binärer Vorgang auf eine Dateneinheit eines einmaligen Schreibvorgangs von EF angewendet wurde, werden alle weiteren Schreibvorgänge, die auf diese Dateneinheit verweisen, abgebrochen, wenn sich der Inhalt der Dateneinheit oder der logische Lösch Status Indikator (sofern vorhanden), der an diese Dateneinheit angefügt ist, vom logischen gelöschten Zustand unterscheidet.

Auf elementare Dateien ohne transparente Struktur kann nicht geschrieben werden. Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.

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

[**Erasebinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**"Read Binary"**](iscardiso7816-readbinary.md)
</dt> <dt>

[**Updatebinary**](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
