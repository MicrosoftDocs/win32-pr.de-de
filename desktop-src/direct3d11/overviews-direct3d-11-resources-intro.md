---
title: Einführung in eine Ressource in Direct3D 11
description: In diesem Thema werden Direct3D-Ressourcen wie Puffer und Texturen beschrieben.
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cc6f9ba62bdfedc59ff2a152588ccad3d81423d55f8c230ff3836c52e5251d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098245"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Einführung in eine Ressource in Direct3D 11

Ressourcen sind die Bausteine Ihrer Szene. Sie enthalten die meisten Daten, die Direct3D zum Interpretieren und Rendern Ihrer Szene verwendet. Ressourcen sind Bereiche im Arbeitsspeicher, auf die die Direct3D-Pipeline zugreifen kann. Ressourcen enthalten die folgenden Datentypen: Geometrie, Texturen, Shaderdaten. In diesem Thema werden Direct3D-Ressourcen wie Puffer und Texturen beschrieben.

Sie können Ressourcen erstellen, die stark typiert oder typlos sind. Sie können steuern, ob Ressourcen sowohl Lese- als auch Schreibzugriff haben. Sie können Ressourcen nur für die CPU, GPU oder beides zugänglich machen. Für jede Pipelinephase können bis zu 128 Ressourcen aktiv sein.

Direct3D garantiert, dass 0 (null) für jede Ressource zurückgesetzt wird, auf die über grenzenlose Grenzen zugegriffen wird.

Der Lebenszyklus einer Direct3D-Ressource ist:

-   Erstellen Sie eine Ressource mit einer der Erstellungsmethoden der [**ID3D11Device-Schnittstelle.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)
-   Binden Sie eine Ressource mithilfe eines Kontexts und einer der festgelegten Methoden der [**ID3D11DeviceContext-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) an die Pipeline.
-   Geben Sie die Ressourcenzuordnung auf, indem Sie die [**Release-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) der Ressourcenschnittstelle aufrufen.

Dieser Abschnitt enthält die folgenden Themen:

-   [Starke und schwache Typisierung](#strong-vs-weak-typing)
-   [Ressourcenansichten](#resource-views)
-   [Unformatiert von Pufferansichten](#raw-views-of-buffers)
-   [Zugehörige Themen](#related-topics)

## <a name="strong-vs-weak-typing"></a>Starke und schwache Typisierung

Es gibt zwei Möglichkeiten, das Layout (oder den Speicherbedarf) einer Ressource vollständig anzugeben:

-   Typ: Geben Sie den Typ vollständig an, wenn die Ressource erstellt wird.
-   Typlos: Geben Sie den Typ vollständig an, wenn die Ressource an die Pipeline gebunden ist.

Durch das Erstellen einer vollständig typierten Ressource wird die Ressource auf das Format beschränkt, mit dem sie erstellt wurde. Dadurch kann die Runtime den Zugriff optimieren, insbesondere wenn die Ressource mit Flags erstellt wird, die angeben, dass sie nicht von der Anwendung zugeordnet werden kann. Ressourcen, die mit einem bestimmten Typ erstellt wurden, können nicht mithilfe des Ansichtsmechanismus neu interpretiert werden, es sei denn, die Ressource wurde mit dem DDI BIND PRESENT-Flag D3D10 \_ \_ \_ erstellt. Wenn D3D10 DDI BIND PRESENT festgelegt ist, können Renderziel- oder Shaderressourcenansichten für diese Ressourcen mit einem der vollständig typierten Member der entsprechenden Familie erstellt werden, selbst wenn die ursprüngliche Ressource als vollständig typiert erstellt \_ \_ \_ wurde.

In einer Ressource vom Typ "Weniger" ist der Datentyp unbekannt, wenn die Ressource zum ersten Mal erstellt wird. Die Anwendung muss aus den verfügbaren Formaten mit weniger Formaten wählen (siehe [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Sie müssen die Größe des zu reservierenden Arbeitsspeichers angeben und angeben, ob die Runtime die Untertexture in einer Mipmap generieren muss. Das genaue Datenformat (ob der Arbeitsspeicher als ganze Zahlen, Gleitkommawerte, ganze Zahlen ohne Vorzeichen usw.) wird jedoch erst bestimmt, wenn die Ressource mit einer Ressourcenansicht an die Pipeline gebunden [ist.](#resource-views) Da das Texturformat flexibel bleibt, bis die Textur an die Pipeline gebunden ist, wird die Ressource als schwach typisieren Speicher bezeichnet. Schwach typ getypter Speicher hat den Vorteil, dass er in einem anderen Format wiederverwendet oder neu interpretiert werden kann, solange die Anzahl der Komponenten und die Bitanzahl jeder Komponente in beiden Formaten identisch sind.

Eine einzelne Ressource kann an mehrere Pipelinestufen gebunden werden, solange jede über eine eindeutige Ansicht verfügt, die die Formate an jedem Standort vollständig qualifiziert. Beispielsweise kann eine Ressource, die mit dem Format DXGI \_ FORMAT \_ R32G32B32A32 TYPELESS erstellt wurde, gleichzeitig als \_ \_ DXGI FORMAT \_ R32G32B32A32A32 FLOAT und \_ dxgi \_ FORMAT \_ R32G32B32A32A32 \_ UINT an verschiedenen Stellen in der Pipeline verwendet werden.

## <a name="resource-views"></a>Ressourcenansichten

Ressourcen können in allgemeinen Speicherformaten gespeichert werden, sodass sie von mehreren Pipelinestufen gemeinsam genutzt werden können. Eine Pipelinephase interpretiert Ressourcendaten mithilfe einer Ansicht. Eine Ressourcenansicht ähnelt konzeptionell der Umwandlung der Ressourcendaten, sodass sie in einem bestimmten Kontext verwendet werden kann.

Eine Ansicht kann mit einer typlosen Ressource verwendet werden. Das heißt, Sie können eine Ressource zur Kompilierzeit erstellen und den Datentyp deklarieren, wenn die Ressource an die Pipeline gebunden ist. Eine Ansicht, die für eine typlose Ressource erstellt wurde, verfügt immer über die gleiche Anzahl von Bits pro Komponente. die Art und Weise, wie die Daten interpretiert werden, hängt vom angegebenen Format ab. Das angegebene Format muss aus derselben Familie wie das typlose Format beim Erstellen der Ressource sein. Beispielsweise kann eine Ressource, die mit dem TYPELESS-Format R8G8B8A8 erstellt wurde, nicht als R32 FLOAT-Ressource angezeigt werden, obwohl beide Formate im Arbeitsspeicher die gleiche Größe \_ \_ haben können.

Eine Ansicht macht auch andere Funktionen verfügbar, z. B. die Möglichkeit, Tiefen-/Schablonenoberflächen in einem Shader zurücklesen, eine dynamische Cubemap in einem einzelnen Durchgang zu generieren und gleichzeitig in mehreren Slices eines Volumes zu rendern.



| Ressourcenschnittstelle                                             | Beschreibung                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | Greifen Sie während des Tiefen-Schablonentests auf eine Texturressource zu.                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | Greifen Sie auf eine Texturressource zu, die als Renderziel verwendet wird.                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | Greifen Sie auf eine Shaderressource wie einen konstanten Puffer, einen Texturpuffer, eine Textur oder einen Sampler zu. |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | Greifen Sie mit einem Pixel-Shader oder einem Compute-Shader auf eine ungeordnete Ressource zu.                        |



 

## <a name="raw-views-of-buffers"></a>Unformatiert von Pufferansichten

Sie können sich einen unformatierten Puffer, der auch als [Byteadressenpuffer](direct3d-11-advanced-stages-cs-resources.md)bezeichnet werden kann, als eine Tüte von Bits, auf die Sie rohen Zugriff wünschen, also einen Puffer, auf den Sie bequem über Block von ein bis vier typlosen 32-Bit-Adresswerten zugreifen können. Sie geben an, dass Sie rohen Zugriff auf einen Puffer (oder eine rohe Ansicht eines Puffers) wünschen, wenn Sie eine der folgenden Methoden aufrufen, um eine Ansicht für den Puffer zu erstellen:

-   Um eine Shaderressourcenansicht (SRV) für den Puffer zu erstellen, rufen Sie [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) mit dem [**Flag D3D11 \_ BUFFEREX \_ SRV \_ FLAG RAW \_ auf.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag) Sie geben dieses Flag im **Flags-Member** der [**\_ BUFFEREX \_ SRV-Struktur D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv) an. Sie legen **D3D11 \_ BUFFEREX \_ SRV** im **BufferEx-Member** der [**D3D11 \_ SHADER \_ RESOURCE VIEW \_ \_ DESC-Struktur**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) fest, auf die der *pDesc-Parameter* von **ID3D11Device::CreateShaderResourceView** verweist. Sie legen auch den [**Wert D3D11 \_ SRV \_ DIMENSION \_ BUFFEREX**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)) im **ViewDimension-Member** von **D3D11 \_ SHADER RESOURCE VIEW \_ \_ \_ DESC** fest, um anzugeben, dass es sich bei dem SRV um eine unformatierte Ansicht handelt.
-   Um eine ungeordnete Zugriffsansicht (UAV) für den Puffer zu erstellen, rufen Sie [**ID3D11Device::CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) mit dem [**Flag D3D11 \_ BUFFER \_ UAV FLAG RAW \_ \_ auf.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag) Sie geben dieses Flag im **Flags-Member** der [**\_ PUFFER-UAV-Struktur \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav) an. Sie legen **D3D11 \_ BUFFER \_ UAV** im **Puffer-Member** der [**D3D11 \_ UNORDERED \_ ACCESS VIEW \_ \_ DESC-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc) fest, auf die der *pDesc-Parameter* von **ID3D11Device::CreateUnorderedAccessView** verweist. Sie legen auch den [**Wert D3D11 \_ UAV DIMENSION \_ \_ BUFFER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension) im **ViewDimension-Member** von **D3D11 \_ UNORDERED \_ ACCESS VIEW \_ \_ DESC** fest, um anzugeben, dass es sich bei der UAV um eine unformatierte Ansicht handelt.

Sie können die Objekttypen HLSL [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) und [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) verwenden, wenn Sie mit unformatierten Puffern arbeiten.

Um eine unformatierte Ansicht für einen Puffer zu erstellen, müssen Sie zuerst [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mit dem [**Flag D3D11 \_ RESOURCE \_ MISC BUFFER ALLOW RAW \_ \_ \_ \_ VIEWS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) aufrufen, um die zugrunde liegende Pufferressource zu erstellen. Sie geben dieses Flag im **MiscFlags-Member** der [**D3D11 \_ BUFFER \_ DESC-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) an, auf die der *pDesc-Parameter* von **ID3D11Device::CreateBuffer** verweist. Sie können das **FLAG D3D11 \_ RESOURCE \_ MISC \_ BUFFER ALLOW \_ RAW \_ \_ VIEWS** nicht mit [**dem D3D11 \_ RESOURCE \_ MISC BUFFER STRUCTURED \_ \_ kombinieren.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Wenn Sie außerdem [**D3D11 \_ BIND CONSTANT \_ \_ BUFFER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) in **BindFlags** von **D3D11 \_ BUFFER \_ DESC** angeben, können Sie nicht auch **D3D11 \_ RESOURCE \_ MISC BUFFER ALLOW RAW \_ \_ \_ \_ VIEWS** in **MiscFlags angeben.** Dies ist keine Einschränkung nur für Unformatierungsansichten, da konstante Puffer bereits eine Einschränkung haben, dass sie nicht mit einer anderen Ansicht kombiniert werden können.

Wenn Sie einen Puffer mit [**D3D11 \_ RESOURCE \_ MISC \_ BUFFER \_ ALLOW \_ RAW \_ VIEWS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)erstellen, sind Sie nicht auf die Funktionalität beschränkt, anstatt **D3D11 RESOURCE MISC BUFFER ALLOW RAW VIEWS (D3D11 RESOURCE \_ \_ MISC \_ BUFFER ALLOW RAW \_ \_ \_ VIEWS)** nicht auf die Funktionalität zu setzen. Das heißt, Sie können einen solchen Puffer für nicht unformatierten Zugriff auf eine beliebige Weise verwenden, die mit Direct3D möglich ist. Wenn Sie das **Flag D3D11 \_ RESOURCE \_ MISC BUFFER ALLOW RAW \_ \_ \_ \_ VIEWS** angeben, erhöhen Sie nur die verfügbaren Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> <dt>

[Neue Ressourcentypen](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 