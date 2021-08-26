---
description: Konvertiert ein typisches C/C++-Bytearray in einen universellen Bytepuffer (IStream-Objekt).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: ISCardTypeConv::ConvertByteArrayToByteBuffer-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 5616dc56ac893d6298e12014f3ee31d38bf1c55fb5367f354bf97da704ade0c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013810"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>ISCardTypeConv::ConvertByteArrayToByteBuffer-Methode

\[Die **ConvertByteArrayToByteBuffer-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ConvertByteArrayToByteBuffer-Methode** konvertiert ein typisches C/C++-Bytearray in einen universellen Bytepuffer **(IStream-Objekt).**

Der erstellte Bytepuffer ist ein Stream, der einem Speicherblock zugeordnet ist. Um auf den Puffer zu zugreifen oder diesen zu verwalten, verwenden Sie die methoden, die von der **IStream-Schnittstelle bereitgestellt** werden. Ein einzigartiges Feature dieser Arrayimplementierung ist, dass beim Aufrufen der **IStream::Release-Methode** der zugrunde liegende Arbeitsspeicher für Sie freigegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbyArray* \[ In\]
</dt> <dd>

Zeiger auf das zu konvertierte Bytearray.

</dd> <dt>

*dwArraySize* \[ In\]
</dt> <dd>

Größe des zu konvertierten Bytearrays.

</dd> <dt>

*ppbyBuffer* \[ out\]
</dt> <dd>

Zeiger auf das **IStream-Objekt,** das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Arbeitsspeicher erfolgreich zugeordnet.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Es liegt ein Fehler mit einem oder mehr parametern vor, die an die Funktion übergeben werden.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein Parameter vom Zeigertyp war falsch.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Der zugeordnete Arbeitsspeicher ist verschiebbar. Verwenden Sie die **IStream::Release-Methode,** um den Arbeitsspeicher frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv ist als 53B6AA63-3F56-11D0-916B-00AA00C18068 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> </dl>

 

 
