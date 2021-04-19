---
description: Mit der Initialize-Methode wird das ibytebuffer-Objekt für die Verwendung vorbereitet. Diese Methode muss aufgerufen werden, bevor andere Methoden in der ibytebuffer-Schnittstelle aufgerufen werden.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Ibytebuffer:: Initialize-Methode (scardssp. h)'
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
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364185"
---
# <a name="ibytebufferinitialize-method"></a>Ibytebuffer:: Initialize-Methode

\[Die **Initialize** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Mit der **Initialize** -Methode wird das [**ibytebuffer**](ibytebuffer.md) -Objekt für die Verwendung vorbereitet. Diese Methode muss aufgerufen werden, bevor andere Methoden in der **ibytebuffer** -Schnittstelle aufgerufen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LSIZE* \[ in\]
</dt> <dd>

Anfängliche Größe (in Bytes) der Daten, die der Stream enthalten soll.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Wenn nicht **null**, werden die anfänglichen Daten in den Stream geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen neuen [**ibytebuffer**](ibytebuffer.md) -Stream verwenden, wird diese Methode aufgerufen, bevor eine der anderen **ibytebuffer** -Methoden verwendet wird.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Initialisierung des [**ibytebuffer**](ibytebuffer.md) -Objekts.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

