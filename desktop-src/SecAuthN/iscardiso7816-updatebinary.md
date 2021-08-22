---
description: Die UpdateBinary-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der die in einer elementaren Datei vorhandenen Bits mit den Bits aktualisiert, die im APDU-Befehl angegeben sind.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: ISCardISO7816::UpdateBinary-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 46f7bbc66d76fd9d07390e6d78f25cc96111801cea8f715d84b81e704518cbbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577010"
---
# <a name="iscardiso7816updatebinary-method"></a>ISCardISO7816::UpdateBinary-Methode

\[Die **UpdateBinary-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **UpdateBinary-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der die in einer elementaren Datei vorhandenen Bits mit den im APDU-Befehl angegebenen Bits aktualisiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateBinary(
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

Offset zum Schreibspeicherort (Update) in die Binärdatei ab dem Anfang der Binärdatei. Wenn b8=1 in P1, dann sind b7 und b6 von P1 auf 0 (RFU-Bits) festgelegt, b5 bis b1 von P1 sind ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Byte, das in Dateneinheiten vom Anfang der Datei aktualisiert werden soll. Wenn b8=0 in P1 ist, ist P1 \| \| P2 der Offset des ersten Byte, das in Dateneinheiten vom Anfang der Datei aktualisiert werden soll.

</dd> <dt>

*byP2* \[ In\]
</dt> <dd>

Offset zum Schreibspeicherort (Update) in die Binärdatei ab dem Anfang der Binärdatei. Wenn b8=1 in P1, dann sind b7 und b6 von P1 auf 0 (RFU-Bits) festgelegt, b5 bis b1 von P1 sind ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Byte, das in Dateneinheiten vom Anfang der Datei aktualisiert werden soll. Wenn b8=0 in P1 ist, ist P1 \| \| P2 der Offset des ersten Byte, das in Dateneinheiten vom Anfang der Datei aktualisiert werden soll.

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Zeiger auf die Zeichenfolge der zu aktualisierenden Dateneinheiten.

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

Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der Smartcard die Sicherheitsattribute der zu verarbeitenden elementaren Datei erfüllt.

Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.

Elementare Dateien ohne transparente Struktur können nicht gelöscht werden. Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
