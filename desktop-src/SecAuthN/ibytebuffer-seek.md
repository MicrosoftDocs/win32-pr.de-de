---
description: Die Seek-Methode ändert den Suchzeiger auf eine neue Position relativ zum Anfang des Puffers, zum Ende des Puffers oder zum aktuellen Suchzeiger.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: IByteBuffer::Seek-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 70c4af327fad5014c5d6dec80dd29441f51a03639a108249991c83f53e5d2be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016250"
---
# <a name="ibytebufferseek-method"></a>IByteBuffer::Seek-Methode

\[Die **Seek-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Seek-Methode** ändert den Suchzeiger auf eine neue Position relativ zum Anfang des Puffers, zum Ende des Puffers oder zum aktuellen Suchzeiger.

## <a name="syntax"></a>Syntax


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dlibMove* \[ In\]
</dt> <dd>

Verschiebung, die dem von *dwOrigin* angegebenen Speicherort hinzugefügt werden soll. Wenn *dwOrigin* STREAM \_ SEEK SET \_ ist, wird dies als Wert ohne Vorzeichen und nicht als signiert interpretiert.

</dd> <dt>

*dwOrigin* \[ In\]
</dt> <dd>

Gibt den Ursprung für die verschiebung an, die in *dlibMove* angegeben ist. Der Ursprung kann einer der Werte in der folgenden Tabelle sein.



| Wert                                                                                                                                                                | Bedeutung                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**STREAM \_ SEEK \_ SET**</dt> </dl> | Der neue Suchzeiger ist ein Offset relativ zum Anfang des Streams. In diesem Fall ist der *dlibMove-Parameter* die neue Suchposition relativ zum Anfang des Streams.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**STREAM \_ SEEK \_ CUR**</dt> </dl> | Der neue Suchzeiger ist ein Offset relativ zur aktuellen Position des Suchzeigers. In diesem Fall ist der *dlibMove-Parameter* die signierte Verschiebung von der aktuellen Suchposition.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**STREAM \_ SEEK \_ END**</dt> </dl> | Der neue Suchzeiger ist ein Offset relativ zum Ende des Streams. In diesem Fall ist der *dlibMove-Parameter* die neue Suchposition relativ zum Ende des Streams.<br/>             |



 

</dd> <dt>

*plibNewPosition* \[ out\]
</dt> <dd>

Zeiger auf die Position, an der diese Methode den Wert des neuen Suchzeigers vom Anfang des Streams schreibt. Sie können diesen Zeiger auf **NULL** festlegen, um anzugeben, dass Sie an diesem Wert nicht interessiert sind. In diesem Fall stellt diese Methode den neuen Suchzeiger nicht bereit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Die **Seek-Methode** ändert den Suchzeiger, sodass nachfolgende Lese- und Schreibvorgänge an einer anderen Position im Streamobjekt erfolgen können. Es ist ein Fehler, der vor dem Anfang des Streams gesucht werden soll. Es ist jedoch kein Fehler, nach dem Ende des Streams zu suchen. Das Suchen über das Ende des Streams hinaus ist für nachfolgende Schreibvorgänge nützlich, da der Stream zu diesem Zeitpunkt auf die Suchposition unmittelbar vor Abschluss des Schreibvorgangs erweitert wird.

Sie können diese Methode auch verwenden, um den aktuellen Wert des Suchzeigers abzurufen, indem Sie diese Methode aufrufen, wobei der *dwOrigin-Parameter* auf STREAM \_ SEEK CUR und der \_ *dlibMove-Parameter* auf 0 (null) festgelegt sind, damit der Suchzeiger nicht geändert wird. Der aktuelle Suchzeiger wird im *plibNewPosition-Parameter* zurückgegeben.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Positionierung des Suchzeigers auf eine neue Position.


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
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



 

