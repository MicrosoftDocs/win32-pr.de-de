---
description: Die DirectShow-Basisklassen stellen Hilfsfunktionen für die Behandlung der AM \_ MEDIA \_ TYPE-Struktur bereit.
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Medientypfunktionen (Mtype.h)
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
ms.openlocfilehash: ef47b944d5d445f57779f99cb8517a773a7efba19ae3f2133f896fcba7b86548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153158"
---
# <a name="media-type-functions"></a>Medientypfunktionen

Die DirectShow-Basisklassen stellen Hilfsfunktionen für die Behandlung der [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) bereit.

Die **AM \_ MEDIA \_ TYPE-Struktur** enthält einen Zeiger (den **pbFormat-Member)** auf einen anderen Speicherblock, der als *Formatblock* bezeichnet wird. Wenn Sie mit dieser Struktur arbeiten, müssen Sie daher bei der Speicherbelegung vorsichtig sein, um Speicherverluste zu vermeiden.

Die folgenden Funktionen weisen Arbeitsspeicher zu:

-   **CreateMediaType** ordnet eine neue **AM \_ MEDIA \_ TYPE-Struktur** und den Formatblock zu.
-   **CopyMediaType** kopiert in eine vorhandene **AM \_ MEDIA \_ TYPE-Struktur,** weist jedoch den Formatblock zu.
-   **CreateAudioMediaType** initialisiert eine vorhandene **AM \_ MEDIA \_ TYPE-Struktur** und ordnet optional den Formatblock zu.

Die folgenden Funktionen stellen Arbeitsspeicher frei:

-   **FreeMediaType** gibt den Formatblock frei.
-   **DeleteMediaType** gibt eine **AM \_ MEDIA \_ TYPE-Struktur** einschließlich des Formatblocks frei.



| Funktion                                             | Beschreibung                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | Kopiert eine vom Task zugeordnete **AM \_ MEDIA \_ TYPE-Struktur.**                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | Initialisiert eine Medientypstruktur mit einer Wellenformatstruktur.                                           |
| [**CreateMediaType**](createmediatype.md)           | Ordnet eine **AM MEDIA \_ \_ TYPE-Struktur** aus einer vorhandenen **AM MEDIA \_ \_ TYPE-Struktur** zu und initialisiert sie. |
| [**DeleteMediaType**](deletemediatype.md)           | Löscht eine vom Task zugeordnete **AM \_ MEDIA \_ TYPE-Struktur.**                                                     |
| [**FreeMediaType**](freemediatype.md)               | Gibt eine taskbezogene **AM \_ MEDIA \_ TYPE-Struktur** aus dem Arbeitsspeicher frei.                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




