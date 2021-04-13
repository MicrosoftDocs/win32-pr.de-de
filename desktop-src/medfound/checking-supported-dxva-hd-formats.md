---
description: .
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Überprüfen unterstützter DXVA-HD-Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7560d574cee5fca21ab8de78b01b87af1de5a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484123"
---
# <a name="checking-supported-dxva-hd-formats"></a>Überprüfen unterstützter DXVA-HD-Formate

## <a name="checking-supported-input-formats"></a>Unterstützte Eingabeformate werden überprüft

Gehen Sie folgendermaßen vor, um eine Liste der Eingabeformate zu erhalten, die vom Microsoft DirectX Video Acceleration High Definition-Gerät (DXVA-HD) unterstützt werden:

1.  Wenden Sie [**idxvahd \_ Device:: getvideoprocesordevicecaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) an, um die Gerätefunktionen abzurufen.
2.  Überprüfen Sie den **inputformatcount** -Member der [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur. Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.
3.  Weisen Sie ein Array von **D3DFORMAT** -Werten der Größe **inputformatcount** zu.
4.  Übergeben Sie dieses Array an die [**idxvahd \_ Device:: getvideoprocess orinputformats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) -Methode. Die-Methode füllt das Array mit einer Liste von Eingabe Formaten.

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



## <a name="checking-supported-output-formats"></a>Überprüfen unterstützter Ausgabeformate

Gehen Sie folgendermaßen vor, um eine Liste der Ausgabeformate zu erhalten, die vom DXVA-HD-Gerät unterstützt werden:

1.  Wenden Sie [**idxvahd \_ Device:: getvideoprocesordevicecaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) an, um die Gerätefunktionen abzurufen.
2.  Überprüfen Sie den **outputformatcount** -Member der [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur. Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.
3.  Weisen Sie ein Array von **D3DFORMAT** -Werten der Größe **outputformatcount** zu.
4.  Übergeben Sie dieses Array an die [**idxvahd \_ Device:: getvideoprocess oroutputformats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) -Methode. Die-Methode füllt das Array mit einer Liste von Ausgabeformaten.

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

 

 



