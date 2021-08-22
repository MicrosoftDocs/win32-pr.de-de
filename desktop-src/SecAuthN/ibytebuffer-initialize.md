---
description: Die Initialize-Methode bereitet das IByteBuffer-Objekt für die Verwendung vor. Diese Methode muss aufgerufen werden, bevor andere Methoden in der IByteBuffer-Schnittstelle aufgerufen werden.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: IByteBuffer::Initialize-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28a525b26d49dd5df8a2be3ba6a5af5a16459c26e191368badae34ca381488e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417630"
---
# <a name="ibytebufferinitialize-method"></a>IByteBuffer::Initialize-Methode

\[Die **Initialize-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Initialize-Methode** bereitet das [**IByteBuffer-Objekt**](ibytebuffer.md) für die Verwendung vor. Diese Methode muss aufgerufen werden, bevor andere Methoden in der **IByteBuffer-Schnittstelle** aufgerufen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lSize* \[ In\]
</dt> <dd>

Die Anfangsgröße der Daten, die der Stream enthalten soll, in Bytes.

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Wenn nicht **NULL,** die anfänglichen Daten, die in den Stream geschrieben werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Wenn Sie einen neuen [**IByteBuffer-Stream**](ibytebuffer.md) verwenden, rufen Sie diese Methode auf, bevor Sie eine der anderen **IByteBuffer-Methoden** verwenden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Initialisierung des [**IByteBuffer-Objekts.**](ibytebuffer.md)


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

