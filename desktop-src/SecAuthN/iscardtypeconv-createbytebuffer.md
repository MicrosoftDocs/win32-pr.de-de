---
description: Erstellt einen universellen Puffer von Bytes, der einem IStream-Objekt (ibytebuffer) zugeordnet ist.
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'Iscardtypekonv:: up-ByteBuffer-Methode (scarddat. h)'
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
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042323"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a>Iscardtypekonv:: deatebytebuffer-Methode

\[Die Methode " **kreatebytebuffer** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Methode** "-Methode" erstellt einen universellen Puffer von Bytes, die einem **IStream** -Objekt ([**ibytebuffer**](ibytebuffer.md)) zugeordnet sind.

Der erstellte Byte Puffer ist ein Datenstrom, der über einem Speicherblock zugeordnet ist. Verwenden Sie die von der **IStream** -Schnittstelle bereitgestellten Methoden, um auf den Puffer zuzugreifen oder ihn zu verwalten. Ein eindeutiges Feature zu dieser Array Implementierung besteht darin, dass beim aufruft der **IStream:: Release** -Methode der zugrunde liegende Arbeitsspeicher für Sie freigegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwallocsize* \[ in\]
</dt> <dd>

Größe des Arbeitsspeichers in Bytes, der für das Array zugeordnet werden soll.

</dd> <dt>

*ppbybuff* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das IStream-Objekt, das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Arbeitsspeicher wurde erfolgreich zugewiesen.<br/>                                                        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Der zugewiesene Arbeitsspeicher ist beweglicher. Verwenden Sie die **IStream:: Release** -Methode, um den Arbeitsspeicher freizugeben.

Um ein typisches C/C++-Bytearray zu erstellen, rufen Sie " [**kreatebytearray**](iscardtypeconv-createbytearray.md)" auf.

Zum Erstellen eines Automation SafeArray mit nicht signierten Zeichen (Bytes) rufen Sie " [**kreatesafearray**](iscardtypeconv-createsafearray.md)" auf.

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
</dt> <dt>

[**"Kreatebytearray"**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**"Anatesafearray"**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
