---
title: How To Get Adapter Display Modes
description: In diesem Thema wird gezeigt, wie Sie microsoft DirectX Graphic Infrastructure (DXGI) verwenden, um die gültigen Anzeigemodi zu erhalten, die einem Adapter zugeordnet sind.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921d373a9ff0f79baaf848a55cbab0d08fd4e119d30a0a0cb917832830589dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119570"
---
# <a name="how-to-get-adapter-display-modes"></a>How To: Get Adapter Display Modes

In diesem Thema wird gezeigt, wie Sie microsoft DirectX Graphic Infrastructure (DXGI) verwenden, um die gültigen Anzeigemodi zu erhalten, die einem Adapter zugeordnet sind. DirectX 10 und 11 können DXGI verwenden, um die gültigen Anzeigemodi zu erhalten. Wenn Sie die gültigen Anzeigemodi kennen, wird sichergestellt, dass Ihre Anwendung einen gültigen Vollbildmodus ordnungsgemäß auswählen kann.

**So erhalten Sie Adapteranzeigemodi**

1.  Erstellen Sie ein [**IDXGIFactory-Objekt,**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) und verwenden Sie es zum Aufzählen der verfügbaren Adapter. Weitere Informationen finden Sie unter [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).
2.  Rufen Sie IDXGIAdapter::EnumOutputs auf, um die Ausgaben für jeden Adapter aufzählen.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Rufen Sie IDXGIOutput::GetDisplayModeList auf, um ein Array von [**DXGI \_ MODE \_ DESC-Strukturen**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) und die Anzahl der Elemente im Array abzurufen. Jede **DXGI \_ MODE \_ DESC-Struktur** stellt einen gültigen Anzeigemodus für die Ausgabe dar.
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

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 