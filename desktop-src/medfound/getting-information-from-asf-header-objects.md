---
description: ASF-Headerinformationen werden in den ASF-Headerobjekten einer Mediendatei gespeichert.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Abrufen von Informationen aus ASF-Headerobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346e57721137fd6064e4d6b9fd21080d96c10e740bb7f7ed45bf3fef4cc92722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974439"
---
# <a name="getting-information-from-asf-header-objects"></a>Abrufen von Informationen aus ASF-Headerobjekten

ASF-Headerinformationen werden in den ASF-Headerobjekten einer Mediendatei gespeichert. Media Foundation stellt das [ASF ContentInfo-Objekt](asf-contentinfo-object.md) für die Arbeit mit dem Headerobjekt bereit. Ein aufgefülltes ContentInfo-Objekt ist erforderlich, damit die Anwendung Headerinformationen einer vorhandenen Datei lesen kann. Dies wird erreicht, indem [**IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)aufgerufen wird. Wenn die Analyse erfolgreich abgeschlossen wird, wird die ASF-Bibliothek für die Datei, die intern von Media Foundation verwaltet wird, mit Headerinformationen aus verschiedenen Headerobjekten aufgefüllt. Einige dieser Eigenschaften werden für die Anwendung verfügbar gemacht, die sie über Attribute der Präsentationsbeschreibung, des Streamdeskriptors, des Profils und der Metadateneigenschaften abrufen kann.

Die vollständige Liste der Attribute finden Sie unter [Media Foundation Attribute für ASF-Headerobjekte.](media-foundation-attributes-for-asf-header-objects.md)

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Abrufen von Headerinformationen aus einem Präsentationsdeskriptor

Ein Präsentationsdeskriptorobjekt enthält die Beschreibung einer bestimmten Medienquelle, in diesem Fall die ASF-Medienquelle. Wenn der **ParseHeader-Aufruf** erfolgreich abgeschlossen wurde, werden Informationen auf Dateiebene aus dem Headerobjekt als Attribute im Präsentationsdeskriptor gespeichert. Um den Präsentationsdeskriptor zu erstellen, rufen Sie [**IMFASFContentInfo::GeneratePresentationDescriptor auf.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Diese Methode gibt einen Zeiger auf ein aufgefülltes Präsentationsdeskriptorobjekt zurück, das diese Attribute für die ASF-Datei enthält, die dem ContentInfo-Objekt zugeordnet ist. Um Werte für bestimmte Attribute abzurufen, rufen **Sie DIE METHODEN VONATTRIBUTES::Getxxx** für den Präsentationsdeskriptor auf, und geben Sie das **MF PD \_ \_ ASF \_ xxx-Attribut** an.

Der folgende Beispielcode ruft die Wiedergabedauer einer ASF-Datei ab, die von einem ContentInfo-Objekt angegeben wird.


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



Weitere Informationen zu Präsentationsdeskriptoren im Allgemeinen finden Sie unter [Präsentationsdeskriptoren.](presentation-descriptors.md)

Den vollständigen Satz von Präsentationsdeskriptorattributen finden Sie unter [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Abrufen von Headerinformationen aus einem Streamdeskriptor

Ein Streamdeskriptorobjekt macht die [**SCHNITTSTELLE "STREAMSStreamDescriptor"**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) verfügbar und beschreibt die Merkmale der Datenströme in der Datei. Der Präsentationsdeskriptor für den ASF-Inhalt enthält mindestens einen Streamdeskriptor, der die im Headerobjekt aufgeführten Streams darstellt. Nachdem der Aufruf von [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) erfolgreich abgeschlossen wurde, werden die zugrunde liegenden Streamdeskriptoren mit Datenstromebeneninformationen aus den verschiedenen Headerobjekten aufgefüllt. Um einen Streamdeskriptor für einen ASF-Stream abzurufen, rufen [**Sie DIE Generierung VON 2017 auf: "PresentationDescriptor::GetStreamDescriptorByIndex"**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) für den Präsentationsdeskriptor, der aus dem ContentInfo-Objekt generiert wird.

Einige der Streameigenschaften werden als Attribute für Streamdeskriptoren festgelegt. Rufen Sie **DIE ATTRIBUTEAttributes::Getxxx-Methoden** für einen Streamdeskriptor auf, und geben Sie das **MF SD \_ \_ ASF \_ xxx-Attribut** an.

Den vollständigen Satz von Streamdeskriptorattributen finden Sie unter "ASF-Specific Stream Descriptor"-Attribute, die unter [Stream-Deskriptorattribute](stream-descriptor-attributes.md)aufgeführt sind.

## <a name="retrieving-header-information-from-the-profile-object"></a>Abrufen von Headerinformationen aus dem Profilobjekt

Zusätzlich zu Streamdeskriptoren beschreibt das ASF-Profilobjekt auch die Streameigenschaften. Um das Profil einer vorhandenen ASF-Datei abzurufen, rufen [**Sie IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)auf. Das von dieser Methode zurückgegebene ASF-Profilobjekt enthält keines der **MF \_ PD \_ ASF \_ xxx-Attribute.** Diese Attribute sind für die Anwendung erst verfügbar, nachdem [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) zum Generieren des Profilobjekts aus einem Präsentationsdeskriptor aufruft. Sie können das Profil verwenden, um Zeiger auf die Objekte für gegenseitigen Ausschluss und Streampriorisierung abzurufen.

Informationen zum Profilobjekt finden Sie unter [ASF-Profil.](asf-profile.md)

## <a name="retrieving-metadata-from-header-objects"></a>Abrufen von Metadaten aus Headerobjekten

Eine ASF-Datei kann mehrere Metadateneigenschaften enthalten, die während der Dateicodierung festgelegt werden. Eine Anwendung kann diese Eigenschaften mit dem ContentInfo-Objekt aufzählen. Einige dieser Eigenschaften, z. B. Informationen zur variablen Bitrate (Variable Bit Rate, VBR), stehen der Anwendung über Attribute für präsentationsdeskriptor, Streamdeskriptoren und Medientypen für die Mediendatei zur Verfügung. Diese Attribute werden während der Initialisierung über den [**ParseHeader-Aufruf**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) für das ContentInfo-Objekt festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF ContentInfo-Objekt](asf-contentinfo-object.md)
</dt> </dl>

 

 



