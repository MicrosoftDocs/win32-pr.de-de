---
description: Die Methode "Read Binary" erstellt einen APDU-Befehl (Application Protocol Data Unit), der eine Antwortnachricht abruft, die diesen Teil des Inhalts einer transparent strukturierten elementaren Datei enthält.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'ISCardISO7816:: Read Binary-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867847"
---
# <a name="iscardiso7816readbinary-method"></a>ISCardISO7816:: Read Binary-Methode

\[Die Methode "read **Binary** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Methode "read **Binary** " erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der eine Antwortnachricht abruft, die diesen Teil des Inhalts einer transparent strukturierten elementaren Datei enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP1* \[ in\]
</dt> <dd>

Das Feld P1-P2, versetzt zum ersten Byte, das am Anfang der Datei gelesen werden soll. Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt. der Wert von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei gelesen werden soll. Wenn der Wert für "B8 = 0" in P1 \| \| beträgt, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei gelesen werden soll.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Das Feld P1-P2, versetzt zum ersten Byte, das am Anfang der Datei gelesen werden soll. Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt. der Wert von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei gelesen werden soll. Wenn der Wert für "B8 = 0" in P1 \| \| beträgt, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei gelesen werden soll.

</dd> <dt>

*lbytestoread* \[ in\]
</dt> <dd>

Anzahl der Bytes, die aus dem transparenten EF gelesen werden sollen.

Wenn das Feld "Le" nur Nullen enthält, sollten alle Bytes bis zum Ende der Datei in der Grenze von 256 für die kurze Länge oder 65536 für die erweiterte Länge gelesen werden.

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

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.

Elementare Dateien ohne transparente Struktur können nicht gelöscht werden. Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.

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

[**Updatebinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**"Write Binary"**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
