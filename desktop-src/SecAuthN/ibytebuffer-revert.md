---
description: 'Die Revert-Methode verwirft alle Änderungen, die seit dem letzten ibytebuffer:: Commit-Befehl an einem transaktiven Datenstrom vorgenommen wurden.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Ibytebuffer:: Revert-Methode (scardssp. h)'
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
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214530"
---
# <a name="ibytebufferrevert-method"></a>Ibytebuffer:: Revert-Methode

\[Die **Revert** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **Revert** -Methode verwirft alle Änderungen, die seit dem letzten [**ibytebuffer:: Commit**](ibytebuffer-commit.md) -Befehl an einem transaktiven Datenstrom vorgenommen wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S \_ OK gibt an, dass der-Rückruf erfolgreich war und der Stream auf seine vorherige Version zurückgesetzt wurde.

## <a name="remarks"></a>Bemerkungen

Diese Methode verwirft Änderungen, die seit dem letzten Commitvorgang an einem transaktiven Datenstrom vorgenommen wurden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Zurücksetzen eines transaktiven Streams auf den Vorgang mit dem letzten Commit.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
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



 

