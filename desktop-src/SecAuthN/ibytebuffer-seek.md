---
description: Die Seek-Methode ändert den Such Zeiger an eine neue Position relativ zum Anfang des Puffers, bis zum Ende des Puffers oder zum aktuellen Such Zeiger.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'Ibytebuffer:: Seek-Methode (scardssp. h)'
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
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867871"
---
# <a name="ibytebufferseek-method"></a>Ibytebuffer:: Seek-Methode

\[Die **Seek** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **Seek** -Methode ändert den Such Zeiger an eine neue Position relativ zum Anfang des Puffers, bis zum Ende des Puffers oder zum aktuellen Such Zeiger.

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

*dlibmove* \[ in\]
</dt> <dd>

Die Verschiebung, die dem durch *dwOrigin* festgelegten Speicherort hinzugefügt werden soll. Wenn *dwOrigin* für Stream \_ Seek \_ festgelegt ist, wird dies als unsignierter Wert und nicht als signiert interpretiert.

</dd> <dt>

*dwOrigin* \[ in\]
</dt> <dd>

Gibt den Ursprung der in *dlibmove* angegebenen Verschiebung an. Der Ursprung kann einer der Werte in der folgenden Tabelle sein.



| Wert                                                                                                                                                                | Bedeutung                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**Stream \_ - \_ Suchsatz**</dt> </dl> | Der neue Seek-Zeiger ist ein Offset relativ zum Anfang des Streams. In diesem Fall ist der *dlibmove* -Parameter die neue Suchposition relativ zum Anfang des Streams.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**Stream \_ Seek \_ cur**</dt> </dl> | Der neue Seek-Zeiger ist ein Offset relativ zum aktuellen suchzeigerort. In diesem Fall ist der *dlibmove* -Parameter die signierte Verschiebung von der aktuellen Suchposition.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**\_ \_ streamsuchende**</dt> </dl> | Der neue Seek-Zeiger ist ein Offset relativ zum Ende des Streams. In diesem Fall ist der *dlibmove* -Parameter die neue Suchposition relativ zum Ende des Streams.<br/>             |



 

</dd> <dt>

*plibnewposition* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Speicherort, an dem diese Methode den Wert des neuen Such Zeigers vom Anfang des Streams schreibt. Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist. In diesem Fall bietet diese Methode nicht den neuen Such Zeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Die **Seek** -Methode ändert den Seek-Zeiger, sodass nachfolgende Lese-und Schreibvorgänge an einem anderen Speicherort im Stream-Objekt stattfinden können. Es ist ein Fehler, vor dem Anfang des Streams zu suchen. Es handelt sich jedoch nicht um einen Fehler, der über das Ende des Streams hinaus sucht. Die Suche über das Ende des Streams ist für nachfolgende Schreibvorgänge nützlich, da der Stream zu diesem Zeitpunkt direkt vor dem Schreibvorgang auf die Suchposition erweitert wird.

Sie können diese Methode auch verwenden, um den aktuellen Wert des Such Zeigers abzurufen, indem Sie diese Methode aufrufen, wobei der *dwOrigin* -Parameter auf Stream \_ Seek \_ cur festgelegt und der *dlibmove* -Parameter auf 0 (null) festgelegt ist, sodass der Such Zeiger nicht geändert wird. Der aktuelle Seek-Zeiger wird im Parameter " *plibnewposition* " zurückgegeben.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie der Such Zeiger auf eine neue Position positioniert wird.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

