---
description: Entfernt die Zugriffseinschränkung für einen Bereich von Bytes, der zuvor mit IByteBuffer::LockRegion eingeschränkt wurde.
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: IByteBuffer::UnlockRegion-Methode (Scardssp.h)
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
ms.openlocfilehash: 798569621c1a46e73ea6fd8e2f4f3333c3a0cbcef32618797fcba39d35b55bf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127390"
---
# <a name="ibytebufferunlockregion-method"></a>IByteBuffer::UnlockRegion-Methode

\[Die **UnlockRegion-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **UnlockRegion-Methode** entfernt die Zugriffseinschränkung für einen Bereich von Bytes, der zuvor mit [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md)eingeschränkt wurde.

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

*libOffset* \[ In\]
</dt> <dd>

Byteoffset für den Anfang des Bereichs.

</dd> <dt>

*cb* \[ In\]
</dt> <dd>

Länge des zu beschränkenden Bereichs in Bytes.

</dd> <dt>

*dwLockType* \[ In\]
</dt> <dd>

Zugriffseinschränkungen, die zuvor für den Bereich gelten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Die **IByteBuffer::UnlockRegion-Methode** entsperrt eine Region, die zuvor mithilfe der [**IByteBuffer::LockRegion-Methode**](ibytebuffer-lockregion.md) gesperrt wurde. Gesperrte Bereiche müssen später explizit entsperrt werden, indem **IByteBuffer::UnlockRegion** mit genau den gleichen Werten für die Parameter *libOffset,* *cb* und *dwLockType* aufgerufen wird. Die Region muss entsperrt werden, bevor der Stream freigegeben wird. Zwei angrenzende Regionen können nicht separat gesperrt und dann mit einem einzigen Entsperraufruf entsperrt werden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Entsperren eines Bytebereichs.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

