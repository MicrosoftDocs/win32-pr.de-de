---
description: Die Commit-Methode stellt sicher, dass alle Änderungen, die an einem im Transaktionsmodus geöffneten Objekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: IByteBuffer::Commit-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: af165e6f0a805532eade820dcb67968a77186cee3f90cfc48a240d387b1f31b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127410"
---
# <a name="ibytebuffercommit-method"></a>IByteBuffer::Commit-Methode

\[Die **Commit-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Commit-Methode** stellt sicher, dass alle Änderungen, die an einem im Transaktionsmodus geöffneten Objekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*grfCommitFlags* \[ In\]
</dt> <dd>

Steuert, auf welche Weise ein Commit für die Änderungen am Streamobjekt ausgeführt wird. Eine Definition dieser Werte finden Sie in der STGC-Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Mit dieser Methode wird sichergestellt, dass Änderungen an einem Im Transaktionsmodus geöffneten Streamobjekt im übergeordneten Speicher widergespiegelt werden. Änderungen, die seit dem Öffnen oder letzten Commit am Stream vorgenommen wurden, werden im übergeordneten Speicherobjekt widergespiegelt. Wenn das übergeordnete Element im Transaktionsmodus geöffnet wird, kann das übergeordnete Element zu einem späteren Zeitpunkt ein Rollback der Änderungen an diesem Streamobjekt ausführen. Die Implementierung der Verbunddatei unterstützt das Öffnen von Datenströmen im Transaktionsmodus nicht. Daher hat diese Methode nur sehr geringe Auswirkungen als das Leeren von Speicherpuffern.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Committen von Änderungen an den Speicher.


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
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



 

