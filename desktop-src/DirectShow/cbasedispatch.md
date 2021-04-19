---
description: Die cbasedispatch-Klasse ist eine Basisklasse zum Implementieren der IDispatch-Schnittstelle in einem DirectShow-Filter.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Cbasedispatch-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361910"
---
# <a name="cbasedispatch-class"></a>Cbasedispatch-Klasse

![cbasedispatch-Klassenhierarchie](images/cutil01.png)

Die **cbasedispatch** -Klasse ist eine Basisklasse zum Implementieren der **IDispatch** -Schnittstelle in einem DirectShow-Filter.

Diese Klasse ist auf die Unterstützung der Automatisierungs kompatiblen Schnittstellen beschränkt, die von der DirectShow-Typbibliothek, QuartzTypeLib, exportiert werden. Beispielsweise verwenden die Klassen [**cmediacontrol**](cmediacontrol.md) und [**cmediaposition**](cmediaposition.md) **cbasedispatch** zum Implementieren von [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) bzw. [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition). Aufgrund dieser Einschränkung gibt es wahrscheinlich keinen Grund, **cbasedispatch** direkt in ihren eigenen Filtern zu verwenden.

Gehen Sie folgendermaßen vor, um diese Klasse zu verwenden:

-   Deklarieren Sie eine neue Klasse, die **IDispatch** unterstützt.
-   Geben Sie der neuen Klasse eine private Member-Variable vom Typ **cbasedispatch**.
-   Implementieren Sie die **IDispatch** -Methoden.
-   Nennen Sie in Ihren **IDispatch** -Methoden die **cbasedispatch** -Methoden.

Weitere Informationen finden Sie im Quellcode für eine der in ctlutil. h deklarierten Beispiel Klassen.



| Öffentliche Methoden                                             | BESCHREIBUNG                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Cbasedispatch**](cbasedispatch-cbasedispatch.md)       | Konstruktormethode.                                                                                                 |
| [**~ Cbasedispatch**](cbasedispatch--cbasedispatch.md)     | Dekonstruktormethode.                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | Ordnet einem entsprechenden Satz von DISPIDs einen Satz von Namen zu.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können. |
| [**Gettypeingefocount**](cbasedispatch-gettypeinfocount.md) | Ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




