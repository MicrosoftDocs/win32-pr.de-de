---
description: Die CSeekingPassThru-Klasse ist ein Hilfsobjekt, das CPosPassThru- und CRendererPosPassThru-Objekte erstellt.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: CSeekingPassThru-Klasse (Seekpt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ffb8436623cb5ba5f415ceb8bbdafe00e22487da2bbfaba5d02ee4c8f189c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953769"
---
# <a name="cseekingpassthru-class"></a>CSeekingPassThru-Klasse

Die `CSeekingPassThru` -Klasse ist ein Hilfsobjekt, das [**CPosPassThru-**](cpospassthru.md) und [**CRendererPosPassThru-Objekte**](crendererpospassthru.md) erstellt.

Die Klassen **CPosPassThru** und **CRendererPosPassThru** sind Hilfsobjekte, die Suchbefehle upstream übergeben. Daher ist die `CSeekingPassThru` -Klasse ein Hilfsobjekt zum Erstellen von Hilfsobjekten.

Es ist nicht erforderlich, diese Klasse direkt zu verwenden. Verwenden Sie stattdessen die [**CreatePosPassThru-Funktion,**](createpospassthru.md) die alle Details der Verwendung dieser Klasse verarbeitet. Es hat den weiteren Vorteil, dass das Objekt aus Quartz.dll geladen wird, wodurch die Codegröße Ihres Filters etwas reduziert wird. Weitere Informationen finden Sie unter [**CPosPassThru.**](cpospassthru.md)

Die `CSeekingPassThru` -Klasse macht die [**ISeekingPassThru-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) verfügbar. Die [**ISeekingPassThru::Init-Methode**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) initialisiert das -Objekt. Nachdem das Objekt initialisiert wurde, kann der Filter es nach den Schnittstellen [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) und [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) abfragen.



| Öffentliche Methoden                                                  | BESCHREIBUNG                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | Konstruktormethode.                |
| [**~CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | Destruktormethode.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Erstellt eine Instanz des -Objekts. |
| ISeekingPassThru-Methoden                                        | BESCHREIBUNG                        |
| [**Init**](cseekingpassthru-init.md)                           | Initialisiert das Objekt.            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Seekpt.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




