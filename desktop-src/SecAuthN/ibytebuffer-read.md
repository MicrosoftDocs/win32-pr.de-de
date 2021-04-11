---
description: Die Read-Methode liest eine angegebene Anzahl von Bytes aus dem Puffer Objekt in den Arbeitsspeicher, beginnend beim aktuellen Such Zeiger.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'Ibytebuffer:: Read-Methode (scardssp. h)'
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
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217774"
---
# <a name="ibytebufferread-method"></a>Ibytebuffer:: Read-Methode

\[Die **Read** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **Read** -Methode liest eine angegebene Anzahl von Bytes aus dem Puffer Objekt in den Arbeitsspeicher, beginnend beim aktuellen Such Zeiger.

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

*PBYTE* \[ vorgenommen\]
</dt> <dd>

Zeigt auf den Puffer, in den die Streamdaten gelesen werden. Wenn ein Fehler auftritt, ist dieser Wert **null**.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Anzahl der Daten bytes, die aus dem Datenstrom Objekt gelesen werden sollen.

</dd> <dt>

*pcbread* \[ vorgenommen\]
</dt> <dd>

Adresse einer **Long** -Variablen, die die tatsächliche Anzahl von Bytes empfängt, die aus dem Streamobjekt gelesen wurden. Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist. In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der gelesenen Bytes bereit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Methode liest Bytes aus diesem Datenstrom Objekt in den Arbeitsspeicher. Das Stream-Objekt muss im STGM- \_ Lesemodus geöffnet werden. Mit dieser Methode wird der Such Zeiger mit der tatsächlichen Anzahl der gelesenen Bytes angepasst.

Die Anzahl der tatsächlich gelesenen Bytes wird auch im *pcbread* -Parameter zurückgegeben.

Hinweise für Aufrufer

Die tatsächliche Anzahl von gelesenen Bytes kann weniger als die Anzahl der angeforderten Bytes sein, wenn ein Fehler auftritt oder wenn das Ende des Streams während des Lesevorgangs erreicht wird.

Einige Implementierungen geben möglicherweise einen Fehler zurück, wenn das Ende des Streams während des Lesevorgang erreicht wird. Sie müssen darauf vorbereitet sein, die Fehlerrückgabe-oder S \_ OK-Rückgabewerte am Ende der Datenstrom Lesevorgänge zu behandeln.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Bytes aus dem Puffer gelesen werden.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

