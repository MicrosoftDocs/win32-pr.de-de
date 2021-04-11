---
description: Die Clone-Methode erstellt ein neues-Objekt mit einem eigenen Such Zeiger, der auf die gleichen Bytes wie das ursprüngliche ibytebuffer-Objekt verweist.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'Ibytebuffer:: Clone-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217334"
---
# <a name="ibytebufferclone-method"></a>Ibytebuffer:: Clone-Methode

\[Die **Klon** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **Clone** -Methode erstellt ein neues-Objekt mit einem eigenen Such Zeiger, der auf die gleichen Bytes wie das ursprüngliche [**ibytebuffer**](ibytebuffer.md) -Objekt verweist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppbytebuffer* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung verweist auf den Speicherort eines [**ibytebuffer**](ibytebuffer.md) -Zeigers auf das neue Streamobjekt. Wenn Sie den **ibytebuffer** -Zeiger nicht mehr verwenden, geben Sie ihn durch Aufrufen der [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Funktion frei. Wenn ein Fehler auftritt, ist dieser Parameter **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt ein neues Streamobjekt für den Zugriff auf die gleichen bytes, jedoch mit einem separaten Such Zeiger. Das neue Streamobjekt sieht die gleichen Daten wie das Quelldaten Strom Objekt. Änderungen, die in ein-Objekt geschrieben werden, sind direkt in der anderen sichtbar. Bereichs Sperren werden zwischen den Streamobjekten freigegeben.

Die anfängliche Einstellung des Such Zeigers in der geklonten Streaminstanz ist mit der aktuellen Einstellung des Such Zeigers im ursprünglichen Stream zum Zeitpunkt des Klon Vorgangs identisch.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Klonen der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle.


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
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



 

