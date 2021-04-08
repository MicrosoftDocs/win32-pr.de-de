---
description: 'Entfernt die Zugriffsbeschränkung für einen Bereich von Bytes, der zuvor mithilfe von ibytebuffer:: LockRegion eingeschränkt wurde.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Ibytebuffer:: UnlockRegion-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960543"
---
# <a name="ibytebufferunlockregion-method"></a>Ibytebuffer:: UnlockRegion-Methode

\[Die **UnlockRegion** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **UnlockRegion** -Methode entfernt die Zugriffsbeschränkung für einen Bereich von Bytes, der zuvor mithilfe von [**ibytebuffer:: LockRegion**](ibytebuffer-lockregion.md)eingeschränkt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*liboffset* \[ in\]
</dt> <dd>

Der Byte Offset für den Anfang des Bereichs.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Länge (in Byte) des Bereichs, der eingeschränkt werden soll.

</dd> <dt>

*dwLockType* \[ in\]
</dt> <dd>

Zugriffs Einschränkungen, die zuvor auf den Bereich gesetzt wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Die **ibytebuffer:: UnlockRegion** -Methode entsperrt einen zuvor gesperrten Bereich mithilfe der [**ibytebuffer:: LockRegion**](ibytebuffer-lockregion.md) -Methode. Gesperrte Bereiche müssen später explizit entsperrt werden, indem **ibytebuffer:: UnlockRegion** mit exakt denselben Werten für die Parameter *liboffset*, *CB* und *dwLockType* aufgerufen wird. Die Region muss entsperrt werden, bevor der Stream freigegeben wird. Zwei angrenzende Regionen können nicht separat gesperrt und dann mit einem einzigen Unlock-Befehl entsperrt werden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie ein Bereich von Bytes entsperrt wird.


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
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



 

