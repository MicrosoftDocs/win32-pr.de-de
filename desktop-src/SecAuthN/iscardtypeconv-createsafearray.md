---
description: Erstellt ein Automation SAFEARRAY-Zeichen ohne Vorzeichen (Bytes).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: ISCardTypeConv::CreateSafeArray-Methode (Hidddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 50b1adc227e651f3ce3b904389b57812cfb9dedee235f07057425880c0c8e32f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013740"
---
# <a name="iscardtypeconvcreatesafearray-method"></a>ISCardTypeConv::CreateSafeArray-Methode

\[Die **CreateSafeArray-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **CreateSafeArray-Methode** erstellt ein Automation SAFEARRAY mit Zeichen ohne Vorzeichen (Bytes).

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nAllocSize* \[ In\]
</dt> <dd>

Größe des Arbeitsspeichers in Bytes, der dem Array zugeordnet werden soll.

</dd> <dt>

*ppArray* \[ out\]
</dt> <dd>

Zeiger auf das SAFEARRAY-Objekt, das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Arbeitsspeicher wurde erfolgreich zugeordnet.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Es liegt ein Problem mit einem oder mehreren parametern vor, die an die Funktion übergeben werden.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend freier Arbeitsspeicher zum Erfüllen der Anforderung.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Um ein typisches C/C++-Bytearray zu erstellen, rufen [**Sie CreateByteArray**](iscardtypeconv-createbytearray.md)auf.

Um einen universellen Puffer von Bytes zu erstellen, der einem **IStream** [**(IByteBuffer**](ibytebuffer.md))-Objekt zugeordnet ist, rufen [**Sie CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)auf.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> <dt>

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
