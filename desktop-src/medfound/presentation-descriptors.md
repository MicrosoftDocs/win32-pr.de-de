---
description: Präsentations Deskriptoren
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Präsentations Deskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356845"
---
# <a name="presentation-descriptors"></a>Präsentations Deskriptoren

Eine *Präsentation* ist ein Satz verwandter Mediendaten Ströme, die eine gemeinsame Präsentationszeit haben. Eine Präsentation kann z. b. aus den Audio-und Videostreams von einem Film bestehen. Ein *Präsentations Deskriptor* ist ein Objekt, das die Beschreibung einer bestimmten Präsentation enthält. Präsentations Deskriptoren werden verwendet, um Medienquellen und einige Medien senken zu konfigurieren.

Jeder Präsentations Deskriptor enthält eine Liste mit einem oder mehreren Daten *Strom Deskriptoren*. Diese beschreiben die Datenströme in der Präsentation. Datenströme können entweder ausgewählt oder deaktiviert werden. Nur die ausgewählten Streams führen zu Daten. Nicht ausgewählte Streams sind nicht aktiv, und es werden keine Daten erzeugt. Jeder Datenstrom Deskriptor verfügt über einen *Medientyp Handler*, der verwendet wird, um den Medientyp des Streams zu ändern oder den aktuellen Medientyp des Streams zu erhalten. (Weitere Informationen zu Medientypen finden Sie unter [Medientypen](media-types.md).)

In der folgenden Tabelle werden die primären Schnittstellen angezeigt, die von den einzelnen Objekten verfügbar gemacht werden.



| Object                  | Schnittstelle                                                      |
|-------------------------|----------------------------------------------------------------|
| Präsentations Deskriptor | [**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Datenstrom Deskriptor       | [**IMF-Deskriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Medientyp Handler      | [**IMF mediatypeer Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Medienquellen Präsentationen

Jede Medienquelle bietet einen Präsentations Deskriptor, der die Standardkonfiguration für die Quelle beschreibt. In der Standardkonfiguration ist mindestens ein Stream ausgewählt, und jeder ausgewählte Stream weist einen Medientyp auf. Um den Präsentations Deskriptor abzurufen, nennen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Die-Methode gibt einen [**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Zeiger zurück.

Sie können den Präsentations Deskriptor der Quelle ändern, um einen anderen Satz von Streams auszuwählen. Ändern Sie den Präsentations Deskriptor nicht, es sei denn, die Medienquelle wurde beendet. Die Änderungen werden angewendet, wenn Sie [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) zum Starten der Quelle aufruft.

Um die Anzahl der Streams abzurufen, nennen Sie [**imfpresentationdescriptor:: getstreamdescriptorcount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount). Um den Datenstrom Deskriptor für einen Stream abzurufen, nennen Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , und übergeben Sie den Index des Datenstroms. Streams werden von 0 (null) indiziert. Die **getstreamdescriptorbyindex** -Methode gibt einen [**IMF streamdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) -Zeiger zurück. Außerdem wird ein boolesches Flag zurückgegeben, das angibt, ob der Stream ausgewählt ist. Wenn der Stream ausgewählt ist, erzeugt die Medienquelle Daten für diesen Datenstrom. Andernfalls erzeugt die Quelle keine Daten für diesen Stream. Um einen Stream auszuwählen, wenden Sie [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) mit dem Index des Streams an. Um die Auswahl eines Streams zu deaktivieren, nennen Sie [**imfpresentationdescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).

Der folgende Code zeigt, wie der Präsentations Deskriptor aus einer Medienquelle abgerufen und die Streams aufgelistet werden.


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a>Medientyp Handler

Um den Medientyp des Streams zu ändern oder um den aktuellen Medientyp des Streams zu erhalten, verwenden Sie den Medientyp Handler des Stream-Deskriptors. Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) zum Abrufen des Medientyp Handlers. Diese Methode gibt einen [**IMF Media**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) Type-Zeiger zurück.

Wenn Sie einfach wissen möchten, welche Art von Daten im Stream ist (z. b. Audiodaten oder Videos), nennen Sie [**imfmediatyphandler:: getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Diese Methode gibt die GUID für den Haupt Medientyp zurück. Beispielsweise verbindet eine Wiedergabe Anwendung in der Regel einen Audiodatenstrom mit dem audiorenderer und einem Videostream mit dem Videorenderer. Wenn Sie die Medien Sitzung oder das topologielader verwenden, um eine Topologie zu erstellen, ist die GUID des Haupt Typs möglicherweise die einzigen Formatinformationen, die Sie benötigen.

Wenn Ihre Anwendung ausführlichere Informationen zum aktuellen Format benötigt, müssen Sie [**imfmediatyphandler:: getcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype)aufrufen. Diese Methode gibt einen Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle des Medientyps zurück. Verwenden Sie diese Schnittstelle, um die Details des Formats zu erhalten.

Der Medientyp Handler enthält außerdem eine Liste der unterstützten Medientypen für den Datenstrom. Um die Größe der Liste abzurufen, nennen Sie [**imfmediatypehandler:: getmediatypecount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount). Um einen Medientyp aus der Liste abzurufen, nennen Sie [**imfmediatypeer Handler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) mit dem Index des Medientyps. Medientypen werden in der ungefähren Reihenfolge der bevorzugte Reihenfolge zurückgegeben. Für Audioformate werden z. b. höhere Stichproben Raten gegenüber niedrigeren Stichproben Raten bevorzugt. Es gibt jedoch keine definitive Regel, die die Reihenfolge bestimmt, sodass Sie Sie einfach als Richtlinie behandeln sollten.

Die Liste der unterstützten Typen darf nicht alle möglichen Medientypen enthalten, die der Stream unterstützt. Um zu testen, ob ein bestimmter Medientyp unterstützt wird, nennen Sie [**imfmediatypehandler:: ismediatypesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported). Um den Medientyp festzulegen, müssen Sie [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype)aufrufen. Wenn die Methode erfolgreich ausgeführt wird, enthält der Stream Daten, die dem angegebenen Format entsprechen. Die **setcurrentmediatype** -Methode ändert nicht die Liste der bevorzugten Typen.

Der folgende Code zeigt, wie Sie den Medientyp Handler, die bevorzugten Medientypen aufzählen und den Medientyp festlegen. In diesem Beispiel wird davon ausgegangen, dass die Anwendung über einen Algorithmus verfügt, der hier nicht angezeigt wird, um den Medientyp auszuwählen. Die Besonderheiten hängen stark von Ihrer Anwendung ab.


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



