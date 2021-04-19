---
description: Die DirectShow-Basisklassen stellen Hilfsfunktionen zum Verarbeiten der am- \_ \_ Medientyp Struktur bereit.
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Medientyp Funktionen (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367413"
---
# <a name="media-type-functions"></a>Medientyp Funktionen

Die DirectShow-Basisklassen stellen Hilfsfunktionen zum Verarbeiten der [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur bereit.

Die **am \_ \_ Medientyp** -Struktur enthält einen Zeiger (den **pbformat** -Member) zu einem anderen Speicherblock, der als *Format Block* bezeichnet wird. Wenn Sie mit dieser Struktur arbeiten, müssen Sie daher vorsichtig bei der Speicher Belegung sein, um Speicher Verluste zu vermeiden.

Die folgenden Funktionen weisen Speicher zu:

-   Mit " **kreatemediatype** " wird eine neue **am- \_ \_ Medientyp** Struktur und der Format Block zugeordnet.
-   **Copymediatype** kopiert in eine vorhandene **\_ \_ Medientyp** Struktur, aber weist den Format Block zu.
-   " **Tinateaudiomediatype** " Initialisiert eine vorhandene **am- \_ \_ Medientyp** Struktur und weist optional den Format Block zu.

Die folgenden Funktionen können Arbeitsspeicher freigeben:

-   " **Freimediatype** " gibt den Format Block frei.
-   **Deletemediatype** gibt eine **am \_ \_ Medientyp** -Struktur frei, einschließlich des Format Blocks.



| Funktion                                             | BESCHREIBUNG                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Copymediatype**](copymediatype.md)               | Kopiert eine Aufgabe zugewiesene **am \_ \_ Medientyp** Struktur.                                                      |
| [**"Kreateaudiomediatype"**](createaudiomediatype.md) | Initialisiert eine Medientyp Struktur, wenn eine Wave-Format-Struktur angegeben ist.                                           |
| [**"Kreatemediatype"**](createmediatype.md)           | Ordnet eine **am- \_ \_ Medientyp** Struktur zu und initialisiert sie aus einer vorhandenen **am- \_ \_ Medientyp** Struktur. |
| [**Deletemediatype**](deletemediatype.md)           | Löscht eine Aufgabe zugewiesene **am \_ \_ Medientyp** Struktur.                                                     |
| [**Freimediatype**](freemediatype.md)               | Gibt eine Aufgaben zugewiesene **am \_ \_ Medientyp** -Struktur aus dem Arbeitsspeicher frei.                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




