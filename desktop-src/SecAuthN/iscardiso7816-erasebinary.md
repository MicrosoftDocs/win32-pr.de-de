---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der einen Teil des Inhalts einer elementaren Datei sequenziell auf den logischen Lösch Zustand festlegt, beginnend bei einem bestimmten Offset.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'ISCardISO7816:: erasebinary-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373303"
---
# <a name="iscardiso7816erasebinary-method"></a>ISCardISO7816:: erasebinary-Methode

\[Die **erasebinary** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **erasebinary** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der einen Teil des Inhalts einer elementaren Datei sequenziell auf den logischen Lösch Zustand festlegt, beginnend bei einem bestimmten Offset.

## <a name="syntax"></a>Syntax


```C++
HRESULT EraseBinary(
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

RFU-Position.

Wenn "B8 = 1" in P1 ist, werden B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, der Wert für "B5 bis B1" von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, der vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).

Wenn in P1 den Wert 0 (null) hat, \| \| ist P1 P2 der Offset des ersten Bytes, das vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).

Wenn das Datenfeld vorhanden ist, wird der Offset der ersten Dateneinheit, die nicht gelöscht werden soll, codiert. Dieser Offset muss höher sein als der in P1-P2 codierte. Wenn das Datenfeld leer ist, wird der Befehl bis zum Ende der Datei gelöscht.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

RFU-Position.

Wenn "B8 = 1" in P1 ist, werden B7 und B6 von P1 auf NULL (RFU Bits) festgelegt, der Wert für "B5 bis B1" von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, der vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).

Wenn in P1 den Wert 0 (null) hat, \| \| ist P1 P2 der Offset des ersten Bytes, das vom Anfang der Datei gelöscht werden soll (in den Dateneinheiten).

Wenn das Datenfeld vorhanden ist, wird der Offset der ersten Dateneinheit, die nicht gelöscht werden soll, codiert. Dieser Offset muss höher sein als der in P1-P2 codierte. Wenn das Datenfeld leer ist, wird der Befehl bis zum Ende der Datei gelöscht.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Ein Zeiger auf die Daten, die den Löschbereich angeben. Dieser Parameter kann **null** sein.

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**"Read Binary"**](iscardiso7816-readbinary.md)
</dt> <dt>

[**Updatebinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**"Write Binary"**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
