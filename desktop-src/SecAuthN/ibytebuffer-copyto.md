---
description: Die CopyTo-Methode kopiert eine angegebene Anzahl von Bytes vom aktuellen Suchzeiger im -Objekt in den aktuellen Suchzeiger in einem anderen -Objekt.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: IByteBuffer::CopyTo-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4c4dc3861120d56dd5bff13fe1e77fd97e1fc32efed9622f18ee51b5160d1c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417640"
---
# <a name="ibytebuffercopyto-method"></a>IByteBuffer::CopyTo-Methode

\[Die **CopyTo-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **CopyTo-Methode** kopiert eine angegebene Anzahl von Bytes vom aktuellen Suchzeiger im -Objekt in den aktuellen Suchzeiger in einem anderen -Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pByteBuffer* \[ In\]
</dt> <dd>

Zeigt auf den Zielstream. Der Stream, auf den *pByteBuffer* zeigt, kann ein neuer Stream oder ein Klon des Quellstreams sein.

</dd> <dt>

*cb* \[ In\]
</dt> <dd>

Anzahl der Bytes, die aus dem Quellstream kopiert werden sollen.

</dd> <dt>

*read* \[ out\]
</dt> <dd>

Zeiger auf den Speicherort, an den diese Methode die tatsächliche Anzahl der aus der Quelle gelesenen Bytes schreibt. Sie können diesen Zeiger auf **NULL** festlegen, um anzugeben, dass Sie an diesem Wert nicht interessiert sind. In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der gelesenen Bytes bereit.

</dd> <dt>

*wwwwritten* \[ out\]
</dt> <dd>

Zeiger auf den Speicherort, an den diese Methode die tatsächliche Anzahl von Bytes schreibt, die in das Ziel geschrieben wurden. Sie können diesen Zeiger auf **NULL** festlegen, um anzugeben, dass Sie an diesem Wert nicht interessiert sind. In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der geschriebenen Bytes bereit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Diese Methode kopiert die angegebenen Bytes aus einem Stream in einen anderen. Sie kann auch verwendet werden, um einen Stream in sich selbst zu kopieren. Der Suchzeiger in jeder Streaminstanz wird für die Anzahl der gelesenen oder geschriebenen Bytes angepasst.

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



 

