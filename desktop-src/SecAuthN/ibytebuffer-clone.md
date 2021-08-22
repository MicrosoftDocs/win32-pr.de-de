---
description: Die Clone-Methode erstellt ein neues -Objekt mit einem eigenen Suchzeiger, der auf die gleichen Bytes wie das ursprüngliche IByteBuffer-Objekt verweist.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: IByteBuffer::Clone-Methode (Scardssp.h)
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
ms.openlocfilehash: fae7fbe32b18a81557200b5c5519092bb2edd84290d9909cf884308a9173aac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417680"
---
# <a name="ibytebufferclone-method"></a>IByteBuffer::Clone-Methode

\[Die **Clone-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Clone-Methode** erstellt ein neues -Objekt mit einem eigenen Suchzeiger, der auf die gleichen Bytes wie das ursprüngliche [**IByteBuffer-Objekt**](ibytebuffer.md) verweist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppByteBuffer* \[ out\]
</dt> <dd>

Bei erfolgreicher Verarbeitung zeigt auf den Speicherort eines [**IByteBuffer-Zeigers**](ibytebuffer.md) auf das neue Streamobjekt. Wenn Sie die Verwendung des **IByteBuffer-Zeigers** abgeschlossen haben, geben Sie ihn frei, indem Sie die [**IUnknown::Release-Funktion**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufrufen. Wenn ein Fehler auftritt, ist dieser Parameter **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Diese Methode erstellt ein neues Streamobjekt für den Zugriff auf die gleichen Bytes, aber mit einem separaten Suchzeiger. Das neue Streamobjekt sieht die gleichen Daten wie das Quellstreamobjekt. Änderungen, die in ein Objekt geschrieben werden, sind sofort im anderen sichtbar. Bereichssperren werden von den Streamobjekten gemeinsam genutzt.

Die anfängliche Einstellung des Suchzeigers in der geklonten Streaminstanz ist mit der aktuellen Einstellung des Suchzeigers im ursprünglichen Stream zum Zeitpunkt des Klonvorgang identisch.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Klonen der [**IByteBuffer-Schnittstelle.**](ibytebuffer.md)


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

