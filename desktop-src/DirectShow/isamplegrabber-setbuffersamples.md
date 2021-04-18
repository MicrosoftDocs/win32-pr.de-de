---
description: Die setbuffersamples-Methode gibt an, ob Beispiel Daten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Isamplegrabber:: setbuffersamples-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371432"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>Isamplegrabber:: setbuffersamples-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **setbuffersamples** -Methode gibt an, ob Beispiel Daten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.

## <a name="syntax"></a>Syntax


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Puffer* 
</dt> <dd>

Boolescher Wert, der angibt, ob Beispiel Daten gepuffert werden. **True** gibt an, dass der Filter Beispiel Daten in einen internen Puffer kopiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um den kopierten Puffer abzurufen, nennen Sie [**isamplegrabber:: getcurrentbuffer**](isamplegrabber-getcurrentbuffer.md).

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

 

 




