---
description: Überprüfen der unterstützten DXVA-HD-Formate
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Überprüfen der unterstützten DXVA-HD-Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b28586148bb96a918c8a230a25ff1477af73e0604d3b62e11e644e8276b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035408"
---
# <a name="checking-supported-dxva-hd-formats"></a>Überprüfen der unterstützten DXVA-HD-Formate

## <a name="checking-supported-input-formats"></a>Überprüfen der unterstützten Eingabeformate

Gehen Sie wie folgt vor, um eine Liste der Eingabeformate abzurufen, die das Dxva-HD-Gerät (Video Acceleration High Definition) von Microsoft DirectX unterstützt:

1.  Rufen Sie [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) auf, um die Gerätefunktionen abzurufen.
2.  Überprüfen Sie den **InputFormatCount-Member** der [**DXVAHD \_ VPDEVCAPS-Struktur.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.
3.  Ordnen Sie ein Array von **D3DFORMAT-Werten** der Größe **InputFormatCount** zu.
4.  Übergeben Sie dieses Array an die [**IDXVAHD \_ Device::GetVideoProcessorInputFormats-Methode.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) Die -Methoden füllen das Array mit einer Liste von Eingabeformaten aus.

Diese Schritte sind im folgenden Code dargestellt:


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a>Überprüfen der unterstützten Ausgabeformate

Gehen Sie wie folgt vor, um eine Liste der Ausgabeformate abzurufen, die das DXVA-HD-Gerät unterstützt:

1.  Rufen Sie [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) auf, um die Gerätefunktionen abzurufen.
2.  Überprüfen Sie den **OutputFormatCount-Member** der [**DXVAHD-VPDEVCAPS-Struktur. \_**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.
3.  Ordnen Sie ein Array von **D3DFORMAT-Werten** der Größe **OutputFormatCount** zu.
4.  Übergeben Sie dieses Array an die [**IDXVAHD \_ Device::GetVideoProcessorOutputFormats-Methode.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) Die -Methoden füllen das Array mit einer Liste von Ausgabeformaten aus.

Diese Schritte sind im folgenden Code dargestellt:


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



