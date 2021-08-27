---
description: Die IDirect3DDevice9-Schnittstelle unterstützt die Scheitelpunktverarbeitung in Software und Hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Verarbeiten von Scheitelpunktdaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4656aadee8f39c61be438f85ae0829f0b10dac42c7e5c9014b6ba8c164b3257b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118610"
---
# <a name="processing-vertex-data-direct3d-9"></a>Verarbeiten von Scheitelpunktdaten (Direct3D 9)

Die [**IDirect3DDevice9-Schnittstelle unterstützt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die Scheitelpunktverarbeitung in Software und Hardware. Im Allgemeinen sind die Gerätefunktionen für die Software- und Hardware-Scheitelpunktverarbeitung nicht identisch. Hardwarefunktionen sind je nach Anzeigeadapter und Treiber variabel, während die Softwarefunktionen festgelegt sind.

Die folgenden Flags steuern das Scheitelpunktverarbeitungsverhalten für die Hardwareabstraktionsschicht (Hardware Abstraction Layer, HALOGEN) und Referenzgeräte.

-   D3DERATE \_ SOFTWARE \_ VERTEXPROCESSING
-   D3DERATE \_ HARDWARE \_ VERTEXPROCESSING
-   D3DERATE \_ MIXED \_ VERTEXPROCESSING

Geben Sie beim Aufrufen von [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)eines der Scheitelpunktverarbeitungsverhaltensflags an. Das Flag für den gemischten Modus ermöglicht dem Gerät die Verarbeitung von Software- und Hardware-Scheitelpunkt. Für ein Gerät kann immer nur ein Scheitelpunktverarbeitungsflag festgelegt werden. Beachten Sie, dass beim Erstellen eines reinen Geräts \_ \_ (D3DCREATE PUREDEVICE) das Flag D3DCREATE HARDWARE VERTEXPROCESSING \_ festgelegt werden muss.

Um duale Scheitelpunktverarbeitungsfunktionen auf einem einzelnen Gerät zu vermeiden, können zur Laufzeit nur die Hardwarevertexverarbeitungsfunktionen abgefragt werden. Die Verarbeitungsfunktionen für Softwarevertex sind fest und können zur Laufzeit nicht abgefragt werden.

Das VertexProcessingCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) bestimmt die Hardwarevertexverarbeitungsfunktionen des Geräts.

Für die Verarbeitung von Softwarevertex werden die folgenden Funktionen unterstützt.

-   Das D3DVTXPCAPS \_ DIRECTIONALLIGHTS-Mitglied von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   D3DVTXPCAPS \_ LOCALVIEWER-Mitglied von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   D3DVTXPCAPS \_ MATERIALSOURCE7-Mitglied von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   das D3DVTXPCAPS \_ POSITIONALLIGHTS-Mitglied von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   D3DVTXPCAPS \_ TEXGEN-Mitglied von [D3DVTXPCAPS](d3dvtxpcaps.md)
-   das D3DVTXPCAPS \_ TWEENING-Mitglied von [D3DVTXPCAPS](d3dvtxpcaps.md)

Darüber hinaus werden in der folgenden Tabelle die Werte aufgeführt, die für Elemente der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für ein Gerät im Softwarevertexverarbeitungsmodus festgelegt werden.



| Member                 | Funktionen zur Verarbeitung von Softwarevertex |
|------------------------|-----------------------------------------|
| MaxActiveLights        | Unbegrenzt                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | 0xFFFFFFFF                              |



 

Im Allgemeinen sollte jede Anwendung, die an die Scheitelpunktverarbeitung gebunden ist, ein HALOGEN-Gerät verwenden. Die Softwarevertexverarbeitung bietet eine garantierte Reihe von Scheitelpunktverarbeitungsfunktionen, einschließlich einer ungebundenen Anzahl von Beleuchtungen und vollständiger Unterstützung für programmierbare Vertex-Shader. Sie können jederzeit zwischen software- und hardwarevertex processing (Scheitelpunktverarbeitung) umschalten, wenn Sie das HALOGEN-Gerät verwenden (dies ist der einzige Gerätetyp, der die Hardware- und Softwarevertexverarbeitung unterstützt). Die einzige Anforderung ist, dass Scheitelpunktpuffer, die für die Softwarevertexverarbeitung verwendet werden, im Systemspeicher zugeordnet werden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
