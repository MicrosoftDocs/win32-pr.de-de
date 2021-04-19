---
description: Die Commit-Methode stellt sicher, dass alle Änderungen, die an einem im transaktiven Modus geöffneten Objekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'Ibytebuffer:: Commit-Methode (scardssp. h)'
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
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356945"
---
# <a name="ibytebuffercommit-method"></a>Ibytebuffer:: Commit-Methode

\[Die **Commit** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **Commit** -Methode stellt sicher, dass alle Änderungen, die an einem im transaktiven Modus geöffneten Objekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*GRF commitflags* \[ in\]
</dt> <dd>

Steuert, auf welche Weise ein Commit für die Änderungen am Streamobjekt ausgeführt wird. Eine Definition dieser Werte finden Sie in der stgc-Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Methode stellt sicher, dass Änderungen an einem im Transaktionsmodus geöffneten Datenstrom Objekt im übergeordneten Speicher widergespiegelt werden. Änderungen, die seit dem Öffnen oder letzten Commit an dem Stream vorgenommen wurden, werden in das übergeordnete Speicher Objekt übernommen. Wenn das übergeordnete Element im transaktiven Modus geöffnet wird, kann das übergeordnete Element immer noch zu einem späteren Zeitpunkt wieder hergestellt werden, um die Änderungen auf dieses Streamobjekt zurückzusetzen. Die Implementierung von Verbund Dateien unterstützt das Öffnen von Datenströmen im transaktiven Modus nicht. Daher hat diese Methode nur wenig Auswirkungen als das Leeren von Speicher Puffern.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das übernehmen von Änderungen am Speicher veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

