---
description: Erstellt ein typisches C/C++-Bytearray.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: ISCardTypeConv::CreateByteArray-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 297fc58d3a1457e48a16eb4330b11b506813eae23218484d3dbacce637f194c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013750"
---
# <a name="iscardtypeconvcreatebytearray-method"></a>ISCardTypeConv::CreateByteArray-Methode

\[Die **CreateByteArray-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **CreateByteArray-Methode** erstellt ein typisches C/C++-Bytearray.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwAllocSize* \[ In\]
</dt> <dd>

Größe (in Bytes) des Arbeitsspeichers, der für das Array zugeordnet werden soll.

</dd> <dt>

*ppbyArray* \[ out\]
</dt> <dd>

Zeiger auf das bytearray, das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Arbeitsspeicher erfolgreich zugeordnet.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Es liegt ein Fehler mit einem oder mehr parametern vor, die an die Funktion übergeben werden.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend freier Arbeitsspeicher zum Erfüllen der Anforderung.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Rufen Sie [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)auf, um einen universellen Bytepuffer zu erstellen, der einem **IStream-Objekt** [**(IByteBuffer)**](ibytebuffer.md)zugeordnet ist.

Rufen Sie [**CreateSafeArray**](iscardtypeconv-createsafearray.md)auf, um ein Automation SAFEARRAY mit Zeichen ohne Vorzeichen (Bytes) zu erstellen.

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
</dt> <dt>

[**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[**CreateSafeArray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
