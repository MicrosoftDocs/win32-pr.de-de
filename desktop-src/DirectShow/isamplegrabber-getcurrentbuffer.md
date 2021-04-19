---
description: Die getcurrentbuffer-Methode ruft eine Kopie des Puffers ab, der mit dem letzten Beispiel verknüpft ist.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'Isamplegrabber:: getcurrentbuffer-Methode (qedit. h)'
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
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369162"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>Isamplegrabber:: getcurrentbuffer-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **getcurrentbuffer** -Methode ruft eine Kopie des Puffers ab, der mit dem letzten Beispiel verknüpft ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbuffersize* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Größe des Puffers. Wenn *pbuffer* den Wert **null** hat, erhält dieser Parameter die erforderliche Puffergröße in Bytes. Wenn *pbuffer* nicht **null** ist, legen Sie diesen Parameter auf die Größe des Puffers (in Bytes) fest. Bei der Ausgabe empfängt der-Parameter die Anzahl der Bytes, die in den Puffer kopiert wurden. Dieser Wert kann kleiner sein als die Größe des Puffers.

</dd> <dt>

*pbuffer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Bytearray mit der Größe *pbuffersize* oder **null**. Wenn dieser Parameter nicht **null** ist, wird der aktuelle Puffer in das Array kopiert. Wenn dieser Parameter **null** ist, erhält der *pbuffersize* -Parameter die erforderliche Puffergröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ invalidArg**</dt> </dl>          | Die Stichproben werden nicht gepuffert. Aufrufen von [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md).<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>         | Der angegebene Puffer ist nicht groß genug.<br/>                                                                         |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>             | **Null** -Zeigerargument.<br/>                                                                                        |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Der Filter ist nicht verbunden.<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl>   | Der Filter hat noch keine Stichproben empfangen. Um ein Beispiel zu liefern, führen Sie das Diagramm aus oder halten es an.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Um die Pufferung zu aktivieren, wenden Sie [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md) mit dem Wert **true** an.

Ruft diese Methode zweimal auf. Legen Sie für den ersten-Befehl *pbuffer* auf **null** fest. Die Größe des Puffers wird in " *pbuffersize*" zurückgegeben. Weisen Sie dann ein Array zu, und nennen Sie die Methode erneut. Übergeben Sie im zweiten-Befehl die Größe des Arrays in *pbuffersize*, und übergeben Sie die Adresse des Arrays in *pbuffer*. Wenn das Array nicht groß genug ist, gibt die Methode "E \_ outo fmemory" zurück.

Der *pbuffer* -Parameter wird als **Long** -Zeiger eingegeben, aber der Inhalt des Puffers hängt vom Format der Daten ab. Wenden Sie [**isamplegrabber:: getconnectedmediatype**](isamplegrabber-getconnectedmediatype.md) an, um den Medientyp des Formats zu erhalten.

Diese Methode wird nicht aufgerufen, während das Filter Diagramm ausgeführt wird. Während der Ausführung des Filter Diagramms wird der Inhalt des Puffers beim Empfang eines neuen Beispiels überschrieben. Die beste Möglichkeit, diese Methode zu verwenden, ist die Verwendung des "One-Shot"-Modus, der das Diagramm nach dem Empfang des ersten Beispiels stoppt. Um den One-Shot-Modus festzulegen, wenden Sie [**isamplegrabber:: setoneshot**](isamplegrabber-setoneshot.md)an.

Der Filter puffert keine vorab Beispiele oder Beispiele, in denen das **dwstreamid** -Element der " [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) "-Struktur etwas anderes als "am-Stream-Medien" ist \_ \_ .

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden der Beispiel-Grabber](using-the-sample-grabber.md)
</dt> <dt>

[**Isamplegrabber-Schnittstelle**](isamplegrabber.md)
</dt> </dl>

 

 




