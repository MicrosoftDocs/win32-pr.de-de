---
description: Erstellt einen APDU-Befehl (Application Protocol Data Unit), der einen Teil des Inhalts einer elementaren Datei ab einem angegebenen Offset sequenziell auf seinen logischen gelöschten Zustand setzt.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: ISCardISO7816::EraseBinary-Methode (Scardssp.h)
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
ms.openlocfilehash: 012927e21e3ed897136a9b058ae03539b7d2e2ac0e581d04cb14235aed9ae80f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007898"
---
# <a name="iscardiso7816erasebinary-method"></a>ISCardISO7816::EraseBinary-Methode

\[Die **EraseBinary-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **EraseBinary-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der einen Teil des Inhalts einer elementaren Datei ab einem angegebenen Offset sequenziell in seinen logischen gelöschten Zustand einordnt.

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

*byP1* \[ In\]
</dt> <dd>

RFU-Position.

Wenn b8=1 in P1, dann sind b7 und b6 von P1 auf 0 (RFU-Bits) festgelegt, b5 bis b1 von P1 sind ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Byte, das (in Dateneinheiten) vom Anfang der Datei gelöscht werden soll.

Wenn b8=0 in P1, dann ist P1 P2 der Offset des ersten Byte, das (in Dateneinheiten) vom Anfang der Datei \| \| gelöscht werden soll.

Wenn das Datenfeld vorhanden ist, wird der Offset der ersten Dateneinheit, die nicht gelöscht werden soll, mit codesiert. Dieser Offset muss höher sein als der in P1-P2 codierte Offset. Wenn das Datenfeld leer ist, wird der Befehl bis zum Ende der Datei gelöscht.

</dd> <dt>

*byP2* \[ In\]
</dt> <dd>

RFU-Position.

Wenn b8=1 in P1, dann sind b7 und b6 von P1 auf 0 (RFU-Bits) festgelegt, b5 bis b1 von P1 sind ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Byte, das (in Dateneinheiten) vom Anfang der Datei gelöscht werden soll.

Wenn b8=0 in P1, dann ist P1 P2 der Offset des ersten Byte, das (in Dateneinheiten) vom Anfang der Datei \| \| gelöscht werden soll.

Wenn das Datenfeld vorhanden ist, wird der Offset der ersten Dateneinheit, die nicht gelöscht werden soll, mit codesiert. Dieser Offset muss höher sein als der in P1-P2 codierte Offset. Wenn das Datenfeld leer ist, wird der Befehl bis zum Ende der Datei gelöscht.

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Ein Zeiger auf die Daten, die den Löschbereich angibt. Dieser Parameter kann NULL **sein.**

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem von diesem Vorgang erstellten APDU-Befehl gefüllt. Wenn *ppCmd auf* **NULL** festgelegt wurde, wird intern ein [**SMARTCARD-ISCardCmd-Objekt**](iscardcmd.md) erstellt und mithilfe des *ppCmd-Zeigers* zurückgegeben. [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ein ungültiger Parameter wurde übergeben.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde übergeben.<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) die Sicherheitsattribute der elementaren Datei erfüllt, die verarbeitet wird.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, legt er die Datei als aktuelle elementare Datei fest.

Elementare Dateien ohne eine transparente Struktur können nicht gelöscht werden. Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.

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
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
