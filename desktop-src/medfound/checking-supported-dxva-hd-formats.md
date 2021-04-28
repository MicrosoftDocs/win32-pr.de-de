---
description: Überprüfen der unterstützten DXVA-HD-Formate
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Überprüfen der unterstützten DXVA-HD-Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090008"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="5656f-103">Überprüfen der unterstützten DXVA-HD-Formate</span><span class="sxs-lookup"><span data-stu-id="5656f-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="5656f-104">Überprüfen der unterstützten Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="5656f-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="5656f-105">Gehen Sie wie folgt vor, um eine Liste der Eingabeformate zu erhalten, die vom DXVA-HD-Gerät (Microsoft DirectX Video Acceleration High Definition) unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="5656f-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="5656f-106">Rufen [**Sie IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) auf, um die Gerätefunktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5656f-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="5656f-107">Überprüfen Sie **das InputFormatCount-Member** der [**DXVAHD \_ VPDEVCAPS-Struktur.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="5656f-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="5656f-108">Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.</span><span class="sxs-lookup"><span data-stu-id="5656f-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="5656f-109">Ordnen Sie ein Array von **D3DFORMAT-Werten** der Größe **InputFormatCount zu.**</span><span class="sxs-lookup"><span data-stu-id="5656f-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="5656f-110">Übergeben Sie dieses Array an die [**IDXVAHD \_ Device::GetVideoProcessorInputFormats-Methode.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats)</span><span class="sxs-lookup"><span data-stu-id="5656f-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="5656f-111">Die Methoden füllen das Array mit einer Liste von Eingabeformaten aus.</span><span class="sxs-lookup"><span data-stu-id="5656f-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="5656f-112">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="5656f-112">The following code shows these steps:</span></span>


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



## <a name="checking-supported-output-formats"></a><span data-ttu-id="5656f-113">Überprüfen der unterstützten Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="5656f-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="5656f-114">Gehen Sie wie folgt vor, um eine Liste der Ausgabeformate zu erhalten, die das DXVA-HD-Gerät unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5656f-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="5656f-115">Rufen [**Sie IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) auf, um die Gerätefunktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5656f-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="5656f-116">Überprüfen Sie **das OutputFormatCount-Member** der [**DXVAHD \_ VPDEVCAPS-Struktur.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="5656f-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="5656f-117">Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.</span><span class="sxs-lookup"><span data-stu-id="5656f-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="5656f-118">Ordnen Sie ein Array **von D3DFORMAT-Werten** der Größe **OutputFormatCount zu.**</span><span class="sxs-lookup"><span data-stu-id="5656f-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="5656f-119">Übergeben Sie dieses Array an die [**IDXVAHD \_ Device::GetVideoProcessorOutputFormats-Methode.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats)</span><span class="sxs-lookup"><span data-stu-id="5656f-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="5656f-120">Die Methoden füllen das Array mit einer Liste von Ausgabeformaten aus.</span><span class="sxs-lookup"><span data-stu-id="5656f-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="5656f-121">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="5656f-121">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5656f-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5656f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5656f-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="5656f-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



