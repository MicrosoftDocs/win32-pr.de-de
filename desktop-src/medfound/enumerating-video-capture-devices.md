---
description: In diesem Thema wird beschrieben, wie die Video Erfassungsgeräte im Benutzersystem aufgelistet werden und wie eine Instanz eines Geräts erstellt wird.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Auflisten von Video Erfassungs Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393270"
---
# <a name="enumerating-video-capture-devices"></a>Auflisten von Video Erfassungs Geräten

In diesem Thema wird beschrieben, wie die Video Erfassungsgeräte im System des Benutzers aufgelistet werden und wie eine Instanz eines Geräts erstellt wird.

Gehen Sie folgendermaßen vor, um die Video Erfassungsgeräte auf dem System aufzulisten:

1.  Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen. Diese Funktion empfängt einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger.
2.  Aufrufen Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) , um das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) festzulegen. Legen Sie den Attribut Wert auf das **MF \_ devsource- \_ Attribut \_ \_ Quelltyp \_ VidCap \_ GUID** fest.
3.  [**Mfenumschlag mvicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)aufruft. Diese Funktion empfängt ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern und der Array Größe. Jeder Zeiger stellt ein bestimmtes Video Erfassungsgerät dar.

So erstellen Sie eine Instanz eines Aufzeichnungs Geräts:

-   Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) zum Abrufen eines Zeigers auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle.

Diese Schritte sind im folgenden Code dargestellt:


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



Nachdem Sie die Medienquelle erstellt haben, geben Sie die Schnittstellen Zeiger frei, und geben Sie den Speicher für das Array frei:


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



