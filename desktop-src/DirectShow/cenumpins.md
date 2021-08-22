---
description: Die CEnumPins-Klasse implementiert einen Enumerator für Pins.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: CEnumPins-Klasse (Amfilter.h)
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
ms.openlocfilehash: 7135a07aedb879503d36011b274bdeab8035924b91bb5d9bc656d6d89dfbe201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567004"
---
# <a name="cenumpins-class"></a>CEnumPins-Klasse

![cenumpins-Klassenhierarchie](images/filter03.png)

Die `CEnumPins` -Klasse implementiert einen Enumerator für Pins.

Diese Klasse implementiert die [**IEnumPins-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) Sie ruft die folgenden [**CBaseFilter-Methoden**](cbasefilter.md) auf:

-   [**CBaseFilter::GetPin:**](cbasefilter-getpin.md)Ruft einen Pin für den Filter ab, auf den von einem nullbasierten Index verwiesen wird.
-   [**CBaseFilter::GetPinCount:**](cbasefilter-getpincount.md)Ruft die Gesamtzahl der Pins im Filter ab.
-   [**CBaseFilter::GetPinVersion:**](cbasefilter-getpinversion.md)Bestimmt, ob sich die Pins geändert haben.

Wenn der Filter pins dynamisch erstellt oder zerstört, erhöht er die Pinversion, sobald sich die Stecknadeln ändern. Wenn sich die Versionsnummer ändert, wird das Enumeratorobjekt nicht mehr mit dem Filter synchronisiert. Sobald der Enumerator nicht mehr synchron ist, geben die Methoden in `CEnumPins` VFW \_ E \_ ENUM \_ OUT OF SYNC \_ \_ zurück. Rufen Sie die [**CEnumPins::Reset-Methode**](cenumpins-reset.md) auf, um den Enumerator erneut zu synchronisieren.



| Öffentliche Methoden                             | Beschreibung                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | Konstruktormethode.                                             |
| [**~CEnumPins**](cenumpins--cenumpins.md) | Destruktormethode. Virtuellen.                                     |
| IEnumPins-Methoden                          | Beschreibung                                                     |
| [**Klon**](cenumpins-clone.md)           | Erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. |
| [**Weiter**](cenumpins-next.md)             | Ruft eine angegebene Anzahl von Pins ab.                           |
| [**Zurücksetzen**](cenumpins-reset.md)           | Setzt die Enumerationsfolge auf den Anfang zurück.               |
| [**Überspringen**](cenumpins-skip.md)             | Überspringt eine angegebene Anzahl von Pins.                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




