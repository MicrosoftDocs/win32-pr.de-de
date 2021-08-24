---
description: Die CBaseDispatch-Klasse ist eine Basisklasse zum Implementieren der IDispatch-Schnittstelle in einem DirectShow-Filter.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: CBaseDispatch-Klasse (Ctlutil.h)
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
ms.openlocfilehash: 1a094ad3b79dbeb8c4dfc2888de01a521738740fc19ad70b521172d3194fd9f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793315"
---
# <a name="cbasedispatch-class"></a>CBaseDispatch-Klasse

![cbasedispatch-Klassenhierarchie](images/cutil01.png)

Die **CBaseDispatch-Klasse** ist eine Basisklasse zum Implementieren der **IDispatch-Schnittstelle** in einem DirectShow-Filter.

Diese Klasse ist auf die Unterstützung der Automation-kompatiblen Schnittstellen beschränkt, die von der DirectShow-Typbibliothek,TypeLib, exportiert werden. Beispielsweise verwenden die [**Klassen CMediaControl**](cmediacontrol.md) und [**CMediaPosition**](cmediaposition.md) **CBaseDispatch,** um [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) bzw. [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)zu implementieren. Aufgrund dieser Einschränkung gibt es wahrscheinlich keinen Grund, **CBaseDispatch** direkt in Ihren eigenen Filtern zu verwenden.

Gehen Sie wie folgt vor, um diese Klasse zu verwenden:

-   Deklarieren Sie eine neue Klasse, die **IDispatch unterstützt.**
-   Geben Sie ihrer neuen Klasse eine private Membervariable vom Typ **CBaseDispatch.**
-   Implementieren Sie die **IDispatch-Methoden.**
-   Rufen Sie **in Ihren IDispatch-Methoden** die **CBaseDispatch-Methoden** auf.

Weitere Informationen finden Sie im Quellcode für eine der In Ctlutil.h deklarierten Beispielklassen.



| Öffentliche Methoden                                             | BESCHREIBUNG                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | Konstruktormethode.                                                                                                 |
| [**~CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Destruktormethode.                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | Karten einen Satz von Namen zu einem entsprechenden Satz von DISPIDs.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Ruft die Typinformationen für das -Objekt ab, die dann verwendet werden können, um die Typinformationen für eine Schnittstelle abzurufen. |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | Ruft die Anzahl der Schnittstellen für Typinformationen ab, die das -Objekt bietet.                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




