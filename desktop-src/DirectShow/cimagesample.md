---
description: Die CImageSample-Klasse implementiert ein Medienbeispiel, das eine geräteunabhängige GDI-Bitmap (DIB) verwaltet.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: CImageSample-Klasse (Winutil.h)
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
ms.openlocfilehash: afd19b6aba7546ec420985adf6d58d3f7acc7546913ec8f1c168c80ad3b7ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402407"
---
# <a name="cimagesample-class"></a>CImageSample-Klasse

![cimagesample-Klassenhierarchie](images/wutil03.png)

Die `CImageSample` -Klasse implementiert ein Medienbeispiel, das eine geräteunabhängige GDI-Bitmap (DIB) verwaltet. Diese Klasse wird von der [**CMediaSample-Klasse**](cmediasample.md) abgeleitet. Sie ist für die Verwendung mit der [**CImageAllocator-Klasse**](cimageallocator.md) vorgesehen. Die **CImageAllocator-Klasse** stellt eine Zuweisung bereit, die `CImageSample` -Objekte erstellt.



| Geschützte Membervariablen                        | BESCHREIBUNG                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**m \_ DibData**](cimagesample-m-dibdata.md)      | Enthält Informationen zum DIB, das von diesem Objekt verwaltet wird.  |
| [**m \_ bInit**](cimagesample-m-binit.md)          | Gibt an, ob das Objekt initialisiert wurde.                |
| Öffentliche Methoden                                    | BESCHREIBUNG                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | Konstruktormethode.                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | Ruft Informationen zum DIB ab, das von diesem Objekt verwaltet wird. |
| [**SetDIBData**](cimagesample-setdibdata.md)     | Legt Informationen zum DIB fest, das von diesem Objekt verwaltet wird.      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




