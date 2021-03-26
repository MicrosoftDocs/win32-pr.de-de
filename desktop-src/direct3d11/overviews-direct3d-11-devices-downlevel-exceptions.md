---
title: Ausnahmen
description: In diesem Thema werden Ausnahmen bei der Verwendung von Direct3D 11 auf downlevelhardware beschrieben.
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97920ae42347cf618b22df82abc3b6e06bd5200d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316274"
---
# <a name="exceptions"></a>Ausnahmen

Einige Features von Direct3D 11 werden nicht vollständig durch Funktionsebenen angegeben. In diesem Thema werden Ausnahmen bei der Verwendung von Direct3D 11 auf downlevelhardware beschrieben. Möglicherweise wurde eine Funktion hinzugefügt, nachdem die Featureebene definiert wurde (und einen aktualisierten Treiber erfordert), oder vielleicht unterschiedliche GPUs implementieren weit verbreitete Implementierungen. Ausnahmen auf Featureebene können in den folgenden Gruppen erfasst werden:

-   [Erweiterte Formate](#extended-formats)
-   [Multisample-Antialiasing](#multisample-anti-aliasing)
-   [Texture2D-Größen](#texture2d-sizes)
-   [Spezielles Verhalten von Adaptern für Featureebene 9](#special-behavior-of-adapters-for-feature-level-9)
-   [Zugehörige Themen](#related-topics)

Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen

## <a name="extended-formats"></a>Erweiterte Formate

Ein erweitertes Format ist ein Pixel Format, das zu Direct3D 10,1 und Direct3D 11 für featureebenen 10 \_ 0 und 10 1 hinzugefügt wird \_ . Ein erweitertes Format erfordert einen aktualisierten Treiber (für Direct3D 10 \_ 1 oder niedriger). Verwenden Sie [**ID3D11Device:: checkformatsupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) und [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) , um die Unterstützung für diese erweiterten Formate abzufragen.

Ein erweitertes Format:

-   Fügt Unterstützung für die BGRA-Reihenfolge von 8-Bit-Ressourcen pro Komponente hinzu.
-   Ermöglicht die Umwandlung eines ganzzahligen SwapChain-Puffers. Dies ermöglicht es einer Anwendung, das sRGB-Suffix hinzuzufügen oder \_ zu entfernen oder zu einer XR-Verlaufs \_ austauschkette zu Rendering.
-   Fügt optionale Unterstützung für das DXGI- \_ Format hinzu \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm.
-   Gewährleistet, dass eine \_ \_ R16G16B16A16 \_ float-Swapkette im DXGI-Format dargestellt wird, als ob die enthaltenen Daten nicht sRGB-codiert sind.

Der vollständige Satz erweiterter Formate wird entweder vollständig unterstützt oder nicht unterstützt, mit Ausnahme des XR- \_ Bias-Formats. Das Format "XR- \_ Bias" lautet:

-   Nicht unterstützt auf 9 Ebenen
-   Optional in der 10 \_ 0-oder 10 \_ 1-Ebene
-   Garantiert auf 11- \_ 0-Ebene

## <a name="multisample-anti-aliasing"></a>Multisample-Antialiasing

MSAA-Implementierungen sind bei GPU-Implementierungen kaum üblich. Funktionsebene 10,1 hat einige klar definierte Minima hinzugefügt, aber auf niedrigeren featureebenen muss MSAA explizit mithilfe von [**ID3D11Device:: checkmultisamplequalitylevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels)getestet werden.

## <a name="texture2d-sizes"></a>Texture2D-Größen

Eine Featureebene gewährleistet, dass eine minimale Größe erstellt werden kann. eine Anwendung kann jedoch bis zur vollständigen Größe, die von der GPU unterstützt wird, größere Texturen erstellen. Eine Anwendung erwartet einen Fehler von einer Methode, z. b. [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) , wenn ein Maximum überschritten wird.

## <a name="special-behavior-of-adapters-for-feature-level-9"></a>Spezielles Verhalten von Adaptern für Featureebene 9

Die drei niedrigsten featureebenen \_ D3D \_ Featureebene \_ 9 \_ 1, D3D \_ Feature \_ Level \_ 9 \_ 2 und D3D \_ Feature \_ Level \_ 9 \_ 3, geben eine gemeinsame Implementierungs-DLL frei und behandeln das [**idxgiadapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) -Argument \[ als Vorlagen Adapter für D3D11CreateDevice andswapchain \] und erstellen einen eigenen Adapter als Teil der Geräte Erstellung. Dies bedeutet, dass der an die Erstellungs Routine umgegebene **idxgiadapter** nicht derselbe Adapter ist, der über idxgidevice:: GetAdapter vom Gerät abgerufen wurde. Dies wirkt sich darauf aus, dass die **idxgioutputs** -Enumeration, die vom bestandenen Adapter aufgelistet wird, nicht verwendet werden kann, um einen voll Bildschirm mit einem beliebigen Gerät der Ebene 9 einzugeben, da diese Ausgaben nicht im Besitz des Geräte Adapters sind. Es wird empfohlen, den übergebenen Vorlagen Adapter zu verwerfen und den erstellten Adapter des Geräts mithilfe von idxgidevice:: GetAdapter abzurufen, wobei [**idxgidevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) mithilfe von QueryInterface von der Direct3D-Geräteschnittstelle abgerufen werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 auf downlevelhardware](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 