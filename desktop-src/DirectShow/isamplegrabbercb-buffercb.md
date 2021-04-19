---
description: Die buffercb-Methode ist eine Rückruf Methode, die einen Zeiger auf den Beispiel Puffer empfängt.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'Isamplegrabbercb:: buffercb-Methode (qedit. h)'
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
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359790"
---
# <a name="isamplegrabbercbbuffercb-method"></a>Isamplegrabbercb:: buffercb-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **buffercb** -Methode ist eine Rückruf Methode, die einen Zeiger auf den Beispiel Puffer empfängt.

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

*Sampletime* 
</dt> <dd>

Startzeit des Beispiels in Sekunden.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf einen Puffer, der die Beispiel Daten enthält. Das Format der Daten hängt vom Medientyp der Eingabe-PIN des beispielgrabers ab. Um den Medientyp abzurufen, nennen Sie [**isamplegrabber:: getconnectedmediatype**](isamplegrabber-getconnectedmediatype.md).

</dd> <dt>

*Bufferlen* 
</dt> <dd>

Länge des Puffers, auf den *pbuffer* zeigt (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder andernfalls einen **HRESULT** -Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Diese Rückruf Methode erhält einen Zeiger auf die Daten im neuesten Medien Beispiel.

> [!Note]  
> Diese Methode erhält einen Zeiger auf die ursprünglichen Beispiel Daten, nicht auf eine Kopie. In der ursprünglichen Dokumentation wurde fälschlicherweise angegeben, dass *pbuffer* eine Kopie der Daten enthält.

 

Rufen Sie zum Einrichten des Rückrufs [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md)auf.

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

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**Isamplegrabbercb-Schnittstelle**](isamplegrabbercb.md)
</dt> </dl>

 

 




