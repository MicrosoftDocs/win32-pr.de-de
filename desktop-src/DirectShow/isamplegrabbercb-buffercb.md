---
description: Die BufferCB-Methode ist eine Rückrufmethode, die einen Zeiger auf den Beispielpuffer empfängt.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: ISampleGrabberCB::BufferCB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c92e83c8daf5bf129a9aa8330bcc53caa88537f2395aeceebd8b5da2037c5b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817590"
---
# <a name="isamplegrabbercbbuffercb-method"></a>ISampleGrabberCB::BufferCB-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die **BufferCB-Methode** ist eine Rückrufmethode, die einen Zeiger auf den Beispielpuffer empfängt.

## <a name="syntax"></a>Syntax


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SampleTime* 
</dt> <dd>

Startzeit des Beispiels in Sekunden.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf einen Puffer, der die Beispieldaten enthält. Das Format der Daten hängt vom Medientyp des Eingabepins des Beispielgrabbers ab. Rufen Sie [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md)auf, um den Medientyp abzurufen.

</dd> <dt>

*BufferLen* 
</dt> <dd>

Länge des Puffers, auf den *pBuffer* zeigt, in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder andernfalls einen **HRESULT-Fehlercode.**

## <a name="remarks"></a>Hinweise

Diese Rückrufmethode empfängt einen Zeiger auf die Daten im letzten Medienbeispiel.

> [!Note]  
> Diese Methode empfängt einen Zeiger auf die ursprünglichen Beispieldaten, keine Kopie. In der ursprünglichen Dokumentation wurde fälschlicherweise angegeben, dass *pBuffer* eine Kopie der Daten enthält.

 

Rufen Sie [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md)auf, um den Rückruf einzurichten.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**ISampleGrabberCB-Schnittstelle**](isamplegrabbercb.md)
</dt> </dl>

 

 




