---
description: Die cimagesample-Klasse implementiert ein Medien Beispiel, das eine GDI-geräteunabhängige Bitmap (DIB) verwaltet.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Cimagesample-Klasse (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356340"
---
# <a name="cimagesample-class"></a>Cimagesample-Klasse

![cimagesample-Klassenhierarchie](images/wutil03.png)

Die- `CImageSample` Klasse implementiert ein Medien Beispiel, das eine GDI-geräteunabhängige Bitmap (DIB) verwaltet. Diese Klasse wird von der [**cmediasample**](cmediasample.md) -Klasse abgeleitet. Es ist für die Verwendung mit der [**cimagezuordcator**](cimageallocator.md) -Klasse vorgesehen. Die **cimagezuordcator** -Klasse stellt eine Zuweisung bereit, die- `CImageSample` Objekte erstellt.



| Geschützte Member-Variablen                        | BESCHREIBUNG                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**Mio. \_ dibdata**](cimagesample-m-dibdata.md)      | Enthält Informationen über das DIB, das von diesem-Objekt verwaltet wird.  |
| [**m- \_ binit**](cimagesample-m-binit.md)          | Gibt an, ob das Objekt initialisiert wurde.                |
| Öffentliche Methoden                                    | BESCHREIBUNG                                                       |
| [**Cimagesample**](cimagesample-cimagesample.md) | Konstruktormethode.                                               |
| [**Getdibdata**](cimagesample-getdibdata.md)     | Ruft Informationen über das DIB ab, das von diesem-Objekt verwaltet wird. |
| [**Setdibdata**](cimagesample-setdibdata.md)     | Legt Informationen über das DIB fest, das von diesem-Objekt verwaltet wird.      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




