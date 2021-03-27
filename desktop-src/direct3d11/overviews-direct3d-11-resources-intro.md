---
title: Einführung in eine Ressource in Direct3D 11
description: In diesem Thema werden Direct3D-Ressourcen wie Puffer und Texturen vorgestellt.
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb466883991795a66eec0ba1b99f5c989fa33c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390646"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Einführung in eine Ressource in Direct3D 11

Ressourcen sind die Bausteine Ihrer Szene. Sie enthalten den größten Teil der Daten, die Direct3D zum Interpretieren und Rendering Ihrer Szene verwendet. Ressourcen sind Bereiche im Speicher, auf die die Direct3D-Pipeline zugreifen kann. Die Ressourcen enthalten die folgenden Datentypen: Geometrie, Texturen und Shader-Daten. In diesem Thema werden Direct3D-Ressourcen wie Puffer und Texturen vorgestellt.

Sie können Ressourcen erstellen, die stark typisiert oder typlos sind; Sie können steuern, ob Ressourcen sowohl Lese-als auch Schreibzugriff haben. Sie können Ressourcen nur für die CPU, die GPU oder beides verfügbar machen. Für jede Pipelinephase können bis zu 128 Ressourcen aktiv sein.

Direct3D garantiert, dass NULL für alle Ressourcen zurückgegeben wird, auf die außerhalb der Grenzen zugegriffen wird.

Der Lebenszyklus einer Direct3D-Ressource lautet:

-   Erstellen Sie eine Ressource mit einer der Create-Methoden der [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle.
-   Binden Sie eine Ressource mithilfe eines Kontexts und einer der Set-Methoden der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle an die Pipeline.
-   Hebt die Freigabe der Ressource auf, indem die [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) -Methode der Ressourcen Schnittstelle aufgerufen wird.

Dieser Abschnitt enthält die folgenden Themen:

-   [Starke vs-schwache Typisierung](#strong-vs-weak-typing)
-   [Ressourcen Sichten](#resource-views)
-   [Unformatierte Ansichten von Puffern](#raw-views-of-buffers)
-   [Zugehörige Themen](#related-topics)

## <a name="strong-vs-weak-typing"></a>Starke vs-schwache Typisierung

Es gibt zwei Möglichkeiten, das Layout (oder den Speicherbedarf) einer Ressource vollständig anzugeben:

-   Typisiert: Geben Sie den Typ beim Erstellen der Ressource vollständig an.
-   Typlos: Geben Sie den Typ vollständig an, wenn die Ressource an die Pipeline gebunden ist.

Durch das Erstellen einer vollständig typisierten Ressource wird die Ressource auf das Format beschränkt, mit dem Sie erstellt wurde. Dadurch kann die Laufzeit den Zugriff optimieren, insbesondere dann, wenn die Ressource mit Flags erstellt wird, die angeben, dass Sie nicht von der Anwendung zugeordnet werden kann. Ressourcen, die mit einem bestimmten Typ erstellt wurden, können nicht mit dem Ansichts Mechanismus neu interpretiert werden, es sei denn, die Ressource wurde mit dem \_ Flag d3d10 DDI \_ Bind \_ vorhanden erstellt. Wenn d3d10 \_ DDI \_ Bind \_ vorhanden ist, können Renderziel-oder Shader-Ressourcen Sichten für diese Ressourcen mithilfe eines der vollständig typisierten Member der entsprechenden Familie erstellt werden, auch wenn die ursprüngliche Ressource als vollständig typisiert erstellt wurde.

In einer Ressource vom Typ less ist der Datentyp beim ersten Erstellen der Ressource unbekannt. Die Anwendung muss aus den verfügbaren Typen weniger Formate auswählen (siehe [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Sie müssen die Größe des zuzuordnenden Speichers angeben und angeben, ob die Laufzeit die Unterstrukturen in einer MipMap generieren muss. Allerdings wird das genaue Datenformat (unabhängig davon, ob der Arbeitsspeicher als ganze Zahlen, Gleit Komma Werte, ganze Zahlen ohne Vorzeichen usw. interpretiert wird) erst bestimmt, wenn die Ressource mit einer [Ressourcen Ansicht](#resource-views)an die Pipeline gebunden ist. Da das Textur Format flexibel bleibt, bis die Textur an die Pipeline gebunden ist, wird die Ressource als schwach typisierter Speicher bezeichnet. Schwach typisierter Speicher hat den Vorteil, dass er in einem anderen Format wieder verwendet oder erneut interpretiert werden kann, solange die Anzahl der Komponenten und die Bitzahl der einzelnen Komponenten in beiden Formaten identisch sind.

Eine einzelne Ressource kann an mehrere Pipeline Stufen gebunden werden, solange Sie jeweils über eine eindeutige Ansicht verfügen, die die Formate der einzelnen Speicherorte vollständig qualifiziert. Beispielsweise könnte eine Ressource, die mit dem Format DXGI \_ Format \_ R32G32B32A32 typless erstellt wurde, \_ als DXGI \_ \_ -Format R32G32B32A32 \_ float und ein DXGI- \_ Format \_ R32G32B32A32 \_ uint an verschiedenen Positionen in der Pipeline gleichzeitig verwendet werden.

## <a name="resource-views"></a>Ressourcen Sichten

Ressourcen können in allgemeinen Speicher Formaten gespeichert werden, sodass Sie von mehreren Pipeline Stufen gemeinsam genutzt werden können. Eine Pipeline Phase interpretiert Ressourcen Daten mithilfe einer Ansicht. Eine Ressourcen Ansicht ähnelt konzeptionell der Umwandlung der Ressourcen Daten, sodass Sie in einem bestimmten Kontext verwendet werden kann.

Eine Sicht kann mit einer typlosen Ressource verwendet werden. Das heißt, Sie können zum Zeitpunkt der Kompilierung eine Ressource erstellen und den Datentyp deklarieren, wenn die Ressource an die Pipeline gebunden ist. Eine für eine typlose Ressource erstellte Ansicht hat immer die gleiche Anzahl von Bits pro Komponente. die Art und Weise, wie die Daten interpretiert werden, hängt vom angegebenen Format ab. Das angegebene Format muss von derselben Familie wie das typlose Format sein, das beim Erstellen der Ressource verwendet wird. Beispielsweise kann eine Ressource, die mit dem Format "R8G8B8A8 typless" erstellt wurde, \_ nicht als "R32 float"-Ressource angezeigt werden, \_ obwohl beide Formate die gleiche Größe im Arbeitsspeicher aufweisen können.

Eine Ansicht macht auch andere Funktionen verfügbar, wie z. b. die Möglichkeit, Tiefe-/Schablone-Oberflächen in einem Shader zu lesen, eine dynamische cubemap in einem einzelnen Durchlauf zu erzeugen und gleichzeitig mehrere Slices eines Volumes zu rendern.



| Ressourcen Schnittstelle                                             | BESCHREIBUNG                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | Greifen Sie während der tiefen Schablone auf eine Textur Ressource zu.                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | Greifen Sie auf eine Textur Ressource zu, die als Renderziel verwendet wird.                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | Greifen Sie auf eine Shader-Ressource zu, z. b. einen konstanten Puffer, einen Textur Puffer, eine Textur oder einen Sampler. |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | Greifen Sie mit einem Pixelshader oder einem Compute-Shader auf eine ungeordnete Ressource zu.                        |



 

## <a name="raw-views-of-buffers"></a>Unformatierte Ansichten von Puffern

Sie können sich einen Rohdaten Puffer vorstellen, der auch als [byteadresspuffer](direct3d-11-advanced-stages-cs-resources.md)bezeichnet werden kann, als Behälter von Bits, für die Sie rohzugriff benötigen, d. h. einen Puffer, auf den Sie bequem über Segmente von einem bis zu 4 32-Bit-typlosen Adress Werten zugreifen können. Wenn Sie eine der folgenden Methoden aufrufen, um eine Ansicht für den Puffer zu erstellen, geben Sie an, dass Sie den rohzugriff auf einen Puffer (oder eine unformatierte Ansicht eines Puffers) wünschen:

-   Um eine Shader-Ressourcen Ansicht (SRV) für den Puffer zu erstellen, rufen Sie [**ID3D11Device:: kreateshaderresourceview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) mit dem Flag [**D3D11 \_ bufferex \_ SRV \_ Flag \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)auf. Sie geben dieses Flag im **Flags** -Member der [**D3D11 \_ bufferex \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv) -Struktur an. Sie legen **D3D11 \_ bufferex \_ SRV** im **bufferex** -Member der [**D3D11 \_ Shader- \_ Ressourcenansichts \_ \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) -Struktur fest, auf die der *PDE SC* -Parameter von **ID3D11Device:: kreateshaderresourceview** zeigt. Außerdem legen Sie den Wert der [**D3D11 \_ SRV- \_ Dimension \_ bufferex**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)) im **viewdimension** -Member der **D3D11 \_ Shader \_ Resource \_ View \_ ensc** fest, um anzugeben, dass der SRV eine unformatierte Ansicht ist.
-   Rufen Sie zum Erstellen einer unsorschen Zugriffs Ansicht (UAV) für den Puffer [**ID3D11Device:: dashateunorderedaccessview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) mit dem Flag [**D3D11 \_ buffer \_ UAV \_ Flag \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)auf. Sie geben dieses Flag im **Flags** -Member der [**\_ \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav) -Struktur des D3D11-Puffers an. Sie legen **" \_ D3D11 \_ buffer UAV** " im **Puffer** Element der [**nicht geordneten Struktur "D3D11 \_ unsortierter \_ Zugriffsansicht \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc) " fest, auf die der *PDE SC* -Parameter von **ID3D11Device:: kreateunorderedaccessview** zeigt. Außerdem legen Sie den Wert des [**D3D11 \_ UAV- \_ Dimensions \_ Puffers**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension) im Ansichts **Dimensions** Element von **D3D11 \_ unsortierter \_ Zugriffsansicht \_ \_ Deaktivieren** fest, um anzugeben, dass die UAV eine unformatierte Ansicht ist.

Sie können den HLSL- [**byteaddressbuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) -und den [**rwbyteaddressbuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) -Objekttyp verwenden, wenn Sie mit Rohdaten Puffer arbeiten.

Um eine unformatierte Ansicht für einen Puffer zu erstellen, müssen Sie zuerst [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mit [**dem \_ D3D11 Resource \_ misc \_ buffer \_ Allow \_ RAW \_ views**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) -Flag aufrufen, um die zugrunde liegende Puffer Ressource zu erstellen. Sie geben dieses Flag im **Fehlerflags** -Member der [**D3D11- \_ Puffer \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) -Debug-Struktur an, auf die der *PDE SC* -Parameter von **ID3D11Device::** up-Buffer zeigt. Sie können das Flag " **D3D11 \_ Resource \_ misc \_ buffer \_ Allow \_ RAW \_ views** " nicht mit einem [**\_ strukturierten D3D11 Resource \_ misc- \_ Puffer \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)kombinieren. Wenn Sie [**D3D11 \_ Bind \_ Constant \_ buffer**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) in **bindflags** von **D3D11 \_ buffer \_** Debug angeben, können Sie auch **D3D11 \_ Resource \_ misc \_ buffer \_ Allow \_ RAW \_ views** in falsch **Flags** nicht angeben. Dies ist keine Einschränkung für nur unformatierte Sichten, weil Konstante Puffer bereits über eine Einschränkung verfügen, die nicht mit einer anderen Ansicht kombiniert werden kann.

Abgesehen von den oben genannten ungültigen Fällen, wenn Sie einen Puffer mit dem [**D3D11- \_ ressourcenmisc-Puffer "unformatierte \_ \_ \_ \_ \_ Sichten zulassen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)" erstellen, sind Sie nicht auf die Funktionalität beschränkt, und es wird nicht festgelegt, **\_ \_ \_ \_ dass \_ \_ "D3D11 Resource** Das heißt, Sie können einen solchen Puffer für nicht reinen Zugriff auf eine beliebige Anzahl von Methoden verwenden, die mit Direct3D möglich sind. Wenn Sie das Flag " **D3D11 \_ Resource \_ misc \_ buffer \_ Allow \_ RAW \_ views** " angeben, erhöhen Sie nur die verfügbaren Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> <dt>

[Neue Ressourcentypen](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 