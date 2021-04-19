---
description: Die cmediaposition-Klasse verarbeitet die IDispatch-Methoden der Dual-Schnittstelle imediaposition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Cmediaposition-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369623"
---
# <a name="cmediaposition-class"></a>Cmediaposition-Klasse

![cmediaposition-Klassenhierarchie](images/cutil14.png)

Die **cmediaposition** -Klasse verarbeitet die **IDispatch** -Methoden der Dual-Schnittstelle [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) .

Diese Klasse erbt die Schnittstelle [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) , implementiert Sie jedoch nicht. **IDispatch** wird durch die [**cbasedispatch**](cbasedispatch.md) -Klasse und die DirectShow-Typbibliothek implementiert. Verwenden Sie diese Klasse nicht direkt. Verwenden Sie stattdessen eine der folgenden Klassen:

-   Quell Filter: Verwenden Sie die [**csourceseeking**](csourceseeking.md) -Basisklasse, um Suchvorgänge zu implementieren.
-   Transformations Filter: Verwenden Sie die [**cpospassthru**](cpospassthru.md) -Klasse, um Such Befehle zu übergeben.
-   Renderer: Verwenden Sie die [**crendererpospassthru**](crendererpospassthru.md) -Klasse, um Such Befehle zu übergeben.



| Öffentliche Methoden                                              | BESCHREIBUNG                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Cmediaposition**](cmediaposition-cmediaposition.md)     | Konstruktormethode.                                                                                                 |
| IDispatch-Methoden                                           | BESCHREIBUNG                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Ordnet einem entsprechenden Satz von DISPIDs einen Satz von Namen zu.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können. |
| [**Gettypeingefocount**](cmediaposition-gettypeinfocount.md) | Ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.                                            |
| [**Invoke**](cmediaposition-invoke.md)                     | Bietet Zugriff auf Eigenschaften und Methoden, die vom-Objekt verfügbar gemacht werden.                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




