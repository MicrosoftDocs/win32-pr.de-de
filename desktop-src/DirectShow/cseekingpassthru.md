---
description: Die cseekingpassthru-Klasse ist ein Hilfsobjekt, das cpospassthru-und crendererpospassthru-Objekte erstellt.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Cseekingpassthru-Klasse (seekpt. h)
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
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371982"
---
# <a name="cseekingpassthru-class"></a>Cseekingpassthru-Klasse

Die `CSeekingPassThru` -Klasse ist ein Hilfsobjekt, das [**cpospassthru**](cpospassthru.md) -und [**crendererpospassthru**](crendererpospassthru.md) -Objekte erstellt.

Die **cpospassthru** -Klasse und die **crendererpospassthru** -Klasse sind Hilfsobjekte, die Suchbefehle an Upstream übergeben, sodass die- `CSeekingPassThru` Klasse ein Hilfsobjekt zum Erstellen von Hilfsobjekten ist.

Es ist nicht erforderlich, diese Klasse direkt zu verwenden. Verwenden Sie stattdessen die Funktion " [**kreatepospassthru**](createpospassthru.md) ", die alle Details der Verwendung dieser Klasse behandelt. Dies hat den weiteren Vorteil, dass das Objekt aus Quartz.dll geladen wird, wodurch die Codegröße Ihres Filters etwas verringert wird. Weitere Informationen finden Sie unter [**cpospassthru**](cpospassthru.md).

Die- `CSeekingPassThru` Klasse macht die [**iseekingpassthru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) -Schnittstelle verfügbar. Die [**iseekingpassthru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) -Methode initialisiert das-Objekt. Nachdem das Objekt initialisiert wurde, kann es vom Filter für die Schnittstellen [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) und [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) abgefragt werden.



| Öffentliche Methoden                                                  | BESCHREIBUNG                        |
|-----------------------------------------------------------------|------------------------------------|
| [**Cseekingpassthru**](cseekingpassthru-cseekingpassthru.md)   | Konstruktormethode.                |
| [**~ Cseekingpassthru**](cseekingpassthru--cseekingpassthru.md) | Dekonstruktormethode.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Erstellt eine Instanz des-Objekts. |
| Iseekingpassthru-Methoden                                        | BESCHREIBUNG                        |
| [**Init**](cseekingpassthru-init.md)                           | Initialisiert das Objekt.            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Seekpt. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




