---
description: Die cenummediatypes-Klasse implementiert einen Enumerator für bevorzugte Medientypen.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Cenumschlag mediatypes-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354664"
---
# <a name="cenummediatypes-class"></a>Cenum mediatypes-Klasse

![cenenmediatypes-Klassenhierarchie](images/filter04.png)

Die- `CEnumMediaTypes` Klasse implementiert einen Enumerator für bevorzugte Medientypen.

Diese Klasse implementiert die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle. Die folgenden [**cbasepin**](cbasepin.md) -Methoden werden aufgerufen:

-   [**Cbasepin:: getmediatype**](cbasepin-getmediatype.md): Ruft einen Medientyp ab, auf den von einem NULL basierten Index verwiesen wird.
-   [**Cbasepin:: getmediatyetversion**](cbasepin-getmediatypeversion.md): bestimmt, ob sich der Satz bevorzugter Typen geändert hat.

Wenn eine PIN die Liste der bevorzugten Medientypen ändert, erhöht die PIN die Medientyp-Versionsnummer. In diesem Fall wird das Enumeratorobjekt nicht mehr mit der PIN synchronisiert, und die Klassen Methoden geben die Vfw E-Enumeration nicht \_ \_ synchron zurück \_ \_ \_ . Aufrufen der Methode [**cenummediatypes:: Reset**](cenummediatypes-reset.md) zum erneuten Synchronisieren des Enumerators.



| Öffentliche Methoden                                               | BESCHREIBUNG                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**Cenum mediatypes**](cenummediatypes-cenummediatypes.md)   | Konstruktormethode.                                             |
| [**~ Cenum mediatypes**](cenummediatypes--cenummediatypes.md) | Dekonstruktormethode. Virtu.                                     |
| Ienummediatypes-Methoden                                      | BESCHREIBUNG                                                     |
| [**Klon**](cenummediatypes-clone.md)                       | Erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. |
| [**Weiter**](cenummediatypes-next.md)                         | Ruft eine angegebene Anzahl von Medientypen ab.                    |
| [**Zurücksetzen**](cenummediatypes-reset.md)                       | Setzt die Enumerationsfolge auf den Anfang zurück.               |
| [**Überspringen**](cenummediatypes-skip.md)                         | Überspringt eine angegebene Anzahl von Medientypen.                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




