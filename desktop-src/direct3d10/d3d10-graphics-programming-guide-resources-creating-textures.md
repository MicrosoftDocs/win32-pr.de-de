---
description: Eine Textur Ressource ist eine strukturierte Auflistung von Daten.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Erstellen von Textur Ressourcen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958418"
---
# <a name="creating-texture-resources-direct3d-10"></a>Erstellen von Textur Ressourcen (Direct3D 10)

Eine [Textur](d3d10-graphics-programming-guide-resources-types.md) Ressource ist eine strukturierte Auflistung von Daten. Farbwerte werden in der Regel in Texturen gespeichert, und der Zugriff erfolgt während des Renderings durch die [Pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) in verschiedenen Phasen für Eingabe und Ausgabe. Das Erstellen von Texturen und deren Verwendung ist ein wichtiger Bestandteil des Renderings interessanter Szenen in Direct3D 10.

Obwohl Texturen in der Regel Farbinformationen enthalten, ermöglicht das Erstellen von Texturen mit einem anderen [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) es Ihnen, unterschiedliche Arten von Daten zu speichern. Diese Daten können dann von der Direct3D 10-Pipeline auf nicht herkömmliche Weise genutzt werden.

Alle Texturen haben Beschränkungen hinsichtlich des genutzten Speichers und der Anzahl der darin enthaltenen texeln. Diese Grenzwerte werden von [Ressourcen Konstanten](d3d10-graphics-reference-resource-constants.md)angegeben.

-   [Erstellen einer Textur aus einer Datei](#create-a-texture-from-a-file)
    -   [Separates Erstellen von Textur und Ansicht](#create-texture-and-view-separately)
    -   [Gleichzeitiges Erstellen von Textur und Ansicht](#create-texture-and-view-simultaneously)
-   [Erstellen leerer Texturen](#creating-empty-textures)
    -   [Rendering in eine Textur](#rendering-to-a-texture)
    -   [Manuelles Auffüllen von Texturen](#filling-textures-manually)
-   [Mehrere Rendertargets](#multiple-rendertargets)
-   [Zugehörige Themen](#related-topics)

## <a name="create-a-texture-from-a-file"></a>Erstellen einer Textur aus einer Datei

> [!Note]  
> Die [D3DX Utility Library](d3d10-graphics-reference-d3dx10.md) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Wenn Sie eine Textur in Direct3D 10 erstellen, müssen Sie auch eine [Ansicht](d3d10-graphics-programming-guide-resources-access-views.md)erstellen. Eine Sicht ist ein Objekt, das dem Gerät mitteilt, wie während des Renderings auf eine Textur zugegriffen werden soll. Die gängigste Methode, um auf eine Textur zuzugreifen, besteht darin, mithilfe eines [Shaders](../direct3dhlsl/dx-graphics-hlsl.md)aus ihr zu lesen. In einer Shader-Ressourcen Ansicht wird einem Shader mitgeteilt, wie während des Renderings aus einer Textur gelesen werden soll. Die Art der Sicht, die von einer Textur verwendet wird, muss bei der Erstellung angegeben werden.

Das Erstellen einer Textur und das Laden der anfänglichen Daten kann auf zwei verschiedene Arten erfolgen: Erstellen Sie eine Textur und eine separate Ansicht, oder erstellen Sie die Textur und die Ansicht gleichzeitig. Die API stellt beide Techniken bereit, sodass Sie auswählen können, welche für Ihre Anforderungen besser geeignet ist.

### <a name="create-texture-and-view-separately"></a>Separates Erstellen von Textur und Ansicht

Die einfachste Möglichkeit zum Erstellen einer Textur besteht darin, Sie aus einer Bilddatei zu laden. Um die Textur zu erstellen, füllen Sie einfach eine Struktur aus, und geben Sie den Namen der Textur an [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)an.


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



Die D3DX-Funktion [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) führt drei Dinge aus: zunächst erstellt Sie ein Direct3D 10-Textur Objekt. Zweitens wird die Eingabe Bilddatei gelesen. Drittens speichert Sie die Bilddaten im Textur Objekt. Im obigen Beispiel wird eine BMP-Datei geladen, aber die Funktion kann eine Vielzahl von Dateitypen laden.

Das BIND-Flag gibt an, dass die Textur als Shaderressource erstellt wird, sodass eine Shader-Stufe während des Renderings aus der Textur gelesen werden kann.

Im obigen Beispiel werden nicht alle Lade Parameter angegeben. In der Tat ist es häufig vorteilhaft, die Lade Parameter einfach Null auszuwerten, da dies D3DX die Auswahl geeigneter Werte basierend auf dem Eingabebild ermöglicht. Wenn das Eingabebild alle Parameter bestimmen soll, mit denen die Textur erstellt wird, geben Sie einfach **null** für den **loadinfo** -Parameter wie folgt an:


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



Das Angeben von **null** für die ladeinformationen ist eine einfache, aber leistungsstarke Verknüpfung.

Nachdem Sie nun eine Textur erstellt haben, müssen Sie eine Shader-Ressourcen Ansicht erstellen, damit die Textur als Eingabe an einen Shader gebunden werden kann. Da [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) einen Zeiger auf eine Ressource und keinen Zeiger auf eine Textur zurückgibt, müssen Sie den genauen Typ der Ressource ermitteln, die geladen wurde. Anschließend können Sie mithilfe von " [**kreateshaderresourceview**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)" eine Shader-Ressourcen Ansicht erstellen.


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



Obwohl das obige Beispiel eine 2D-Shader-Ressourcen Ansicht erstellt, ist der Code zum Erstellen anderer Shader-Resource-Ansichts Typen sehr ähnlich. Jede Shader-Stufe kann nun diese Textur als Eingabe verwenden.

Die Verwendung von [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und der Verwendung von " [**kreateshaderresourceview**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) " zum Erstellen einer Textur und der zugehörigen Ansicht ist eine Möglichkeit, eine Textur für die Bindung an eine Shader-Phase vorzubereiten. Eine andere Möglichkeit besteht darin, die Textur und ihre Ansicht gleichzeitig zu erstellen. Dies wird im nächsten Abschnitt erläutert.

### <a name="create-texture-and-view-simultaneously"></a>Gleichzeitiges Erstellen von Textur und Ansicht

Direct3D 10 erfordert, dass sowohl eine Textur als auch eine Shader-Ressourcen Ansicht aus einer Textur während der Laufzeit gelesen werden muss. Da die Erstellung einer Textur und einer Shader-Ressourcen Ansicht eine solche häufige Aufgabe ist, stellt D3DX die [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) bereit, um dies für Sie zu tun.


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



Bei einem einzelnen D3DX-Befehl werden sowohl die Textur-als auch die Shader-Ressourcen Ansicht erstellt. Die Funktionalität des **loadinfo** -Parameters ist unverändert. Sie können damit anpassen, wie die Textur erstellt wird, oder die erforderlichen Parameter aus der Eingabedatei ableiten, indem Sie für den **loadinfo** -Parameter **null** angeben.

Das von der [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) -Funktion zurückgegebene [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) -Objekt kann später verwendet werden, um die ursprüngliche [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) -Schnittstelle abzurufen, wenn Sie benötigt wird. Dies kann durch Aufrufen der [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) -Methode erreicht werden.

D3DX bietet eine einzelne Funktion zum Erstellen einer Textur und einer Shader-Ressourcen Ansicht als über-und-Weise. Sie müssen entscheiden, welche Methode zum Erstellen einer Textur und Ansicht am besten den Anforderungen Ihrer Anwendung entspricht.

Nachdem Sie nun wissen, wie eine Textur und die Shader-Ressourcen Ansicht erstellt werden, zeigt der nächste Abschnitt, wie Sie ein Beispiel (lesen) aus dieser Textur mithilfe eines Shaders erstellen können.

## <a name="creating-empty-textures"></a>Erstellen leerer Texturen

Manchmal möchten Anwendungen eine Textur erstellen und die Daten berechnen, die in der Textur gespeichert werden sollen, oder die Grafik [Pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) verwenden, um diese Textur zu rendern und später die Ergebnisse in anderer Verarbeitung zu verwenden. Diese Texturen können von der Grafik Pipeline oder von der Anwendung selbst aktualisiert werden, je nachdem, welche Art von [**Verwendung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) für die Textur bei der Erstellung angegeben wurde.

### <a name="rendering-to-a-texture"></a>Rendering in eine Textur

Der häufigste Fall, eine leere Textur zu erstellen, die während der Laufzeit mit Daten aufgefüllt werden soll, ist der Fall, in dem eine Anwendung in eine Textur gerendert werden soll, und dann die Ergebnisse des Renderingvorgangs in einem nachfolgenden Durchlauf zu verwenden. Mit diesem Zweck erstellte Texturen sollten die Standard [**Verwendung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)angeben.

Im folgenden Codebeispiel wird eine leere Textur erstellt, die von der Pipeline zum Rendering und anschließend als Eingabe für einen [Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)verwendet werden kann.


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



Das Erstellen der Textur erfordert, dass die Anwendung einige Informationen zu den Eigenschaften angibt, die die Textur enthalten wird. Breite und Höhe der Textur in texeln werden auf 256 festgelegt. Für dieses Renderziel ist nur eine einzelne MipMap-Ebene erforderlich. Es ist nur ein Renderziel erforderlich, damit die Array Größe auf 1 festgelegt ist. Jedes Texttyp enthält 4 32-Bit-Gleit Komma Werte, die zum Speichern sehr präziser Informationen verwendet werden können (siehe [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Ein Beispiel pro Pixel ist alles, was benötigt wird. Die Verwendung wird auf Default festgelegt, da dies die effizienteste Platzierung des Renderziels im Arbeitsspeicher ermöglicht. Schließlich wird die Tatsache angegeben, dass die Textur als Renderziel und eine Shaderressource zu unterschiedlichen Zeitpunkten gebunden wird.

Texturen können nicht direkt für das Rendering an die Pipeline gebunden werden. Verwenden Sie eine renderzielansicht, wie im folgenden Codebeispiel gezeigt.


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



Das Format der renderzielansicht wird einfach auf das Format der ursprünglichen Textur festgelegt. Die Informationen in der Ressource sollten als 2D-Textur interpretiert werden, und wir möchten nur die erste MipMap-Ebene des Renderziels verwenden.

Ähnlich wie eine renderzielansicht erstellt werden muss, damit das Renderziel für die Ausgabe an die Pipeline gebunden werden kann, muss eine Shader-Ressourcen Ansicht erstellt werden, sodass das Renderziel als Eingabe an die Pipeline gebunden werden kann. Dies wird im folgenden Codebeispiel veranschaulicht.


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



Die Parameter von Beschreibungen der Shader-Ressourcen Ansicht ähneln denen der Beschreibungen der renderzielsichten und wurden aus denselben Gründen ausgewählt.

### <a name="filling-textures-manually"></a>Manuelles Auffüllen von Texturen

Manchmal möchten Anwendungen Werte zur Laufzeit berechnen, Sie manuell in eine Textur einfügen und dann die Grafik [Pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) in späteren Renderingvorgängen verwenden. Hierzu muss die Anwendung eine leere Textur erstellen, damit die CPU auf den zugrunde liegenden Speicher zugreifen kann. Dies erfolgt durch das Erstellen einer dynamischen Textur und das Erlangen des Zugriffs auf den zugrunde liegenden Speicher, indem eine bestimmte Methode aufgerufen wird. Die erforderliche Vorgehensweise wird im folgenden Codebeispiel veranschaulicht:


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



Beachten Sie, dass das Format auf 32 Bits pro Pixel festgelegt ist, wobei jede Komponente durch 8 Bits definiert wird. Der Usage-Parameter ist auf Dynamic festgelegt, während die Bindungsflags festgelegt werden, um anzugeben, dass ein Shader auf die Textur zugreift. Der Rest der Textur Beschreibung ähnelt der Erstellung eines Renderziels.

Durch Aufrufen von [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) kann die Anwendung auf den zugrunde liegenden Speicher der Textur zugreifen. Der abgerufene Zeiger wird dann verwendet, um die Textur mit Daten zu füllen. Dies ist im folgenden Codebeispiel zu sehen.


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a>Mehrere Rendertargets

Bis zu acht renderzielsichten können gleichzeitig an die Pipeline gebunden werden (mit [**omantrendertargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)). Für jedes Pixel (oder jede Stichprobe, wenn multisamplinggrad aktiviert ist) erfolgt die Mischung unabhängig für jede renderzielansicht. Zwei der Blend-Statusvariablen-blendenable und rendertargetschreitemask-sind Arrays von acht, wobei jedes Array Element einer renderzielansicht entspricht. Wenn mehrere Renderziele verwendet werden, muss jedes Renderziel denselben [Ressourcentyp](d3d10-graphics-programming-guide-resources-types.md) aufweisen (Puffer, 1D-Textur, 2D-Textur Array usw.), und die gleiche Dimension (Breite, Höhe, Tiefe für 3D-Texturen und Array Größe für Textur Arrays) muss vorhanden sein. Wenn die Renderziele Multisampling aufweisen, müssen Sie alle über die gleiche Anzahl von Stichproben pro Pixel verfügen.

Es kann nur ein tiefen Schablone-Puffer aktiv sein, unabhängig davon, wie viele Renderziele aktiv sind. Wenn Textur Arrays als Renderziele verwendet werden, müssen alle Ansichts Dimensionen entsprechend identisch sein. Die Renderziele müssen nicht das gleiche Textur Format aufweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
