---
description: Die GetCurrentBuffer-Methode ruft eine Kopie des Puffers ab, der dem letzten Beispiel zugeordnet ist.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: ISampleGrabber::GetCurrentBuffer-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88af9469a1470a02be62b7684a66990c5622820e370518ed53267bd87d981879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818049"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>ISampleGrabber::GetCurrentBuffer-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die **GetCurrentBuffer-Methode** ruft eine Kopie des Puffers ab, der dem letzten Beispiel zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBufferSize* \[ in, out\]
</dt> <dd>

Zeiger auf die Größe des Puffers. Wenn *pBuffer* **NULL** ist, empfängt dieser Parameter die erforderliche Puffergröße in Bytes. Wenn *pBuffer* nicht **NULL** ist, legen Sie diesen Parameter auf die Größe des Puffers in Bytes fest. Bei der Ausgabe empfängt der Parameter die Anzahl der Bytes, die in den Puffer kopiert wurden. Dieser Wert kann kleiner als die Größe des Puffers sein.

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Zeiger auf ein Bytearray der Größe *pBufferSize* oder **NULL**. Wenn dieser Parameter nicht **NULL** ist, wird der aktuelle Puffer in das Array kopiert. Wenn dieser Parameter **NULL** ist, empfängt der *pBufferSize-Parameter* die erforderliche Puffergröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Beispiele werden nicht gepuffert. Rufen Sie [**ISampleGrabber::SetBufferSamples auf.**](isamplegrabber-setbuffersamples.md)<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Der angegebene Puffer ist nicht groß genug.<br/>                                                                         |
| <dl> <dt>**E \_ POINTER**</dt> </dl>             | **NULL-Zeigerargument.**<br/>                                                                                        |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Filter ist nicht verbunden.<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ WRONG \_ STATE**</dt> </dl>   | Der Filter hat noch keine Beispiele erhalten. Führen Sie das Diagramm aus, oder halten Sie es an, um ein Beispiel zu übermitteln.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Um die Pufferung zu aktivieren, rufen [**Sie ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) mit dem Wert **TRUE** auf.

Rufen Sie diese Methode zweimal auf. Legen Sie *pBuffer* beim ersten Aufruf auf **NULL** fest. Die Größe des Puffers wird in *pBufferSize* zurückgegeben. Ordnen Sie dann ein Array zu, und rufen Sie die Methode erneut auf. Übergeben Sie beim zweiten Aufruf die Größe des Arrays in *pBufferSize* und die Adresse des Arrays in *pBuffer*. Wenn das Array nicht groß genug ist, gibt die Methode E \_ OUTOFMEMORY zurück.

Der *pBuffer-Parameter* wird als **long-Zeiger** eingegeben, aber der Inhalt des Puffers hängt vom Format der Daten ab. Rufen Sie [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) auf, um den Medientyp des Formats abzurufen.

Rufen Sie diese Methode nicht auf, während das Filterdiagramm ausgeführt wird. Während das Filterdiagramm ausgeführt wird, überschreibt der Sample Grabber-Filter den Inhalt des Puffers, sobald er ein neues Beispiel empfängt. Die beste Möglichkeit, diese Methode zu verwenden, ist die Verwendung des "einmaligen Modus", der das Diagramm nach dem Empfang des ersten Beispiels beendet. Um den einmaligen Modus festzulegen, rufen [**Sie ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md)auf.

Der Filter puffert keine Prärollbeispiele oder Beispiele, in denen der **dwStreamId-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) etwas anderes als AM \_ STREAM MEDIA \_ ist.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden des Beispielgrabbers](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber-Schnittstelle**](isamplegrabber.md)
</dt> </dl>

 

 




