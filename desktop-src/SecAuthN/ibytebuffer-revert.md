---
description: Die Revert-Methode verwirft alle Änderungen, die seit dem letzten IByteBuffer::Commit-Aufruf an einem transaktiven Stream vorgenommen wurden.
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: IByteBuffer::Revert-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 46e535560332c43d250b0a26183036342c8cca29144e3d2d1803582387af6bd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101260"
---
# <a name="ibytebufferrevert-method"></a>IByteBuffer::Revert-Methode

\[Die **Revert-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Revert-Methode** verwirft alle Änderungen, die seit dem letzten [**IByteBuffer::Commit-Aufruf**](ibytebuffer-commit.md) an einem transaktiven Stream vorgenommen wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war und der Stream auf die vorherige Version zurückgesetzt wurde.

## <a name="remarks"></a>Hinweise

Diese Methode verwirft Änderungen, die seit dem letzten Commitvorgang an einem transaktiven Stream vorgenommen wurden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie ein transaktiver Stream auf den Vorgang zurückgesetzt wird, für den zuletzt ein Commit ausgeführt wurde.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
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



 

