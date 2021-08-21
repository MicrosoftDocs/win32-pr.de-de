---
description: Hinzufügen von Effekt- und Übergangsobjekten
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Hinzufügen von Effekt- und Übergangsobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929678759d55a51b022cd7b870ddfa7cc5abb72279bcabe1694b5cc4eef211b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160061"
---
# <a name="adding-effect-and-transition-objects"></a>Hinzufügen von Effekt- und Übergangsobjekten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

In DES wird ein Effekt oder Übergang mit zwei -Objekten dargestellt:

-   Ein *Zeitachsenobjekt* stellt den Effekt oder Übergang innerhalb der Zeitachse dar. Für Effekte unterstützt das Timeline-Objekt die [**IAMTimelineEffect-Schnittstelle.**](iamtimelineeffect.md) Für Übergänge wird die [**IAMTimelineTrans-Schnittstelle**](iamtimelinetrans.md) unterstützt. Beide Typen unterstützen die [**IAMTimelineObj-Schnittstelle.**](iamtimelineobj.md)
-   Das *Unterobjekt* ist ein Objekt, das die Datenverarbeitung für den Effekt oder Übergang implementiert. Das Zeitachsenobjekt enthält einen Zeiger auf das Unterobjekt.

Führen Sie die folgenden Schritte aus, um einen Effekt oder Übergang hinzuzufügen.

**1. Erstellen des Zeitachsenobjekts**

Rufen Sie zum Erstellen des Zeitachsenobjekts die [**IAMTimeline::CreateEmptyNode-Methode**](iamtimeline-createemptynode.md) auf. Legen Sie den Typ für einen Effekt auf **TIMELINE \_ MAJOR TYPE \_ \_ EFFECT** oder für einen Übergang auf **TIMELINE MAJOR TYPE \_ \_ \_ TRANSITION** fest.

Im folgenden Beispiel wird ein Übergangsobjekt erstellt:


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. Angeben des Unterobjekts**

Das Zeitachsenobjekt fungiert als Wrapper für ein anderes Objekt, das als *Unterobjekt* bezeichnet wird und die eigentliche Arbeit übernimmt. Das Unterobjekt implementiert eine Datentransformation, die den gewünschten Effekt oder Übergang erzeugt. Eine Liste der Übergänge und Effekte, die mit DES bereitgestellt werden, finden Sie unter [Übergänge und Effekte.](transitions-and-effects.md)

Rufen Sie zum Festlegen des Unterobjekts die [**IAMTimelineObj::SetSubObjectGUID-Methode**](iamtimelineobj-setsubobjectguid.md) für das Zeitachsenobjekt auf, und übergeben Sie dabei den Klassenbezeichner (CLSID) des Unterobjekts. DirectShow stellt einen Enumerator für Videoeffekte und Videoübergänge bereit, mit dem Sie die CLSID abrufen können. Weitere Informationen finden Sie unter [Aufzählen von Effekten und Übergängen.](enumerating-effects-and-transitions.md)

Im folgenden Beispiel wird der [SMPTE Wipe Transition](smpte-wipe-transition.md) als Unterobjekt festgelegt:


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. Festlegen der Start- und Beendigungszeiten**

Um die Start- und Beendigungszeiten festzulegen, rufen Sie die [**IAMTimelineObj::SetStartStop-Methode**](iamtimelineobj-setstartstop.md) auf. Diese Zeiten sind relativ zur Startzeit des übergeordneten Objekts. Effekte können sich innerhalb desselben Objekts überlappen, Übergänge jedoch nicht.

Im folgenden Beispiel wird die Startzeit auf 5 Sekunden und die Beendigungszeit auf 10 Sekunden festgelegt:


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Wenn ein Übergang gerendert wird, wird der Fortschritt des Übergangs an jedem Frame basierend auf einer **Progress-Eigenschaft** berechnet, die auf einen Bereich von 0,0 bis 1,0 normalisiert wird. DES verwendet die Startzeit jedes Frames, um den Fortschrittswert zu berechnen. Dies bedeutet, dass der Wert **Progress** nie genau 1,0 erreicht, wenn die Beendigungszeit für den Übergang der Quellstoppzeit entspricht, da die Startzeit des letzten Frames geringfügig der Beendigungszeit entspricht. Damit der Übergang 1,0 erreicht, legen Sie die Beendigungszeit für den Übergang auf mindestens einen Frame vor der Quellstoppzeit fest.

**4. Einfügen des Objekts in die Zeitachse**

Um das Objekt in die Zeitachse einzufügen, rufen Sie je nach Objekttyp eine der folgenden Methoden für das übergeordnete Element auf:

-   Effekte: [ **IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   Übergänge: [ **IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)

In der [**IAMTimelineEffectable::EffectInsBefore-Methode**](iamtimelineeffectable-effectinsbefore.md) müssen Sie die Priorität des Effekts angeben. Wenn sich Die Auswirkungen auf dasselbe Objekt überschneiden, werden sie in der Reihenfolge ihrer Priorität angewendet. Der Audioeffekt Volume Envelope ist eine Ausnahme. Weitere Informationen finden Sie in der Referenz zum [VolumeUmschlageffekt.](volume-envelope-effect.md) Innerhalb einer Komposition werden alle Audiospuren gemischt, bevor die Audioeffekte für diese Komposition angewendet werden.

Da sich Übergänge für dasselbe Objekt nicht überlappen können, haben sie keinen Prioritätswert.

Im folgenden Beispiel wird das Übergangsobjekt einer Spur hinzugefügt:


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



Im Beispiel wird das Trackobjekt für die [**IAMTimelineTransable-Schnittstelle**](iamtimelinetransable.md) abgefragt, bevor AddTrans aufgerufen wird.

**5. Festlegen von Eigenschaften**

Viele Effekte und Übergänge unterstützen benutzerdefinierte Eigenschaften. Weitere Informationen finden Sie unter [Festlegen von Eigenschaften für Effekte und Übergänge.](setting-properties-on-effects-and-transitions.md)

Beispiel

Im folgenden Codebeispiel wird einer Spur ein [SMPTE-Zurücksetzungsübergang](smpte-wipe-transition.md) hinzugefügt. Es wird davon ausgegangen, dass das Verfolgungsobjekt bereits in der Zeitachse vorhanden ist.


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

 

 



