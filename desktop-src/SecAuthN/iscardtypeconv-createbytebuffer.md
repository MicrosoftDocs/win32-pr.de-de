---
description: Erstellt einen universellen Puffer von Bytes, die einem IStream-Objekt (IByteBuffer) zugeordnet sind.
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: ISCardTypeConv::CreateByteBuffer-Methode (Ddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e95ab8989027cb79dfd48720b08d27042c7bd8f9252d1438152dafbae017d762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922409"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a>ISCardTypeConv::CreateByteBuffer-Methode

\[Die **CreateByteBuffer-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **CreateByteBuffer-Methode** erstellt einen universellen Puffer von Bytes, die einem **IStream** -Objekt ([**IByteBuffer**](ibytebuffer.md)) zugeordnet sind.

Der erstellte Bytepuffer ist ein Stream, der einem Speicherblock zugeordnet ist. Verwenden Sie die von der **IStream-Schnittstelle** bereitgestellten Methoden, um auf den Puffer zuzugreifen oder diesen zu verwalten. Ein einzigartiges Feature dieser Arrayimplementierungen ist, dass beim Aufrufen der **IStream::Release-Methode** der zugrunde liegende Arbeitsspeicher für Sie freigegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwAllocSize* \[ In\]
</dt> <dd>

Größe des Arbeitsspeichers in Bytes, der dem Array zugeordnet werden soll.

</dd> <dt>

*ppbyBuff* \[ out\]
</dt> <dd>

Zeiger auf das IStream-Objekt, das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Arbeitsspeicher wurde erfolgreich zugeordnet.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Es liegt ein Problem mit einem oder mehreren parametern vor, die an die Funktion übergeben werden.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend freier Arbeitsspeicher zum Erfüllen der Anforderung.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Der zugeordnete Arbeitsspeicher ist verschiebbar. Verwenden Sie die **IStream::Release-Methode,** um den Arbeitsspeicher freizugeben.

Um ein typisches C/C++-Bytearray zu erstellen, rufen [**Sie CreateByteArray**](iscardtypeconv-createbytearray.md)auf.

Rufen [**Sie CreateSafeArray**](iscardtypeconv-createsafearray.md)auf, um ein Automation SAFEARRAY-Zeichen ohne Vorzeichen (Bytes) zu erstellen.

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
</dt> <dt>

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**CreateSafeArray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
