---
description: Bestimmt die Größe der IStream-COM-Schnittstelle in Bytes.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: ISCardTypeConv::SizeOfIStream-Methode (Ddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ec150fdf5a6f296b5728131cd59bb6863016fe46fe0769e6159e43b236f77a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013690"
---
# <a name="iscardtypeconvsizeofistream-method"></a>ISCardTypeConv::SizeOfIStream-Methode

\[Die **SizeOfIStream-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **SizeOfIStream-Methode** bestimmt die Größe der **IStream-COM-Schnittstelle** in Bytes.

## <a name="syntax"></a>Syntax


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStrm* \[ In\]
</dt> <dd>

Ein Zeiger  auf die IStream-COM-Schnittstelle.

</dd> <dt>

*ppersonalisierungSize* \[ out\]
</dt> <dd>

Ein Zeiger auf die große ganze Zahl ohne Vorzeichen, die den  gesamten 64-Bit-Sizeof-Wert der IStream-COM-Schnittstelle enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion war erfolgreich, und *\* p msiSize* entspricht der Größe der IStream-COM-Schnittstelle in Bytes.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Es ist ein nicht angegebener Fehler aufgetreten.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *Parameter p msiSize* ist falsch.<br/>                                                       |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | Der *pStrm-Parameter* ist falsch.<br/>                                                          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Unerwarteter Fehler.<br/>                                                                   |



 

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
</dt> </dl>

 

 
