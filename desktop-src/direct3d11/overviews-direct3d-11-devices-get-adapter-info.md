---
title: Vorgehensweise beim erhalten von Adapter Anzeigemodi
description: In diesem Thema wird erläutert, wie Sie die Microsoft DirectX Graphics Infrastructure (DXGI) verwenden, um die einem Adapter zugeordneten gültigen Anzeigemodi zu erhalten.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c2602fcd4e1baa4476bb89273eda676f444e38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315207"
---
# <a name="how-to-get-adapter-display-modes"></a><span data-ttu-id="a02a6-103">Gewusst wie: Anzeigen von Adapter Anzeigemodi</span><span class="sxs-lookup"><span data-stu-id="a02a6-103">How To: Get Adapter Display Modes</span></span>

<span data-ttu-id="a02a6-104">In diesem Thema wird erläutert, wie Sie die Microsoft DirectX Graphics Infrastructure (DXGI) verwenden, um die einem Adapter zugeordneten gültigen Anzeigemodi zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a02a6-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to get the valid display modes associated with an adapter.</span></span> <span data-ttu-id="a02a6-105">DirectX 10 und 11 können DXGI zum Aufrufen der gültigen Anzeigemodi verwenden.</span><span class="sxs-lookup"><span data-stu-id="a02a6-105">DirectX 10 and 11 can use DXGI to get the valid display modes.</span></span> <span data-ttu-id="a02a6-106">Wenn Sie die gültigen Anzeigemodi kennen, wird sichergestellt, dass die Anwendung einen gültigen Vollbildmodus ordnungsgemäß auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="a02a6-106">Knowing the valid display modes ensures that your application can properly choose a valid full-screen mode.</span></span>

<span data-ttu-id="a02a6-107">**So erhalten Sie Adapter Anzeigemodi**</span><span class="sxs-lookup"><span data-stu-id="a02a6-107">**To get adapter display modes**</span></span>

1.  <span data-ttu-id="a02a6-108">Erstellen Sie ein [**idxgifactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) -Objekt, und verwenden Sie es zum Auflisten der verfügbaren Adapter.</span><span class="sxs-lookup"><span data-stu-id="a02a6-108">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object and use it to enumerate the available adapters.</span></span> <span data-ttu-id="a02a6-109">Weitere Informationen finden Sie unter Gewusst [wie: Auflisten von Adaptern](overviews-direct3d-11-devices-enum.md).</span><span class="sxs-lookup"><span data-stu-id="a02a6-109">For more information, see [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).</span></span>
2.  <span data-ttu-id="a02a6-110">Zum Auflisten der Ausgaben für die einzelnen Adapter müssen Sie idxgiadapter:: EnumOutputs aufzählen.</span><span class="sxs-lookup"><span data-stu-id="a02a6-110">Call IDXGIAdapter::EnumOutputs to enumerate the outputs for each adapter.</span></span>
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  <span data-ttu-id="a02a6-111">Rufen Sie idxgioutput:: getdisplaymodelist auf, um ein Array der [**\_ \_ DESC-Strukturen im DXGI-Modus**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) und die Anzahl der Elemente im Array abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a02a6-111">Call IDXGIOutput::GetDisplayModeList to retrieve an array of [**DXGI\_MODE\_DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) structures and the number of elements in the array.</span></span> <span data-ttu-id="a02a6-112">Jede **\_ \_ DESC-Struktur im DXGI-Modus** stellt einen gültigen Anzeigemodus für die Ausgabe dar.</span><span class="sxs-lookup"><span data-stu-id="a02a6-112">Each **DXGI\_MODE\_DESC** structure represents a valid display mode for the output.</span></span>
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="a02a6-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a02a6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a02a6-114">Geräte</span><span class="sxs-lookup"><span data-stu-id="a02a6-114">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="a02a6-115">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a02a6-115">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 