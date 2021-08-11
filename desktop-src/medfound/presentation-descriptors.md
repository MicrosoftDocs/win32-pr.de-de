---
description: Präsentationsdeskriptoren
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Präsentationsdeskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963faeebbb180b504cc11202645a9432bbb3a94e988495b9ddcf96e550b05519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238831"
---
# <a name="presentation-descriptors"></a>Präsentationsdeskriptoren

Bei *einer Präsentation* handelt es sich um eine Reihe verwandter Medienstreams, die eine gemeinsame Präsentationszeit gemeinsam haben. Eine Präsentation kann beispielsweise aus audio- und videostreams aus einem Film bestehen. Ein *Präsentationsdeskriptor* ist ein Objekt, das die Beschreibung einer bestimmten Präsentation enthält. Präsentationsdeskriptoren werden verwendet, um Medienquellen und einige Mediensenken zu konfigurieren.

Jeder Präsentationsdeskriptor enthält eine Liste mit mindestens einem *Streamdeskriptor.* Diese beschreiben die Streams in der Präsentation. Streams kann entweder ausgewählt oder deaktiviert werden. Nur die ausgewählten Datenströme erzeugen Daten. Deaktivierte Streams sind nicht aktiv und erzeugen keine Daten. Jeder Streamdeskriptor verfügt über einen Medientyphandler, der verwendet wird, um den Medientyp des Streams zu ändern oder den aktuellen Medientyp des Streams zu erhalten. (Weitere Informationen zu Medientypen finden Sie unter [Medientypen](media-types.md).)

Die folgende Tabelle zeigt die primären Schnittstellen, die jedes dieser Objekte verfügbar macht.



| Object                  | Schnittstelle                                                      |
|-------------------------|----------------------------------------------------------------|
| Präsentationsdeskriptor | [**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Streamdeskriptor       | [**JAVASCRIPTStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Medientyphandler      | [**DELEGATEMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Medienquellenpräsentationen

Jede Medienquelle bietet einen Präsentationsdeskriptor, der die Standardkonfiguration für die Quelle beschreibt. In der Standardkonfiguration ist mindestens ein Stream ausgewählt, und jeder ausgewählte Stream hat einen Medientyp. Um den Präsentationsdeskriptor zu erhalten, rufen [**Sie DANNMediaSource::CreatePresentationDescriptor auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) Die -Methode gibt einen [**-ZEIGER VOM-Wert FÜR DIEPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) zurück.

Sie können den Präsentationsdeskriptor der Quelle ändern, um einen anderen Satz von Streams auszuwählen. Ändern Sie den Präsentationsdeskriptor nur, wenn die Medienquelle beendet wurde. Die Änderungen werden angewendet, wenn Sie zum Starten der Quelle [**DEN AUFRUF VON DURCHEMEDIASource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) vornehmen.

Um die Anzahl der Streams zu erhalten, rufen [**Sie DIEPRESENTPresentationDescriptor::GetStreamDescriptorCount auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) Um den Streamdeskriptor für einen Stream zu erhalten, rufen Sie [**DIEPRESENTPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) auf, und übergeben Sie den Index des Streams. Streams werden von 0 (null) indiziert. Die **GetStreamDescriptorByIndex-Methode** gibt einen [**ATTRIBUTSTREAMDescriptor-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) zurück. Außerdem wird ein boolesches Flag zurückgegeben, das angibt, ob der Stream ausgewählt ist. Wenn der Stream ausgewählt ist, erzeugt die Medienquelle Daten für diesen Stream. Andernfalls erzeugt die Quelle keine Daten für diesen Stream. Um einen Stream auszuwählen, rufen Sie [**DIEPRESENTPresentationDescriptor::SelectStream mit**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) dem Index des Streams auf. Um die Auswahl eines Streams aufzuheben, rufen [**Sie DANNPresentationDescriptor::D eselectStream auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)

Der folgende Code zeigt, wie Sie den Präsentationsdeskriptor aus einer Medienquelle erhalten und die Streams aufzählen.


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



## <a name="media-type-handlers"></a>Medientyphandler

Um den Medientyp des Streams zu ändern oder den aktuellen Medientyp des Streams zu erhalten, verwenden Sie den Medientyphandler des Streamdeskriptors. Rufen [**Sie DIESTREAMDescriptor::GetMediaTypeHandler auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) um den Medientyphandler zu erhalten. Diese Methode gibt einen [**METHODENMEDIATypeHandler-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) zurück.

Wenn Sie einfach wissen möchten, welche Art von Daten im Stream vorkommt, z. B. Audio oder Video, rufen Sie [**DEN TYP Handler::GetMajorType auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype) Diese Methode gibt die GUID für den Hauptmedientyp zurück. Beispielsweise verbindet eine Wiedergabeanwendung in der Regel einen Audiostream mit dem Audiorenderer und einen Videostream mit dem Videorenderer. Wenn Sie die Mediensitzung oder das Topologielader verwenden, um eine Topologie zu erstellen, ist die Haupttyp-GUID möglicherweise die einzige Formatinformation, die Sie benötigen.

Wenn Ihre Anwendung ausführlichere Informationen zum aktuellen Format benötigt, rufen Sie [**DIEMEDIATypeHandler::GetCurrentMediaType auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) Diese Methode gibt einen Zeiger auf die [**BESCHRIFTUNGMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) des Medientyps zurück. Verwenden Sie diese Schnittstelle, um die Details des Formats zu erhalten.

Der Medientyphandler enthält auch eine Liste der unterstützten Medientypen für den Stream. Um die Größe der Liste zu erhalten, rufen [**SieGEMEDIATypeHandler::GetMediaTypeCount auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) Um einen Medientyp aus der Liste zu erhalten, rufen Sie [**DIEMEDIATypeHandler::GetMediaTypeByIndex mit**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) dem Index des Medientyps auf. Medientypen werden in der ungefähren Reihenfolge ihrer Präferenz zurückgegeben. Bei Audioformaten werden beispielsweise höhere Abtastraten gegenüber niedrigeren Abtastraten bevorzugt. Es gibt jedoch keine definitive Regel, die die Reihenfolge steuert, daher sollten Sie sie einfach als Richtlinie behandeln.

Die Liste der unterstützten Typen enthält möglicherweise nicht alle möglichen Medientypen, die der Stream unterstützt. Um zu testen, ob ein bestimmter Medientyp unterstützt wird, rufen [**Sie DIEMEDIATypeHandler::IsMediaTypeSupported auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported) Rufen Sie zum Festlegen des Medientyps [**DIEMEDIATypeHandler::SetCurrentMediaType auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) Wenn die Methode erfolgreich ist, enthält der Stream Daten, die dem angegebenen Format entsprechen. Die **SetCurrentMediaType-Methode** ändert die Liste der bevorzugten Typen nicht.

Der folgende Code zeigt, wie sie den Medientyphandler erhalten, die bevorzugten Medientypen aufzählen und den Medientyp festlegen. In diesem Beispiel wird davon ausgegangen, dass die Anwendung über einen Algorithmus verfügt, der hier nicht gezeigt wird, um den Medientyp auszuwählen. Die Besonderheiten hängen stark von Ihrer Anwendung ab.


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

[Media Foundation-Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



