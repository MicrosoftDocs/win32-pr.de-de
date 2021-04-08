---
description: Die SetSize-Methode ändert die Größe des Datenstrom Objekts.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'Ibytebuffer:: SetSize-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960544"
---
# <a name="ibytebuffersetsize-method"></a>Ibytebuffer:: SetSize-Methode

\[Die **SetSize** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **SetSize** -Methode ändert die Größe des Datenstrom Objekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*libnewsize* \[ in\]
</dt> <dd>

Neue Größe des Streams als Anzahl von Bytes

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Die **ibytebuffer:: SetSize** -Methode ändert die Größe des Datenstrom Objekts. Rufen Sie diese Methode auf, um Speicherplatz für den Stream vorab zuzuweisen. Wenn der *libnewsize* -Parameter größer als die aktuelle Streamgröße ist, wird der Datenstrom auf die für die Größe definierte Größe erweitert, indem der dazwischen liegende Bereich mit Bytes von undefiniertem Wert aufgefüllt wird. Dieser Vorgang ähnelt der [**ibytebuffer:: Write**](ibytebuffer-write.md) -Methode, wenn sich der Suchzeiger hinter dem aktuellen Streamende befindet.

Wenn der *libnewsize* -Parameter kleiner als der aktuelle Stream ist, wird der Stream auf die markierte Größe gekürzt.

Der Such Zeiger ist von der Änderung der Streamgröße nicht betroffen.

Der Aufruf von **ibytebuffer:: SetSize** kann eine effektive Methode sein, um einen großen Anteil von zusammenhängenden Speicherplatz zu erhalten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die Puffergröße festgelegt wird.


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
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



 

