---
description: Die Write-Methode schreibt eine angegebene Anzahl von Bytes in das Streamobjekt, beginnend beim aktuellen Such Zeiger.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'Ibytebuffer:: Write-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867868"
---
# <a name="ibytebufferwrite-method"></a>Ibytebuffer:: Write-Methode

\[Die **Write** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **Write** -Methode schreibt eine angegebene Anzahl von Bytes in das Streamobjekt, beginnend beim aktuellen Such Zeiger.

## <a name="syntax"></a>Syntax


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PBYTE* \[ in\]
</dt> <dd>

Adresse des Puffers, der die Daten enthält, die in den Stream geschrieben werden sollen. Für diesen Parameter muss ein gültiger Zeiger angegeben werden, auch wenn *CB* NULL ist.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Anzahl der Daten bytes, die in den Stream geschrieben werden sollen. Dieser Parameter kann NULL sein.

</dd> <dt>

*pcbwritten* \[ vorgenommen\]
</dt> <dd>

Adresse einer **langen** Variablen, bei der diese Methode die tatsächliche Anzahl von Bytes schreibt, die in das Datenstrom Objekt geschrieben wurden. Der Aufrufer kann diesen Zeiger auf **null** festlegen. in diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der geschriebenen Bytes bereit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Die **ibytebuffer:: Write** -Methode schreibt die angegebenen Daten in ein Datenstrom Objekt. Der Seek-Zeiger wird für die Anzahl der tatsächlich geschriebenen Bytes angepasst. Die Anzahl der tatsächlich geschriebenen Bytes wird im *pcbwritten* -Parameter zurückgegeben. Wenn die Byte Anzahl 0 Bytes beträgt, hat der Schreibvorgang keine Auswirkung.

Wenn sich der Suchzeiger momentan hinter dem Ende des Streams befindet und die Byte Anzahl ungleich NULL ist, erhöht diese Methode die Größe des Streams auf den Such Zeiger und schreibt die angegebenen Bytes beginnend beim Such Zeiger. Die in den Stream geschriebenen Füll Bytes werden nicht mit einem bestimmten Wert initialisiert. Dies entspricht dem dateiendeverhalten im DOS-FAT-Dateisystem.

Mit einer Byte Anzahl von 0 (null) und einem Such Zeiger hinter das Ende des Streams erstellt diese Methode nicht die Füll bytes, um den Stream auf den Such Zeiger zu vergrößern. In diesem Fall müssen Sie die [**ibytebuffer:: SetSize**](ibytebuffer-setsize.md) -Methode aufrufen, um die Größe des Streams zu vergrößern und die Füll Bytes zu schreiben.

Der *pcbwritten* -Parameter kann auch dann einen Wert aufweisen, wenn ein Fehler auftritt.

In der von com bereitgestellten Implementierung sind Streamobjekte nicht sparsam. Alle Füll Bytes werden schließlich auf dem Datenträger zugeordnet und dem Stream zugewiesen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Schreiben von Bytes in das Stream-Objekt.


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
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



 

