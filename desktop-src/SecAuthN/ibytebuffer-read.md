---
description: Die Read-Methode liest ab dem aktuellen Suchzeiger eine angegebene Anzahl von Bytes aus dem Pufferobjekt in den Arbeitsspeicher.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: IByteBuffer::Read-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb78726228e333205032a3179e5c3bedb05786b072d02e78d5cc85cea7a97336
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482670"
---
# <a name="ibytebufferread-method"></a>IByteBuffer::Read-Methode

\[Die **Read-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Read-Methode** liest ab dem aktuellen Suchzeiger eine angegebene Anzahl von Bytes aus dem Pufferobjekt in den Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pByte* \[ out\]
</dt> <dd>

Zeigt auf den Puffer, in den die Streamdaten gelesen werden. Wenn ein Fehler auftritt, ist dieser Wert **NULL.**

</dd> <dt>

*cb* \[ In\]
</dt> <dd>

Anzahl der Bytes von Daten, die aus dem Streamobjekt gelesen werden soll.

</dd> <dt>

*vorlesen* \[ out\]
</dt> <dd>

Adresse einer **LONG-Variablen,** die die tatsächliche Anzahl der aus dem Streamobjekt gelesenen Bytes empfängt. Sie können diesen Zeiger auf **NULL** festlegen, um anzugeben, dass Sie an diesem Wert nicht interessiert sind. In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der gelesenen Bytes zur Verfügung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Diese Methode liest Bytes aus diesem Streamobjekt in den Arbeitsspeicher. Das Streamobjekt muss im STGM \_ READ-Modus geöffnet werden. Diese Methode passt den Suchzeiger um die tatsächliche Anzahl der gelesenen Bytes an.

Die Anzahl der tatsächlich gelesenen Bytes wird auch im *parameterread zurückgegeben.*

Hinweise für Aufrufer

Die tatsächliche Anzahl der gelesenen Bytes kann geringer als die Anzahl der angeforderten Bytes sein, wenn ein Fehler auftritt oder das Ende des Streams während des Lesevorgang erreicht wird.

Einige Implementierungen geben möglicherweise einen Fehler zurück, wenn das Ende des Streams während des Leselaufs erreicht wird. Sie müssen darauf vorbereitet sein, die Fehler- oder S OK-Rückgabewerte am Ende \_ der Streamlesedaten zu behandeln.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Lesen von Bytes aus dem Puffer.


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
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



 

