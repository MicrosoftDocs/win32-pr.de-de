---
description: Erhält einen Bytezeiger auf den CABLOBAL-Speicherblock, der von der IStream-COM-Schnittstelle verwaltet wird.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: ISCardTypeConv::GetAtIStreamMemory-Methode (Ddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6520b9af0cf8f322045dfbe92ffc66ef624eadfa7b1beef0f528c6b299d1c2bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922399"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>ISCardTypeConv::GetAtIStreamMemory-Methode

\[Die **GetAtIStreamMemory-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **GetAtIStreamMemory-Methode** erhält einen Bytezeiger auf den CABLOBAL-Speicherblock, der von der **IStream-COM-Schnittstelle** verwaltet wird.

Dies ist eine Möglichkeit, den Arbeitsspeicher unter dem **IStream** abzurufen, ohne den sizeof-Wert für den Speicherblock in Bytes abzurufen und die Bytes mithilfe der **IStream-Schnittstelle** in ein temporäres Bytearray zu lesen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStrm* \[ In\]
</dt> <dd>

Ein Zeiger  auf die IStream-COM-Schnittstelle, die den HGLOBAL-Speicherblock verwaltet.

</dd> <dt>

*ppMem* \[ out\]
</dt> <dd>

Ein Zeiger auf das erste Byte des HGLOBAL-Speicherblocks, falls erfolgreich; andernfalls **NULL,** wenn der Vorgang fehlschlägt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Arbeitsspeicher wurde erfolgreich zugeordnet.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Es liegt ein Problem mit einem oder mehreren parametern vor, die an die Funktion übergeben werden.<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein Parameter vom Zeigertyp war falsch.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend freier Arbeitsspeicher zum Erfüllen der Anforderung.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Der **IStream-Verweiszähler** wird für jeden erworbenen *ppMem-Zeiger* erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Ddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv ist als 53B6AA63-3F56-11D0-916B-00AA00C18068 definiert.<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> </dl>

 

 
