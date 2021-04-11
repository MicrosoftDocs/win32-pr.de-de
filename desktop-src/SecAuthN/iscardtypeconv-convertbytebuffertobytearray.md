---
description: Konvertiert einen universellen Puffer von Bytes (IStream-Objekt) in ein typisches C/C++-Bytearray.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'Iscardtypekonv:: convertbytebufferdebytearray-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217460"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a>Iscardtypekonv:: convertbytebufferdebytearray-Methode

\[Die **convertbytebuffertobytearray** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **convertbytebufferesbytearray** -Methode konvertiert einen universellen Puffer von Bytes (**IStream** -Objekt) in ein typisches C/C++-Bytearray.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbybuffer* \[ in\]
</dt> <dd>

Zeiger auf das **IStream** -Objekt, das konvertiert werden soll.

</dd> <dt>

*p-Ray* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Bytearray, das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Arbeitsspeicher wurde erfolgreich zugewiesen.<br/>                                                        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein Parameter vom Zeigertyp war falsch.<br/>                                            |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.<br/>                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardtypeconfiguration**](iscardtypeconv.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> </dl>

 

 
