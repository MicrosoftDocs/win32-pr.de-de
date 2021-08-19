---
description: In diesem Thema wird beschrieben, wie sie die Videoaufzeichnungsgeräte auf dem Benutzersystem aufzählen und eine Instanz eines Geräts erstellen.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Aufzählen von Videoaufnahmegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476c4b41e6f8913414200c7a811ba9625f2c4bc9cfea66875ec5f15b788bdc05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061620"
---
# <a name="enumerating-video-capture-devices"></a>Aufzählen von Videoaufnahmegeräten

In diesem Thema wird beschrieben, wie die Videoaufzeichnungsgeräte auf dem System des Benutzers aufzählt und wie eine Instanz eines Geräts erstellt wird.

Gehen Sie wie folgt vor, um die Videoaufzeichnungsgeräte auf dem System aufzuzählen:

1.  Rufen Sie [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attributspeicher zu erstellen. Diese Funktion empfängt einen [**POINTERAttributes-Zeiger.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Rufen Sie [**DIE ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) auf, um das [ATTRIBUT MF \_ DEVSOURCE ATTRIBUTE SOURCE \_ \_ \_ TYPE](mf-devsource-attribute-source-type.md) festzulegen. Legen Sie den Attributwert auf **MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE \_ TYPE \_ \_ VIDCAP \_ GUID fest.**
3.  Rufen Sie [**MFEnumDeviceSources auf.**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) Diese Funktion empfängt ein Array von [**POINTERActivate-Zeigern**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) und die Arraygröße. Jeder Zeiger stellt ein eigenes Videoaufnahmegerät dar.

So erstellen Sie eine Instanz eines Erfassungsgeräts:

-   Rufen Sie [**DIE AKTIONACTIVATE::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um einen Zeiger auf die [**INTERFACESMediaSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) abzurufen.

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



Geben Sie nach dem Erstellen der Medienquelle die Schnittstellenzeiger frei, und geben Sie den Arbeitsspeicher für das Array frei:


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

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



