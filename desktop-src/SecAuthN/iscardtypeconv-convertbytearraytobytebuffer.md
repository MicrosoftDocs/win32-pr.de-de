---
description: Konvertiert ein typisches C/C++-Bytearray in einen universellen Puffer von Bytes (IStream-Objekt).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'Iscardtypekonv:: convertbytearraydebytebuffer-Methode (scarddat. h)'
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
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867839"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>Iscardtypekonv:: convertbytearraydebytebuffer-Methode

\[Die **convertbytearraytobytebuffer** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **convertbytearrayesbytebuffer** -Methode konvertiert ein typisches C/C++-Bytearray in einen universellen Puffer von Bytes (**IStream** -Objekt).

Der erstellte Byte Puffer ist ein Datenstrom, der über einem Speicherblock zugeordnet ist. Verwenden Sie die von der **IStream** -Schnittstelle bereitgestellten Methoden, um auf den Puffer zuzugreifen oder ihn zu verwalten. Ein eindeutiges Feature zu dieser Array Implementierung besteht darin, dass beim aufruft der **IStream:: Release** -Methode der zugrunde liegende Arbeitsspeicher für Sie freigegeben wird.

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

*pbyarray* \[ in\]
</dt> <dd>

Zeiger auf das Bytearray, das konvertiert werden soll.

</dd> <dt>

*dwarraysize* \[ in\]
</dt> <dd>

Größe des Byte Arrays, das konvertiert werden soll.

</dd> <dt>

*ppbybuffer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das **IStream** -Objekt, das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Arbeitsspeicher wurde erfolgreich zugewiesen.<br/>                                                        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein Parameter vom Zeigertyp war falsch.<br/>                                            |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Der zugewiesene Arbeitsspeicher ist beweglicher. Verwenden Sie die **IStream:: Release** -Methode, um den Arbeitsspeicher freizugeben.

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

 

 
