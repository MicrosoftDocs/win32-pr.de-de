---
description: Die CEnumMediaTypes-Klasse implementiert einen Enumerator für bevorzugte Medientypen.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: CEnumMediaTypes-Klasse (Amfilter.h)
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
ms.openlocfilehash: 1729407f1022c2781fc97f8638ea8748323c151e9bd67c5ad31b30ae05fdff0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131274"
---
# <a name="cenummediatypes-class"></a>CEnumMediaTypes-Klasse

![cenummediatypes-Klassenhierarchie](images/filter04.png)

Die `CEnumMediaTypes` -Klasse implementiert einen Enumerator für bevorzugte Medientypen.

Diese Klasse implementiert die [**IEnumMediaTypes-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) Sie ruft die folgenden [**CBasePin-Methoden**](cbasepin.md) auf:

-   [**CBasePin::GetMediaType:**](cbasepin-getmediatype.md)Ruft einen Medientyp ab, auf den von einem nullbasierten Index verwiesen wird.
-   [**CBasePin::GetMediaTypeVersion:**](cbasepin-getmediatypeversion.md)Bestimmt, ob sich der Satz der bevorzugten Typen geändert hat.

Wenn ein Pin seine Liste der bevorzugten Medientypen ändert, erhöht der Pin die Versionsnummer des Medientyps. In diesem Fall wird das Enumeratorobjekt nicht mehr mit dem Pin synchronisiert, und die Klassenmethoden geben VFW \_ E \_ ENUM \_ OUT OF SYNC \_ \_ zurück. Rufen Sie die [**CEnumMediaTypes::Reset-Methode**](cenummediatypes-reset.md) auf, um den Enumerator erneut zu synchronisieren.



| Öffentliche Methoden                                               | Beschreibung                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | Konstruktormethode.                                             |
| [**~CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | Destruktormethode. Virtuellen.                                     |
| IEnumMediaTypes-Methoden                                      | Beschreibung                                                     |
| [**Klon**](cenummediatypes-clone.md)                       | Erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. |
| [**Weiter**](cenummediatypes-next.md)                         | Ruft eine angegebene Anzahl von Medientypen ab.                    |
| [**Zurücksetzen**](cenummediatypes-reset.md)                       | Setzt die Enumerationsfolge auf den Anfang zurück.               |
| [**Überspringen**](cenummediatypes-skip.md)                         | Überspringt eine angegebene Anzahl von Medientypen.                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




