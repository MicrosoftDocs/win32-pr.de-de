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
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="6cf58-103">Überprüfen unterstützter DXVA-HD-Formate</span><span class="sxs-lookup"><span data-stu-id="6cf58-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="6cf58-104">Unterstützte Eingabeformate werden überprüft</span><span class="sxs-lookup"><span data-stu-id="6cf58-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="6cf58-105">Gehen Sie folgendermaßen vor, um eine Liste der Eingabeformate zu erhalten, die vom Microsoft DirectX Video Acceleration High Definition-Gerät (DXVA-HD) unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="6cf58-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="6cf58-106">Wenden Sie [**idxvahd \_ Device:: getvideoprocesordevicecaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) an, um die Gerätefunktionen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6cf58-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="6cf58-107">Überprüfen Sie den **inputformatcount** -Member der [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur.</span><span class="sxs-lookup"><span data-stu-id="6cf58-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="6cf58-108">Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.</span><span class="sxs-lookup"><span data-stu-id="6cf58-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="6cf58-109">Weisen Sie ein Array von **D3DFORMAT** -Werten der Größe **inputformatcount** zu.</span><span class="sxs-lookup"><span data-stu-id="6cf58-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="6cf58-110">Übergeben Sie dieses Array an die [**idxvahd \_ Device:: getvideoprocess orinputformats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6cf58-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="6cf58-111">Die-Methode füllt das Array mit einer Liste von Eingabe Formaten.</span><span class="sxs-lookup"><span data-stu-id="6cf58-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="6cf58-112">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="6cf58-112">The following code shows these steps:</span></span>


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



## <a name="checking-supported-output-formats"></a><span data-ttu-id="6cf58-113">Überprüfen unterstützter Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="6cf58-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="6cf58-114">Gehen Sie folgendermaßen vor, um eine Liste der Ausgabeformate zu erhalten, die vom DXVA-HD-Gerät unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="6cf58-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="6cf58-115">Wenden Sie [**idxvahd \_ Device:: getvideoprocesordevicecaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) an, um die Gerätefunktionen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6cf58-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="6cf58-116">Überprüfen Sie den **outputformatcount** -Member der [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur.</span><span class="sxs-lookup"><span data-stu-id="6cf58-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="6cf58-117">Dieser Member gibt die Anzahl der unterstützten Eingabeformate an.</span><span class="sxs-lookup"><span data-stu-id="6cf58-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="6cf58-118">Weisen Sie ein Array von **D3DFORMAT** -Werten der Größe **outputformatcount** zu.</span><span class="sxs-lookup"><span data-stu-id="6cf58-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="6cf58-119">Übergeben Sie dieses Array an die [**idxvahd \_ Device:: getvideoprocess oroutputformats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6cf58-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="6cf58-120">Die-Methode füllt das Array mit einer Liste von Ausgabeformaten.</span><span class="sxs-lookup"><span data-stu-id="6cf58-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="6cf58-121">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="6cf58-121">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6cf58-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cf58-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cf58-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="6cf58-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



