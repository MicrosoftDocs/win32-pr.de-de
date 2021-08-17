---
description: Gibt den Bytezeiger frei, der auf den HGLOBAL-Speicherblock, der von einer IStream COM-Schnittstelle verwaltet wird, zeigen.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: ISCardTypeConv::FreeIStreamMemoryPtr-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 62e91f9d8fca06c812370091b407edb73fed433a4c576857a7e089db28d6d856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922389"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a>ISCardTypeConv::FreeIStreamMemoryPtr-Methode

\[Die **FreeIStreamMemoryPtr-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **FreeIStreamMemoryPtr-Methode** gibt den Bytezeiger frei, der auf den HGLOBAL-Speicherblock, der von einer **IStream** COM-Schnittstelle verwaltet wird, verweisen.

## <a name="syntax"></a>Syntax


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStrm* \[ In\]
</dt> <dd>

Zeiger auf die **IStream-Schnittstelle,** die den Speicherblock verwaltet, auf den *pMem zeigt.*

</dd> <dt>

*pMem* \[ In\]
</dt> <dd>

Zeiger auf den Speicherblock, der von der **IStream-Schnittstelle verwaltet** wird.

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

Diese Funktion gibt den Bytezeiger, der auf den von der **IStream-Schnittstelle** verwalteten HGLOBAL-Speicherblockzeigt, vollständig und sauber frei. Der Bytezeiger wird durch einen Aufruf von [**GetAtIStreamMemory erworben.**](iscardtypeconv-getatistreammemory.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> <dt>

[**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
