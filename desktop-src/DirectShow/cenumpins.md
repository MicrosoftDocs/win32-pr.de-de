---
description: Die cenumpins-Klasse implementiert einen Enumerator für Pins.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Cenumpins-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365509"
---
# <a name="cenumpins-class"></a>Cenumpins-Klasse

![cenumpins-Klassenhierarchie](images/filter03.png)

Die- `CEnumPins` Klasse implementiert einen Enumerator für Pins.

Diese Klasse implementiert die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle. Die folgenden [**cbasefilter**](cbasefilter.md) -Methoden werden aufgerufen:

-   [**Cbasefilter:: getpin**](cbasefilter-getpin.md): Ruft eine PIN für den Filter ab, auf die durch einen NULL basierten Index verwiesen wird.
-   [**Cbasefilter:: getpincount**](cbasefilter-getpincount.md): Ruft die Gesamtanzahl der Pins für den Filter ab.
-   [**Cbasefilter:: getpinversion**](cbasefilter-getpinversion.md): bestimmt, ob die Pins geändert wurden.

Wenn der Filter Pins dynamisch erstellt oder zerstört, erhöht er die PIN-Version, wenn die Pins geändert werden. Wenn die Versionsnummer geändert wird, wird das Enumeratorobjekt nicht mehr mit dem Filter synchronisiert. Sobald der Enumerator nicht mehr synchronisiert ist, geben die Methoden in `CEnumPins` VFW \_ E \_ Enum \_ nicht \_ \_ synchron zurück. Zum erneuten Synchronisieren des Enumerators wird die [**cenumpins:: Reset**](cenumpins-reset.md) -Methode aufgerufen.



| Öffentliche Methoden                             | BESCHREIBUNG                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**Cenumpins**](cenumpins-cenumpins.md)   | Konstruktormethode.                                             |
| [**~ Cenumpins**](cenumpins--cenumpins.md) | Dekonstruktormethode. Virtu.                                     |
| Ienumins-Methoden                          | BESCHREIBUNG                                                     |
| [**Klon**](cenumpins-clone.md)           | Erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. |
| [**Weiter**](cenumpins-next.md)             | Ruft eine angegebene Anzahl von Pins ab.                           |
| [**Zurücksetzen**](cenumpins-reset.md)           | Setzt die Enumerationsfolge auf den Anfang zurück.               |
| [**Überspringen**](cenumpins-skip.md)             | Überspringt eine angegebene Anzahl von Pins.                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




