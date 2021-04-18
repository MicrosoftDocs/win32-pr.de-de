---
description: Die cpospassthru-Klasse verarbeitet Such Befehle für Transformations Filter, indem Sie vom Upstream an den nächsten Filter übergeben werden.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Cpospassthru-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372077"
---
# <a name="cpospassthru-class"></a>Cpospassthru-Klasse

![cpospassthru-Basisklassen Hierarchie](images/cutil14.png)

Die- `CPosPassThru` Klasse verarbeitet Such Befehle für Transformations Filter, indem Sie vom Upstream an den nächsten Filter übergeben werden.

Wenn eine Anwendung das Filter Diagramm sucht, übergibt der Filter Diagramm-Manager den rendererfiltern den Suchbefehl. Der Befehl wird über die Ausgabepin jedes Filters Upstream übergeben, bis ein Filter erreicht wird, der den Befehl ausführen kann (sofern vorhanden). Weitere Informationen finden Sie unter [Suchen](seeking.md). Die- `CPosPassThru` Klasse übergibt alle Suchbefehle an die Ausgabepin im upstreamfilter, wie im folgenden Diagramm dargestellt.

![die cpospassthru-Klasse sendet Seek-Befehle Upstream.](images/cpospassthru.png)

Obwohl diese Klasse in der Basisklassen Bibliothek bereitgestellt wird, stellt DirectShow auch dieselbe Klasse in Quartz.dll bereit. Wenn Sie die Quartz.dll-Version verwenden, kann die Codegröße in Ihrem Filter einigermaßen reduziert werden, da die-Klasse zur Laufzeit aus der DLL geladen wird. Um diese Version zu verwenden, müssen Sie [**die Funktion "**](createpospassthru.md) -Funktion" aufrufen.

Delegieren Sie in der **nondelegatingqueryinterface** -Methode der Ausgabe-PIN immer dann an das **cpospassthru** -Objekt, wenn die angeforderte Schnittstelle [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) oder [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition)ist, wie im folgenden Code gezeigt:


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



Sofern nicht angegeben, rufen alle [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methoden in dieser Klasse die entsprechende Methode für die verbundene PIN auf und geben das Ergebnis zurück.



| Öffentliche Methoden                                                    | BESCHREIBUNG                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Cpospassthru**](cpospassthru-cpospassthru.md)                 | Konstruktormethode.                                                                                 |
| [**ForceRefresh**](cpospassthru-forcerefresh.md)                 | Veraltet.                                                                                           |
| [**Getmediatime**](cpospassthru-getmediatime.md)                 | Ruft die Zeitstempel im aktuellen Beispiel ab. Virtu.                                           |
| Imediaposition-Methoden                                            | BESCHREIBUNG                                                                                         |
| [**\_Dauer erhalten**](cpospassthru-get-duration.md)                | Ruft die Dauer des Streams ab.                                                               |
| [**\_CurrentPosition platzieren**](cpospassthru-put-currentposition.md)  | Legt die aktuelle Position relativ zur Gesamtdauer des Streams fest.                            |
| [**\_Stopp Zeit erhalten**](cpospassthru-get-stoptime.md)                | Ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird.         |
| [**\_Stopp Zeit einfügen**](cpospassthru-put-stoptime.md)                | Legt die Uhrzeit fest, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird.              |
| [**\_vorab Zeit**](cpospassthru-get-prerolltime.md)          | Ruft die Datenmenge ab, die vor der Startposition in die Warteschlange eingereiht wird.                         |
| [**\_vorab Zeit festlegen**](cpospassthru-put-prerolltime.md)          | Legt die Menge der Daten fest, die vor der Startposition in die Warteschlange eingereiht werden.                              |
| [**get- \_ Rate**](cpospassthru-get-rate.md)                        | Ruft die Wiedergabe Rate ab.                                                                        |
| [**Put- \_ Rate**](cpospassthru-put-rate.md)                        | Legt die Wiedergabe Rate fest.                                                                             |
| [**\_CurrentPosition erhalten**](cpospassthru-get-currentposition.md)  | Ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.                       |
| [**Canseekforward**](cpospassthru-canseekforward.md)             | Bestimmt, ob der Stream rückwärts Seeding durchgeführt werden kann.                                               |
| [**Canseekabwärts**](cpospassthru-canseekbackward.md)           | Bestimmt, ob für den Datenstrom ein Seeding durchgeführt werden kann.                                                |
| Imediaseeking-Methoden                                             | BESCHREIBUNG                                                                                         |
| [**Prüffunktionen**](cpospassthru-checkcapabilities.md)       | Fragt ab, ob ein Stream Suchfunktionen angegeben hat.                                        |
| [**Converttimeformat**](cpospassthru-converttimeformat.md)       | Konvertiert von einem Zeitformat in ein anderes.                                                           |
| [**Getavailable**](cpospassthru-getavailable.md)                 | Ruft den Zeitraum ab, in dem die Suche effizient ist.                                         |
| [**GetCapabilities**](cpospassthru-getcapabilities.md)           | Ruft alle Suchfunktionen des Streams ab.                                               |
| [**Navigatorobjekt**](cpospassthru-getcurrentposition.md)     | Ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.                       |
| [**Getduration**](cpospassthru-getduration.md)                   | Ruft die Dauer des Streams ab.                                                               |
| [**Getpositions**](cpospassthru-getpositions.md)                 | Ruft die aktuelle Position und die Position des Stopps relativ zur Gesamtdauer des Streams ab. |
| [**Getpreroll**](cpospassthru-getpreroll.md)                     | Ruft die Datenmenge ab, die vor der Startposition in die Warteschlange eingereiht wird.                         |
| [**Getrate**](cpospassthru-getrate.md)                           | Ruft die Wiedergabe Rate ab.                                                                        |
| [**Getstopposition**](cpospassthru-getstopposition.md)           | Ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird.         |
| [**GetTimeFormat**](cpospassthru-gettimeformat.md)               | Ruft das aktuelle Zeitformat ab.                                                                  |
| [**Isformatsupported**](cpospassthru-isformatsupported.md)       | Bestimmt, ob ein angegebenes Zeitformat unterstützt wird.                                            |
| [**Isusingtimeformat**](cpospassthru-isusingtimeformat.md)       | Bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.                          |
| [**Querypreferredformat**](cpospassthru-querypreferredformat.md) | Ruft das bevorzugte Zeitformat für den Stream ab.                                                 |
| [**Setpositions**](cpospassthru-setpositions.md)                 | Legt die aktuelle Position und die Position des Stopps fest.                                                    |
| [**-Aktivität**](cpospassthru-setrate.md)                           | Legt die Wiedergabe Rate fest.                                                                             |
| [**Settimeformat**](cpospassthru-settimeformat.md)               | Legt das Zeitformat fest.                                                                               |
| Hilfsfunktionen                                                  | BESCHREIBUNG                                                                                         |
| [**"Kreatepospassthru"**](createpospassthru.md)                    | Erstellt ein- `CPosPassThru` oder [**crendererpospassthru**](crendererpospassthru.md) -Objekt.            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




