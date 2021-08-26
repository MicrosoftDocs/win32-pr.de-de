---
description: Die Write-Methode schreibt eine angegebene Zahl aus Bytes ab dem aktuellen Suchzeiger in das Streamobjekt.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: IByteBuffer::Write-Methode (Scardssp.h)
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
ms.openlocfilehash: 0033d4f4ee03629d2bedf9f232a43607100bcdca8bfaab457c2236bbfad603d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127350"
---
# <a name="ibytebufferwrite-method"></a>IByteBuffer::Write-Methode

\[Die **Write-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Write-Methode** schreibt eine angegebene Zahl aus Bytes ab dem aktuellen Suchzeiger in das Streamobjekt.

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

*pByte* \[ In\]
</dt> <dd>

Adresse des Puffers, der die Daten enthält, die in den Stream geschrieben werden sollen. Ein gültiger Zeiger muss für diesen Parameter bereitgestellt werden, auch wenn *cb* 0 (null) ist.

</dd> <dt>

*cb* \[ In\]
</dt> <dd>

Anzahl der Datenbytes, die in den Stream geschrieben werden sollen. Dieser Parameter kann 0 (null) sein.

</dd> <dt>

*wwwwritten* \[ out\]
</dt> <dd>

Adresse einer **LONG-Variablen,** in die diese Methode die tatsächliche Anzahl von Bytes schreibt, die in das Streamobjekt geschrieben wurden. Der Aufrufer kann diesen Zeiger auf **NULL** festlegen. In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der geschriebenen Bytes bereit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Die **IByteBuffer::Write-Methode** schreibt die angegebenen Daten in ein Streamobjekt. Der Suchzeiger wird für die Anzahl der tatsächlich geschriebenen Bytes angepasst. Die Anzahl der tatsächlich geschriebenen Bytes wird im *parameter pwwritten* zurückgegeben. Wenn die Byteanzahl 0 Bytes beträgt, hat der Schreibvorgang keine Auswirkungen.

Wenn sich der Suchzeiger derzeit hinter dem Ende des Streams befindet und die Byteanzahl ungleich 0 (null) ist, erhöht diese Methode die Größe des Streams auf den Suchzeiger und schreibt die angegebenen Bytes beginnend beim Suchzeiger. Die in den Stream geschriebenen Füllbytes werden nicht mit einem bestimmten Wert initialisiert. Dies entspricht dem Verhalten am Ende der Datei im MS-DOS FAT-Dateisystem.

Mit einer Byteanzahl von 0 (null) und einem Suchzeiger hinter dem Ende des Streams erstellt diese Methode nicht die Füllbytes, um den Stream auf den Suchzeiger zu erhöhen. In diesem Fall müssen Sie die [**IByteBuffer::SetSize-Methode**](ibytebuffer-setsize.md) aufrufen, um die Größe des Streams zu erhöhen und die Füllbytes zu schreiben.

Der *Parameter "layoutWritten"* kann auch dann einen Wert aufweisen, wenn ein Fehler auftritt.

In der von COM bereitgestellten Implementierung sind Streamobjekte nicht sparse. Alle Füllbytes werden schließlich auf dem Datenträger zugeordnet und dem Stream zugewiesen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Schreiben von Bytes in das Streamobjekt.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

