---
description: Die crenderedinputpin-Klasse ist eine Basisklasse zum Implementieren einer Eingabe-PIN für einen Renderer.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Crenderedinputpin-Klasse (amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370146"
---
# <a name="crenderedinputpin-class"></a>Crenderedinputpin-Klasse

![crenderedinputpin-Klassenhierarchie](images/rbase04.png)

Die **crenderedinputpin** -Klasse ist eine Basisklasse zum Implementieren einer Eingabe-PIN für einen Renderer. Diese Klasse wurde für Renderer-Filter entwickelt, die nicht von der [**cbaserenderer**](cbaserenderer.md) -Klasse abgeleitet werden. (Filter, die von **cbaserenderer** abgeleitet werden, sollten die [**crendererinputpin**](crendererinputpin.md) -Klasse für die Eingabe-PIN verwenden.)

Um diese Klasse verwenden zu können, müssen Sie mindestens die folgenden Schritte ausführen:

-   Deklarieren Sie eine neue PIN-Klasse, die **crenderedinputpin** erbt.
-   Deklarieren Sie in der PIN-Klasse ein kritisches Abschnitts Objekt, das die streamingsperre enthalten soll. Zu diesem Zweck können Sie die [**ccritsec**](ccritsec.md) -Klasse verwenden. Weitere Informationen finden Sie unter [Threads und wichtige Abschnitte](threads-and-critical-sections.md).
-   Überschreiben Sie [**crenderedinputpin:: EndOfStream**](crenderedinputpin-endofstream.md) , um die streamingsperre aufzunehmen.
-   Implementieren Sie die Methoden [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md)und [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) .
-   Implementieren Sie in Ihrem Filter [**cbasefilter:: getpin**](cbasefilter-getpin.md) , um eine Instanz der PIN-Klasse zurückzugeben.

Sie können diese Klasse in einem Renderer verwenden, der über mehr als eine Eingabe-PIN verfügt. Diese Klasse erbt die [**cbasinput Pin**](cbaseinputpin.md) -Klasse.



| Geschützte Member-Variablen                                            | BESCHREIBUNG                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**m \_ batendofistream**](crenderedinputpin-m-batendofstream.md)       | Gibt an, ob das Ende des Streams erreicht wurde.                                                         |
| [**m \_ bcompletenotifiziert**](crenderedinputpin-m-bcompletenotified.md) | Gibt an, ob die PIN ein [**EC \_ Complete**](ec-complete.md) -Ereignis an den Filter Diagramm-Manager gesendet hat. |
| Öffentliche Methoden                                                        | BESCHREIBUNG                                                                                                  |
| [**Aktiv**](crenderedinputpin-active.md)                            | Benachrichtigt die PIN, dass der Filter jetzt aktiv ist.                                                              |
| [**Crenderedinputpin**](crenderedinputpin-crenderedinputpin.md)      | Konstruktormethode.                                                                                          |
| [**Ausführen**](crenderedinputpin-run.md)                                  | Benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird.                                                             |
| IPin-Methoden                                                          | BESCHREIBUNG                                                                                                  |
| [**Endflush**](crenderedinputpin-endflush.md)                        | Beendet einen Löschvorgang.                                                                                      |
| [**EndOfStream**](crenderedinputpin-endofstream.md)                  | Benachrichtigt die PIN, dass keine weiteren Daten erwartet werden, bis der Filter einen neuen Befehl zum Ausführen erhält.            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




