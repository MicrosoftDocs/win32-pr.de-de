---
description: Die SetCallback-Methode gibt eine Rückruf Methode an, die für eingehende Stichproben aufgerufen wird.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'Isamplegrabber:: SetCallback-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360934"
---
# <a name="isamplegrabbersetcallback-method"></a>Isamplegrabber:: SetCallback-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **SetCallback** -Methode gibt eine Rückruf Methode an, die für eingehende Stichproben aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCallback* 
</dt> <dd>

Zeiger auf eine [**isamplegrabbercb**](isamplegrabbercb.md) -Schnittstelle, die die Rückruf Methode enthält, oder **null** , um den Rückruf abzubrechen.

</dd> <dt>

*Whichmethodumcallback* 
</dt> <dd>

Der Index, der die Rückruf Methode angibt. Muss einen der folgenden Werte aufweisen.



| Wert | BESCHREIBUNG                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Der Beispiel-Grabber Filter Ruft die [**isamplegrabbercb:: samplecb**](isamplegrabbercb-samplecb.md) -Methode auf. Diese Methode empfängt einen [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Zeiger.               |
| 1     | Der Beispiel-Grabber Filter Ruft die [**isamplegrabbercb:: buffercb**](isamplegrabbercb-buffercb.md) -Methode auf. Diese Methode empfängt einen Zeiger auf den Puffer, der im Medien Beispiel enthalten ist. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der Datenverarbeitungs Thread wird blockiert, bis die Rückruf Methode zurückgibt. Wenn der Rückruf nicht schnell zurückgegeben wird, kann er die Wiedergabe beeinträchtigen.

Der Filter ruft nicht die Rückruffunktion für ein Vorlauf ausgeführt-Beispiele oder Beispiele auf, bei denen das **dwstreamid** -Element der " [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) "-Struktur etwas anderes als "am-Stream-Medien" ist \_ \_ .

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

 

 




