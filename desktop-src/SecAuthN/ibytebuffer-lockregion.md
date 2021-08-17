---
description: Schränkt den Zugriff auf einen angegebenen Bytebereich im Pufferobjekt ein.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: IByteBuffer::LockRegion-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8575a568615a88552dd3907c7a5733c81dfe2d222661b4d8f9f82e32f0896ecf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482680"
---
# <a name="ibytebufferlockregion-method"></a>IByteBuffer::LockRegion-Methode

\[Die **LockRegion-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **LockRegion-Methode** schränkt den Zugriff auf einen angegebenen Bytebereich im Pufferobjekt ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*libOffset* \[ In\]
</dt> <dd>

Eine ganze Zahl, die den Byteoffset für den Anfang des Bereichs angibt.

</dd> <dt>

*cb* \[ In\]
</dt> <dd>

Eine ganze Zahl, die die Länge des Bereichs in Bytes angibt, der eingeschränkt werden soll.

</dd> <dt>

*dwLockType* \[ In\]
</dt> <dd>

Gibt die Einschränkungen an, die für den Zugriff auf den Bereich angefordert werden. Dies kann einer der Werte in der folgenden Tabelle sein.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**LOCK \_ WRITE**</dt> </dl>             | Der angegebene Bytebereich kann mehrmals geöffnet und gelesen werden. Das Schreiben in den gesperrten Bereich ist jedoch nicht zulässig, mit Ausnahme des Besitzers, dem diese Sperre gewährt wurde.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**LOCK \_ EXCLUSIVE**</dt> </dl> | Das Schreiben in den angegebenen Bytebereich ist mit Ausnahme des Besitzers, dem diese Sperre gewährt wurde, nicht zulässig.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**LOCK \_ ONLYONCE**</dt> </dl>    | Wenn diese Sperre gewährt wird, kann keine andere LOCK \_ ONLYONCE-Sperre für den Bereich erhalten werden. In der Regel ist dieser Sperrtyp ein Alias für einen anderen Sperrtyp. Daher können bestimmte Implementierungen über zusätzliches Verhalten verfügen, das diesem Sperrtyp zugeordnet ist.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Der Bytebereich kann sich über das aktuelle Ende des Streams erstrecken. Das Sperren über das Ende eines Streams hinaus ist als Kommunikationsmethode zwischen verschiedenen Instanzen des Streams nützlich, ohne Daten zu ändern, die tatsächlich Teil des Streams sind.

Es können drei Arten von Sperren unterstützt werden: Sperren, um andere Writer auszuschließen, Sperren zum Ausschließen anderer Reader oder Writer und Sperren, die es nur einem Anfordernden ermöglichen, eine Sperre für den angegebenen Bereich zu erhalten. Dies ist normalerweise ein Alias für einen der beiden anderen Sperrtypen. Eine bestimmte Streaminstanz unterstützt möglicherweise einen der ersten beiden Typen oder beide. Der Sperrtyp wird von *dwLockType* mithilfe eines Werts aus der [**LOCKTYPE-Enumeration**](/windows/win32/api/objidl/ne-objidl-locktype) angegeben.

Alle mit **LockRegion** gesperrten Regionen müssen später explizit entsperrt werden, indem [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) mit genau denselben Werten für die *Parameter libOffset,* *cb* und *dwLockTypegesperrt* wird. Der Bereich muss entsperrt werden, bevor der Stream freigegeben wird. Zwei angrenzende Regionen können nicht separat gesperrt und dann mit einem einzigen Entsperrungsaufruf entsperrt werden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie der Zugriff auf einen Bytebereich eingeschränkt wird.


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

