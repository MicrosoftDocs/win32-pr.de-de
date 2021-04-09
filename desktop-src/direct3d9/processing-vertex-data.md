---
description: Die IDirect3DDevice9-Schnittstelle unterstützt die Scheitelpunkt Verarbeitung in Software und Hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Verarbeiten von Scheitelpunkt Daten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860403"
---
# <a name="processing-vertex-data-direct3d-9"></a>Verarbeiten von Scheitelpunkt Daten (Direct3D 9)

Die [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle unterstützt die Scheitelpunkt Verarbeitung in Software und Hardware. Im Allgemeinen sind die Gerätefunktionen für die Verarbeitung von Software-und Hardware Scheitel Punkten nicht identisch. Die Hardware Funktionen sind abhängig vom Anzeige Adapter und Treiber variabel, während die Softwarefunktionen korrigiert werden.

Die folgenden Flags steuern das Scheitelpunkt Verarbeitungs Verhalten für die Hardware Abstraktionsschicht (HAL) und Referenzgeräte.

-   D3DCREATE \_ Software \_ vertexprocessing
-   D3DCREATE \_ Hardware \_ vertexprocessing
-   D3DCREATE \_ gemischte \_ vertexprocessing

Geben Sie beim Aufrufen von [**IDirect3D9:: createdevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)eines der vertexprozessorverhaltenflags an. Mit dem Flag für den gemischten Modus kann das Gerät sowohl die Software-als auch die Hardware Vertex-Verarbeitung durchführen. Für ein Gerät kann jeweils nur ein vertexverarbeitungsflag festgelegt werden. Beachten Sie, dass das D3DCREATE \_ Hardware \_ vertexprocessing-Flag festgelegt werden muss, wenn ein reines Gerät (D3DCREATE \_ puredevice) erstellt wird.

Um duale Scheitelpunkt Verarbeitungsfunktionen auf einem einzelnen Gerät zu vermeiden, können nur die Hardware-Scheitelpunkt Verarbeitungsfunktionen zur Laufzeit abgefragt werden. Die Verarbeitungsfunktionen der Software-Scheitel Punkte sind korrigiert und können zur Laufzeit nicht abgefragt werden.

Der VertexProcessingCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur bestimmt die Hardware-Scheitelpunkt Verarbeitungsfunktionen des Geräts.

Bei der Verarbeitung von Software Scheitel Punkten werden die folgenden Funktionen unterstützt.

-   der D3DVTXPCAPS \_ DirectionalLights-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   der D3DVTXPCAPS \_ localviewer-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   der D3DVTXPCAPS \_ MATERIALSOURCE7-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   der D3DVTXPCAPS \_ positionallights-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   der D3DVTXPCAPS \_ TEXGEN-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   der D3DVTXPCAPS \_ Tweening-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)

Außerdem werden in der folgenden Tabelle die Werte aufgelistet, die für Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für ein Gerät im Software Scheitelpunkt-Verarbeitungsmodus festgelegt sind.



| Member                 | Verarbeitungsfunktionen für Software Scheitel Punkte |
|------------------------|-----------------------------------------|
| MaxActiveLights        | Unbegrenzt                               |
| Maxuserclipplane      | 6                                       |
| Maxvertexblendmatrices | 4                                       |
| Maxstreams             | 16                                      |
| MaxVertexIndex         | 0xFFFFFFFF                              |



 

Im Allgemeinen sollte jede Anwendung, bei der die Vertexverarbeitung gebunden ist, ein HAL-Gerät verwenden. Die Verarbeitung von Software Scheitel Punkten bietet eine garantierte Reihe von vertexverarbeitungs Funktionen, einschließlich einer unbegrenzten Anzahl von Lichtern und vollständiger Unterstützung für programmierbare Vertex-Shader. Sie können jederzeit zwischen der Verarbeitung von Software-und Hardware Scheitel Punkten wechseln, wenn Sie das HAL-Gerät verwenden (Hierbei handelt es sich um den einzigen Gerätetyp, der die Verarbeitung von Hardware-und Software Scheitel Punkten unterstützt). Die einzige Voraussetzung ist, dass Vertex-Puffer, die für die Verarbeitung von Software Vertex verwendet werden, im Systemspeicher zugeordnet werden müssen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
