---
description: Die csourceseeking-Klasse ist eine abstrakte Klasse für die Implementierung von suchen in Quell Filtern mit einem Ausgabepin.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Csourceseeking-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364748"
---
# <a name="csourceseeking-class"></a>Csourceseeking-Klasse

![csourceseeking-Klassenhierarchie](images/cutil15.png)

Die **csourceseeking** -Klasse ist eine abstrakte Klasse für die Implementierung von suchen in Quell Filtern mit einem Ausgabepin.

Diese Klasse unterstützt die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle. Sie stellt Standard Implementierungen für alle **imediaseeking** -Methoden bereit. Geschützte Member-Variablen speichern die Startzeit, die Endzeit und die aktuelle Rate. Standardmäßig ist das von der-Klasse unterstützte Zeitformat **Zeit \_ Format \_ Medien \_ Zeit** (100-Nanosecond-Einheiten). Weitere Informationen finden Sie unter Hinweise.



| Geschützte Member-Variablen                                          | BESCHREIBUNG                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**m \_ rtduration**](csourceseeking-m-rtduration.md)                | Dauer des Streams.                                                                     |
| [**m \_ rtstart**](csourceseeking-m-rtstart.md)                      | Startzeit.                                                                                 |
| [**m \_ rtstopps**](csourceseeking-m-rtstop.md)                        | Endzeit.                                                                                  |
| [**m \_ drateseeking**](csourceseeking-m-drateseeking.md)            | Wiedergabe Rate.                                                                              |
| [**m \_ dwseekingcaps**](csourceseeking-m-dwseekingcaps.md)          | Suchfunktionen.                                                                       |
| [**m \_ Plock**](csourceseeking-m-plock.md)                          | Zeiger auf ein kritisches Abschnitts Objekt, das gesperrt werden soll.                                           |
| Geschützte Methoden                                                   | BESCHREIBUNG                                                                                 |
| [**Csourceseeking**](csourceseeking-csourceseeking.md)             | Konstruktormethode.                                                                         |
| Reine virtuelle Methoden                                                | BESCHREIBUNG                                                                                 |
| [**Changerate**](csourceseeking-changerate.md)                     | Wird aufgerufen, wenn sich die Wiedergabe Rate ändert.                                                      |
| [**Ändern**](csourceseeking-changestart.md)                   | Wird aufgerufen, wenn die Startposition geändert wird.                                                     |
| [**Changestoppt**](csourceseeking-changestop.md)                     | Wird aufgerufen, wenn die Position des Stopps geändert wird.                                                      |
| Imediaseeking-Methoden                                               | BESCHREIBUNG                                                                                 |
| [**Isformatsupported**](csourceseeking-isformatsupported.md)       | Bestimmt, ob ein angegebenes Zeitformat unterstützt wird.                                    |
| [**Querypreferredformat**](csourceseeking-querypreferredformat.md) | Ruft das bevorzugte Zeitformat des Objekts ab.                                               |
| [**Settimeformat**](csourceseeking-settimeformat.md)               | Legt das Zeitformat fest.                                                                       |
| [**Isusingtimeformat**](csourceseeking-isusingtimeformat.md)       | Bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.                  |
| [**GetTimeFormat**](csourceseeking-gettimeformat.md)               | Ruft das aktuelle Zeitformat ab.                                                          |
| [**Getduration**](csourceseeking-getduration.md)                   | Ruft die Dauer des Streams ab.                                                       |
| [**Getstopposition**](csourceseeking-getstopposition.md)           | Ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird. |
| [**Navigatorobjekt**](csourceseeking-getcurrentposition.md)     | Ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.               |
| [**GetCapabilities**](csourceseeking-getcapabilities.md)           | Ruft alle Suchfunktionen des Streams ab.                                       |
| [**Prüffunktionen**](csourceseeking-checkcapabilities.md)       | Fragt ab, ob der Stream Suchfunktionen angegeben hat.                              |
| [**Converttimeformat**](csourceseeking-converttimeformat.md)       | Konvertiert von einem Zeitformat in ein anderes.                                                   |
| [**Setpositions**](csourceseeking-setpositions.md)                 | Legt die aktuelle Position und die Position des Stopps fest.                                            |
| [**Getpositions**](csourceseeking-getpositions.md)                 | Ruft die aktuelle Position und die Position des Stopps ab.                                       |
| [**Getavailable**](csourceseeking-getavailable.md)                 | Ruft den Zeitraum ab, in dem die Suche effizient ist.                                 |
| [**-Aktivität**](csourceseeking-setrate.md)                           | Legt die Wiedergabe Rate fest.                                                                     |
| [**Getrate**](csourceseeking-getrate.md)                           | Ruft die Wiedergabe Rate ab.                                                                |
| [**Getpreroll**](csourceseeking-getpreroll.md)                     | Ruft die Vorabversion ab.                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Wenn sich die Anfangsposition, die Position der Position oder die Wiedergabe Rate ändert, ruft das **csourceseeking** -Objekt eine entsprechende rein virtuelle Methode auf:

-   Start Position: [ **csourceseeking:: changestart**](csourceseeking-changestart.md)
-   Position des Stopps: [ **csourceseeking:: changestoppt**](csourceseeking-changestop.md)
-   Wiedergabe Rate: [ **csourceseeking:: changerate**](csourceseeking-changerate.md)

Diese Methoden müssen von der abgeleiteten Klasse implementiert werden. Nach jedem Suchvorgang muss ein Filter folgende Aktionen ausführen:

1.  Aufrufen der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für die downstreameingabepin.
2.  Stoppt den Arbeits Thread, der Daten bereitstellt.
3.  Ruft die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für die Eingabe-PIN auf.
4.  Starten Sie den Arbeits Thread neu.
5.  Ruft die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode für die Eingabe-PIN auf.
6.  Legen Sie die Diskontinuität-Eigenschaft im ersten Beispiel fest. Aufrufen der [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode.

Der Aufrufen von [**beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) gibt den Arbeits Thread frei, wenn der Thread blockiert wird, um ein Beispiel zu liefern.

Stellen Sie in Schritt 2 sicher, dass der Thread das Senden von Daten beendet hat. Abhängig von der Implementierung müssen Sie möglicherweise warten, bis der Thread beendet wird, oder wenn der Thread eine Antwort einer Art signalisiert. Wenn der Filter die [**csourcestream**](csourcestream.md) -Klasse verwendet, blockiert die [**csourcestream:: stoppt**](csourcestream-stop.md) -Methode, bis der Arbeits Thread antwortet.

Idealerweise sollte das neue Segment (Schritt 5) vom Arbeits Thread übermittelt werden. Dies kann auch durch das **csourceseeking** -Objekt erfolgen, sofern der Filter es mit den Beispielen serialisiert.

Das folgende Beispiel zeigt eine mögliche Implementierung. Dabei wird davon ausgegangen, dass die Ausgabepin des Quell Filters von **csourceseeking** und [**csourcestream**](csourcestream.md)abgeleitet ist. In diesem Beispiel wird die Hilfsmethode updatefromseek definiert, mit der die Schritte 1 4 ausgeführt werden. Die [**csourcestream:: onthreadstartplay**](csourcestream-onthreadstartplay.md) -Methode wird überschrieben, um das neue Segment zu senden, und um ein Flag festzulegen, das die Diskontinuität angibt. Der Arbeits Thread übernimmt dieses Flag und ruft die [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode auf:


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a>Unterstützung zusätzlicher Zeitformate

Standardmäßig unterstützt diese Klasse das suchen nur in Einheiten der Bezugszeit (Zeit \_ Format \_ Medien \_ Zeit). Um zusätzliche Zeitformate zu unterstützen, überschreiben Sie die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methoden, die sich mit Zeitformaten befassen:

-   [**Imediaseeking:: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**Imediaseeking:: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**Imediaseeking:: isusingtimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**Imediaseeking:: isusingtimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**Imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Überschreiben Sie außerdem die verbleibenden [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methoden, um die erforderlichen Konvertierungen Zwischenzeit Formaten auszuführen. Nachdem die [**settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) -Methode aufgerufen wurde, müssen alle **imediaseeking** -Methoden die eingehenden und ausgehenden Zeitparameter als im neuen Zeitformat behandeln. Wenn die Variable " *m \_ rtduration* " z. b. die Dauer in Einheiten der Verweis Zeit darstellt, das aktuelle Zeitformat aber Frames ist, muss die [**getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode den Wert " *m \_ rtduration* " zurückgeben, der in Frames konvertiert wird. Beispiel:


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



Stellen Sie außerdem sicher, dass Sie \_ \_ in der [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode auf das Flag zum Suchen von returntime achten. Wenn dieses Flag vorhanden ist, konvertieren Sie die Positionswerte in Verweis Zeiten, wenn Sie Sie an den Aufrufer zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützen der Suche in einem Quell Filter](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




