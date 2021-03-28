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
# <a name="how-to-get-adapter-display-modes"></a>Gewusst wie: Anzeigen von Adapter Anzeigemodi

In diesem Thema wird erläutert, wie Sie die Microsoft DirectX Graphics Infrastructure (DXGI) verwenden, um die einem Adapter zugeordneten gültigen Anzeigemodi zu erhalten. DirectX 10 und 11 können DXGI zum Aufrufen der gültigen Anzeigemodi verwenden. Wenn Sie die gültigen Anzeigemodi kennen, wird sichergestellt, dass die Anwendung einen gültigen Vollbildmodus ordnungsgemäß auswählen kann.

**So erhalten Sie Adapter Anzeigemodi**

1.  Erstellen Sie ein [**idxgifactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) -Objekt, und verwenden Sie es zum Auflisten der verfügbaren Adapter. Weitere Informationen finden Sie unter Gewusst [wie: Auflisten von Adaptern](overviews-direct3d-11-devices-enum.md).
2.  Zum Auflisten der Ausgaben für die einzelnen Adapter müssen Sie idxgiadapter:: EnumOutputs aufzählen.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Rufen Sie idxgioutput:: getdisplaymodelist auf, um ein Array der [**\_ \_ DESC-Strukturen im DXGI-Modus**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) und die Anzahl der Elemente im Array abzurufen. Jede **\_ \_ DESC-Struktur im DXGI-Modus** stellt einen gültigen Anzeigemodus für die Ausgabe dar.
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

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 