---
description: Die Informationen zum ASF-Header werden in den ASF-Header Objekten einer Mediendatei gespeichert.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Informationen aus den ASF-Header Objekten werden erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344632"
---
# <a name="getting-information-from-asf-header-objects"></a>Informationen aus den ASF-Header Objekten werden erhalten.

Die Informationen zum ASF-Header werden in den ASF-Header Objekten einer Mediendatei gespeichert. Media Foundation stellt das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " bereit, um mit dem Header Objekt zu arbeiten. Ein aufgefülltes ContentInfo-Objekt ist erforderlich, damit die Anwendung Header Informationen einer vorhandenen Datei lesen kann. Dies wird erreicht, indem [**imfasfcontentinfo::P arsetheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)aufgerufen wird. Wenn die Verarbeitung erfolgreich abgeschlossen wird, wird die ASF-Bibliothek für die Datei, die intern von Media Foundation verwaltet wird, mit Header Informationen aus verschiedenen Header Objekten aufgefüllt. Einige dieser Eigenschaften werden für die Anwendung verfügbar gemacht, die Sie über Attribute auf den Präsentations Deskriptoren, den Datenstrom Deskriptor, das Profil und die Metadateneigenschaften abrufen kann.

Eine umfassende Liste der Attribute finden Sie unter [Media Foundation Attribute für ASF-Header Objekte](media-foundation-attributes-for-asf-header-objects.md).

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Abrufen von Header Informationen von einem Präsentations Deskriptor

Ein Präsentations deskriptorobjekt enthält die Beschreibung einer bestimmten Medienquelle, in diesem Fall die ASF-Medienquelle. Wenn der " **Parser Header** "-Rückruf erfolgreich abgeschlossen wird, werden Informationen auf Dateiebene aus dem Header Objekt als Attribute im Präsentations Deskriptor gespeichert. Um den Präsentations Deskriptor zu erstellen, rufen Sie [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)auf. Diese Methode gibt einen Zeiger auf ein aufgefülltes Präsentations deskriptorobjekt zurück, das diese Attribute für die dem ContentInfo-Objekt zugeordnete ASF-Datei enthält. Um Werte für bestimmte Attribute abzurufen, nennen Sie **imfattributes:: GetXXX** -Methoden für den Präsentations Deskriptor, und geben Sie das MF PD-Attribut "- **\_ \_ ASF \_ xxx** " an.

Der folgende Beispielcode ruft die Wiedergabedauer einer ASF-Datei ab, die durch ein ContentInfo-Objekt angegeben wird.


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



Weitere Informationen zu Präsentations Deskriptoren im Allgemeinen finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).

Den gesamten Satz von Präsentations deskriptorattributen finden Sie unter [Präsentations deskriptorattribute](presentation-descriptor-attributes.md).

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Abrufen von Header Informationen aus einem Datenstrom Deskriptor

Ein Datenstrom Deskriptor-Objekt macht die [**IMF streamdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) -Schnittstelle verfügbar und beschreibt die Merkmale der Datenströme in der Datei. Der Präsentations Deskriptor für den ASF-Inhalt enthält einen oder mehrere streamdeskriptoren, die die im Header Objekt aufgelisteten Streams darstellen. Nachdem der Aufruf von [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) erfolgreich abgeschlossen wurde, werden die zugrunde liegenden streamdeskriptoren mit Informationen auf Streamebene aus den verschiedenen Header Objekten aufgefüllt. Um einen Datenstrom Deskriptor für einen ASF-Stream abzurufen, nennen Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) für den Präsentations Deskriptor, der aus dem ContentInfo-Objekt generiert wird.

Einige der streameigenschaften werden als Attribute für streamdeskriptoren festgelegt. Aufrufen von **imfattributes:: GetXXX** -Methoden für einen Datenstrom Deskriptor und angeben des **MF SD-Attribut \_ \_ \_ xxx** .

Die gesamten Datenstrom deskriptorattribute finden Sie unter den in den [streamdeskriptorattributen](stream-descriptor-attributes.md)aufgeführten Attributen für den ASF-spezifischen streamdeskriptor.

## <a name="retrieving-header-information-from-the-profile-object"></a>Abrufen von Header Informationen aus dem Profil Objekt

Zusätzlich zu den streamdeskriptoren beschreibt das ASF-Profil Objekt auch die streameigenschaften. Um das Profil einer vorhandenen ASF-Datei abzurufen, nennen Sie [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). Das von dieser Methode zurückgegebene ASF-Profil Objekt enthält keines der **MF \_ PD- \_ ASF \_ xxx** -Attribute. Diese Attribute sind nur für die Anwendung verfügbar, nachdem Sie [**mfkreateasfprofilefrompresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) aufgerufen hat, um das Profil Objekt aus einem Präsentations Deskriptor zu generieren. Sie können das Profil verwenden, um Zeiger auf den gegenseitigen Ausschluss und streampriorisierungsobjekte zu erhalten.

Weitere Informationen zum Profil Objekt finden Sie unter [ASF-Profil](asf-profile.md) .

## <a name="retrieving-metadata-from-header-objects"></a>Abrufen von Metadaten aus Header Objekten

Eine ASF-Datei kann mehrere Metadateneigenschaften enthalten, die während der Datei Codierung festgelegt werden. Eine Anwendung kann diese Eigenschaften mit dem ContentInfo-Objekt auflisten. Einige dieser Eigenschaften, z. b. Informationen zu Variablen Bitraten (VBR), sind für die Anwendung über Attribute auf dem Präsentations Deskriptor, streamdeskriptoren und Medientypen für die Mediendatei verfügbar. Diese Attribute werden für das ContentInfo-Objekt während der Initialisierung durch den Parameter " [**parameseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) " festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-ContentInfo-Objekt](asf-contentinfo-object.md)
</dt> </dl>

 

 



