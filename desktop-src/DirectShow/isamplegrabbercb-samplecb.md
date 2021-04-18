---
description: Die samplecb-Methode ist eine Rückruf Methode, die einen Zeiger auf das Medien Beispiel empfängt.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'Isamplegrabbercb:: samplecb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365619"
---
# <a name="isamplegrabbercbsamplecb-method"></a>Isamplegrabbercb:: samplecb-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SampleCB` Methode ist eine Rückruf Methode, die einen Zeiger auf das Medien Beispiel empfängt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sampletime* 
</dt> <dd>

Startzeit des Beispiels in Sekunden.

</dd> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder andernfalls einen **HRESULT** -Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

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

 

 




