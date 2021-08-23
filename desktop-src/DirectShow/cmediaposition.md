---
description: Die CMediaPosition-Klasse verarbeitet die IDispatch-Methoden der dualen IMediaPosition-Schnittstelle.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: CMediaPosition-Klasse (Ctlutil.h)
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
ms.openlocfilehash: 7305d5eded589e167352ce7ff13194b52965b939daf907e8381b64684a03d1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634850"
---
# <a name="cmediaposition-class"></a>CMediaPosition-Klasse

![Hierarchie der Cmediaposition-Klasse](images/cutil14.png)

Die **CMediaPosition-Klasse** verarbeitet die **IDispatch-Methoden** der dualen [**IMediaPosition-Schnittstelle.**](/windows/desktop/api/Control/nn-control-imediaposition)

Diese Klasse erbt die [**IMediaPosition-Schnittstelle,**](/windows/desktop/api/Control/nn-control-imediaposition) implementiert sie jedoch nicht. **IDispatch** wird über die [**CBaseDispatch-Klasse**](cbasedispatch.md) und die DirectShow-Typbibliothek implementiert. Verwenden Sie diese Klasse nicht direkt. Verwenden Sie stattdessen eine der folgenden Klassen:

-   Quellfilter: Verwenden Sie die [**CSourceSeeking-Basisklasse,**](csourceseeking.md) um Suchfunktionen zu implementieren.
-   Transformieren von Filtern: Verwenden Sie die [**CPosPassThru-Klasse,**](cpospassthru.md) um Suchbefehle upstreamzu übergeben.
-   Renderer: Verwenden Sie die [**CRendererPosPassThru-Klasse,**](crendererpospassthru.md) um Suchbefehle upstream zu übergeben.



| Öffentliche Methoden                                              | Beschreibung                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Konstruktormethode.                                                                                                 |
| IDispatch-Methoden                                           | Beschreibung                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Karten einen Satz von Namen zu einem entsprechenden Satz von DISPIDs.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Ruft die Typinformationen für das -Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Ruft die Anzahl der Typinformationsschnittstellen ab, die das -Objekt bereitstellt.                                            |
| [**Invoke**](cmediaposition-invoke.md)                     | Bietet Zugriff auf Eigenschaften und Methoden, die vom -Objekt verfügbar gemacht werden.                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




