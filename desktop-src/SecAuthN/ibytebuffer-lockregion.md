---
description: Schränkt den Zugriff auf einen angegebenen Bereich von Bytes im Buffer-Objekt ein.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'Ibytebuffer:: LockRegion-Methode (scardssp. h)'
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
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217776"
---
# <a name="ibytebufferlockregion-method"></a>Ibytebuffer:: LockRegion-Methode

\[Die **LockRegion** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **LockRegion** -Methode schränkt den Zugriff auf einen angegebenen Bereich von Bytes im Buffer-Objekt ein.

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

*liboffset* \[ in\]
</dt> <dd>

Eine ganze Zahl, die den Byte Offset für den Anfang des Bereichs angibt.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Eine ganze Zahl, die die Länge des Bereichs (in Bytes) angibt, der eingeschränkt werden soll.

</dd> <dt>

*dwLockType* \[ in\]
</dt> <dd>

Gibt die Einschränkungen an, die beim Zugriff auf den Bereich angefordert werden. Dies kann einer der Werte in der folgenden Tabelle sein.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**Sperr \_ Schreibvorgang**</dt> </dl>             | Der angegebene Bereich von Bytes kann beliebig oft geöffnet und gelesen werden, aber das Schreiben in den gesperrten Bereich ist mit Ausnahme des Besitzers, dem diese Sperre erteilt wurde, nicht zulässig.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**\_exklusiv sperren**</dt> </dl> | Das Schreiben in den angegebenen Byte Bereich ist mit Ausnahme des Besitzers, dem diese Sperre erteilt wurde, nicht zulässig.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**\_onlyonce Sperren**</dt> </dl>    | Wenn diese Sperre erteilt wird, kann keine andere Lock \_ onlyonce-Sperre für den Bereich abgerufen werden. In der Regel handelt es sich bei diesem Sperrentyp um einen Alias für einen anderen Sperrentyp. Folglich können bestimmte Implementierungen über zusätzliches Verhalten verfügen, das diesem Sperrentyp zugeordnet ist.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Der Byte Bereich kann nach dem aktuellen Ende des Streams erweitert werden. Das Sperren über das Ende eines Datenstroms hinaus ist als Kommunikationsmethode zwischen verschiedenen Instanzen des Streams nützlich, ohne dass Daten geändert werden, die tatsächlich Teil des Streams sind.

Es können drei Arten von Sperren unterstützt werden: Sperren, um andere Writer auszuschließen, sperren, um andere Reader oder Writer auszuschließen, und sperren, die nur einem Anforderer erlauben, eine Sperre für den angegebenen Bereich zu erhalten, was normalerweise ein Alias für einen der beiden anderen Sperr Typen ist. Eine angegebene Datenstrom Instanz unterstützt möglicherweise einen der beiden ersten Typen oder beides. Der Sperrentyp wird von *dwLockType* mit einem Wert aus der [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) -Enumeration angegeben.

Alle mit **LockRegion** gesperrten Bereiche müssen später explizit entsperrt werden, indem [**ibytebuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) mit exakt denselben Werten für die Parameter *liboffset*, *CB* und *dwLockType* aufgerufen wird. Die Region muss entsperrt werden, bevor der Stream freigegeben wird. Zwei angrenzende Regionen können nicht separat gesperrt und dann mit einem einzigen Unlock-Befehl entsperrt werden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie der Zugriff auf einen Bereich von Bytes beschränkt wird.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

