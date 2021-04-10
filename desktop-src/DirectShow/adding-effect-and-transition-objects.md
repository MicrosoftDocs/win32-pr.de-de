---
description: Hinzufügen von Effekt-und Übergangs Objekten
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Hinzufügen von Effekt-und Übergangs Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041192"
---
# <a name="adding-effect-and-transition-objects"></a>Hinzufügen von Effekt-und Übergangs Objekten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In des wird ein Effekt oder Übergang mit zwei Objekten dargestellt:

-   Ein *Zeitachsen Objekt* stellt den Effekt oder Übergang innerhalb der Zeitachse dar. Für Effekte unterstützt das Timeline-Objekt die [**iamtimelineeffect**](iamtimelineeffect.md) -Schnittstelle. Bei Übergängen wird die [**iamtimelinetrans**](iamtimelinetrans.md) -Schnittstelle unterstützt. Beide Typen unterstützen die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle.
-   Das unter *geordnete* Objekt ist ein Objekt, das die Datenverarbeitung für den Effekt oder Übergang implementiert. Das Timeline-Objekt enthält einen Zeiger auf das unter Objekt.

Führen Sie die folgenden Schritte aus, um einen Effekt oder Übergang hinzuzufügen.

**1. Erstellen des Zeitachsen Objekts**

Um das Timeline-Objekt zu erstellen, rufen Sie die [**iamtimeline::**](iamtimeline-createemptynode.md) -Methode auf. Legen Sie den Typ auf die **Zeitachse des \_ Haupt \_ Typs \_** für einen Effekt oder einen **Zeitachsen \_ \_ \_ haupttypübergang** für einen Übergang fest.

Im folgenden Beispiel wird ein Übergangs Objekt erstellt:


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. Geben Sie das untergeordnete Objekt an.**

Das Zeitachsen Objekt fungiert als Wrapper für ein anderes Objekt, das *als untergeordnetes* Element bezeichnet wird, das die eigentliche Arbeit übernimmt. Das untergeordnete Objekt implementiert eine Datentransformation, die den gewünschten Effekt oder Übergang erzeugt. Eine Liste der Übergänge und Effekte, die mit des bereitgestellt werden, finden Sie unter [Übergänge und Effekte](transitions-and-effects.md).

Um das untergeordnete Objekt festzulegen, wenden Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode für das Timeline-Objekt an, und übergeben Sie dabei den Klassen Bezeichner (CLSID) des untergeordneten Objekts. DirectShow bietet einen Enumerator für Video Effekte und Video Übergänge, die Sie zum Abrufen der CLSID verwenden können. Weitere Informationen finden Sie unter [Enumerieren von Effekten und Übergängen](enumerating-effects-and-transitions.md).

Im folgenden Beispiel wird der [SMPTE](smpte-wipe-transition.md) -zurücksetzen-Übergang als untergeordnetes Objekt festgelegt:


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. Festlegen der Start-und Endzeiten**

Um die Start-und Endzeit Zeiten festzulegen, müssen Sie die [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md) -Methode aufrufen. Diese Zeiten sind relativ zur Startzeit des übergeordneten Objekts. Die Auswirkungen können sich innerhalb desselben Objekts überlappen, aber Übergänge sind nicht möglich.

Im folgenden Beispiel wird die Startzeit auf 5 Sekunden und die Endzeit auf 10 Sekunden festgelegt:


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Wenn ein Übergang gerendert wird, wird der Fortschritt des Übergangs bei jedem Frame basierend auf einer **Fortschritts** Eigenschaft berechnet, die zu einem Bereich von 0,0 bis 1,0 normalisiert wird. Des verwendet die Startzeit der einzelnen Frames, um den Fortschritts Wert zu berechnen. Dies bedeutet, **dass der Statuswert,** wenn die Übergangs Endzeit gleich der Quell Endzeit ist, nie genau 1,0 erreicht, da die Startzeit des letzten Frames etwas länger als die Endzeit ist. Legen Sie die Übergangs Endzeit auf mindestens einen Frame vor der Quell Endzeit fest, damit der Übergang 1,0 erreicht werden kann.

**4. Fügen Sie das Objekt in die Zeitachse ein**

Um das Objekt in die Zeitachse einzufügen, müssen Sie je nach Objekttyp eine der folgenden Methoden für das übergeordnete Element abrufen:

-   Effekte: [ **iamtimelineeffectable:: effectinsbefore**](iamtimelineeffectable-effectinsbefore.md)
-   Übergänge: [ **iamtimelinetransable:: transadd**](iamtimelinetransable-transadd.md)

In der [**iamtimelineeffectable:: effectinsbefore**](iamtimelineeffectable-effectinsbefore.md) -Methode müssen Sie die Priorität des Effekts angeben. Wenn sich die Auswirkungen auf das gleiche Objekt überlappen, werden Sie in der Reihenfolge ihrer Priorität angewendet. Der volumeumschlag-Audioeffekt ist eine Ausnahme. Weitere Informationen finden Sie in der Referenz zu [volumeumschlags Effekten](volume-envelope-effect.md) . Innerhalb einer Komposition werden alle Audiospuren gemischt, bevor die Audioeffekte für diese Komposition angewendet werden.

Da Übergänge sich nicht im selben Objekt überlappen können, haben Sie keinen Prioritätswert.

Im folgenden Beispiel wird das Übergangs Objekt zu einer Spur hinzugefügt:


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



Im Beispiel wird das Track-Objekt für die [**iamtimelinetransable**](iamtimelinetransable.md) -Schnittstelle abgefragt, bevor addTrans aufgerufen wird.

**5. Festlegen von Eigenschaften**

Viele Effekte und Übergänge unterstützen benutzerdefinierte Eigenschaften. Weitere Informationen finden Sie unter [Festlegen von Eigenschaften für Effekte und Übergänge](setting-properties-on-effects-and-transitions.md).

Beispiel

Im folgenden Codebeispiel wird ein [SMPTE](smpte-wipe-transition.md) -Umleitungs Übergang zu einer Spur hinzugefügt. Es wird davon ausgegangen, dass das Track-Objekt bereits in der Zeitachse vorhanden ist


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



