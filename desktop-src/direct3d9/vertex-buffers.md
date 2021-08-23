---
description: Vertexpuffer, dargestellt durch die IDirect3DVertexBuffer9-Schnittstelle, sind Speicherpuffer, die Scheitelpunktdaten enthalten.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Scheitelpunktpuffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ceec0f5aee30597b20142945a4ffd3cbcd29500db4113ac2c8dcdd27d045d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043998"
---
# <a name="vertex-buffers-direct3d-9"></a>Scheitelpunktpuffer (Direct3D 9)

Vertexpuffer, dargestellt durch die [**IDirect3DVertexBuffer9-Schnittstelle,**](/windows/desktop/api) sind Speicherpuffer, die Scheitelpunktdaten enthalten. Scheitelpunktpuffer können jeden Vertextyp enthalten – transformiert oder nicht übersetzt, leuchtet oder unlit – der mithilfe der Renderingmethoden in der [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) gerendert werden kann. Sie können die Scheitelpunkte in einem Scheitelpunktpuffer verarbeiten, um Vorgänge wie Transformation, Beleuchtung oder das Generieren von Clippingflags durchzuführen. Die Transformation wird immer ausgeführt.

Die Flexibilität von Scheitelpunktpuffern macht sie zu idealen Stagingpunkten für die Erneutverwendung transformierten Geometrie. Sie können einen einzelnen Scheitelpunktpuffer erstellen, transformieren, lichten und die Scheitelpunkte beschneiden und das Modell so oft wie nötig in der Szene rendern, ohne es neu zu transformieren, auch wenn sich der Überlappungszustand ändert. Dies ist nützlich, wenn Modelle gerendert werden, die mehrere Texturen verwenden: Die Geometrie wird nur einmal transformiert, und dann können Teile davon nach Bedarf gerendert und mit den erforderlichen Texturänderungen übereinander gewebt werden. Renderzustandsänderungen, die nach der Verarbeitung von Scheiteltices vorgenommen werden, werden wirksam, wenn die Scheitelungen das nächste Mal verarbeitet werden.

-   [Beschreibung](#description)
-   [Arbeitsspeicherpool und -nutzung](#memory-pool-and-usage)

## <a name="description"></a>Beschreibung

Ein Scheitelpunktpuffer wird in Bezug auf seine Funktionen beschrieben: wenn er nur im Systemspeicher vorhanden sein kann, wenn er nur für Schreibvorgänge verwendet wird, sowie den Typ und die Anzahl der Scheitelpunkte, die er enthalten kann. Alle diese Merkmale werden in einer [**D3DVERTEXBUFFER \_ DESC-Struktur**](d3dvertexbuffer-desc.md) gehalten.

Der Format-Member ist auf D3DFMT VERTEXDATA festgelegt, um anzugeben, dass es sich \_ um einen Scheitelpunktpuffer handelt. Der Typ identifiziert den Ressourcentyp des Scheitelpunktpuffers. Der Usage-Struktur-Member enthält allgemeine Funktionsflags. Das D3DUSAGE SOFTWAREPROCESSING-Flag gibt an, dass der Scheitelpunktpuffer bei der \_ Softwarevertexverarbeitung verwendet werden soll. Das Vorhandensein des D3DUSAGE WRITEONLY-Flags in Usage gibt an, dass der Scheitelpunktpufferspeicher nur \_ für Schreibvorgänge verwendet wird. Dadurch kann der Treiber die Scheitelpunktdaten am besten im Arbeitsspeicher platzieren, um eine schnelle Verarbeitung und ein schnelles Rendering zu ermöglichen. Wenn das D3DUSAGE WRITEONLY-Flag nicht verwendet wird, ist es weniger wahrscheinlich, dass der Treiber die Daten an einem Speicherort abspeichert, der für Lesevorgänge \_ ineffizient ist. Dadurch wird die Verarbeitungs- und Renderinggeschwindigkeit etwas geerbt. Wenn dieses Flag nicht angegeben wird, wird davon ausgegangen, dass Anwendungen Lese- und Schreibvorgänge für die Daten innerhalb des Scheitelpunktpuffers ausführen.

Pool gibt die Speicherklasse an, die für den Scheitelpunktpuffer zugeordnet wird. Das D3DPOOL \_ SYSTEMMEM-Flag gibt an, dass das System den Scheitelpunktpuffer im Systemspeicher erstellt hat.

Der Size-Member speichert die Größe der Scheitelpunktpufferdaten in Bytes. Der FVF-Member enthält eine Kombination aus [D3DFVF,](d3dfvf.md) die den Typ der Scheitelungen identifiziert, die der Puffer enthält.

## <a name="memory-pool-and-usage"></a>Arbeitsspeicherpool und -nutzung

Sie können Scheitelpunktpuffer mit der [**IDirect3DDevice9::CreateVertexBuffer-Methode**](/windows/desktop/api) erstellen, die Pool- (Speicherklasse) und Verwendungsparameter verwendet. **IDirect3DDevice9::CreateVertexBuffer** kann auch mit einem angegebenen FVF-Code für die Verwendung in der Vertexverarbeitung fester Funktionen oder als Ausgabe von Prozessvertices erstellt werden. Weitere Informationen finden Sie unter [FVF-Scheitelpunktpuffer (Direct3D 9).](fvf-vertex-buffers.md)

Das D3DUSAGE SOFTWAREPROCESSING-Flag kann festgelegt werden, wenn die Vertexverarbeitung im gemischten Modus oder die \_ Softwarevertexverarbeitung (D3DCREATE \_ MIXED \_ VERTEXPROCESSING/D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING) für dieses Gerät aktiviert ist. D3DUSAGE SOFTWAREPROCESSING muss für Puffer festgelegt werden, die mit der Softwarevertexverarbeitung im gemischten Modus verwendet werden sollen. Sie sollte jedoch nicht für die bestmögliche Leistung festgelegt werden, wenn die Hardwarevertexverarbeitung im gemischten Modus verwendet \_ wird.( D3DERATE \_ HARDWARE \_ VERTEXPROCESSING). Das Festlegen von D3DUSAGE SOFTWAREPROCESSING ist jedoch die einzige Option, wenn ein einzelner Puffer sowohl bei der Hardware- als auch bei der \_ Softwarevertexverarbeitung verwendet werden soll. D3DUSAGE \_ SOFTWAREPROCESSING ist für gemischte sowie für Softwaregeräte zulässig.

Es ist möglich, Scheitelpunkt- und Indexpuffer in den Systemspeicher zu zwingen, indem D3DPOOL SYSTEMMEM angegeben wird, auch wenn die Scheitelpunktverarbeitung \_ auf Hardware erfolgt. Dies ist eine Möglichkeit, zu große Mengen von seitengesperrten Speicher zu vermeiden, wenn ein Treiber diese Puffer in den AGP-Arbeitsspeicher einträgt.

In diesem Abschnitt werden die Konzepte erläutert, die erforderlich sind, um Scheitelpunktpuffer in einer Direct3D-Anwendung zu verstehen und zu verwenden. Die Informationen sind in die folgenden Abschnitte unterteilt.

-   [Erstellen eines Scheitelpunktpuffers (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Zugreifen auf den Inhalt eines Scheitelpunktpuffers (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Rendern aus einem Scheitelpunktpuffer (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [FVF-Scheitelpunktpuffer (Direct3D 9)](fvf-vertex-buffers.md)
-   [Vertexverarbeitung der Funktion korrigiert (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Programmierbare Vertexverarbeitung (Direct3D 9)](programmable-vertex-processing.md)
-   [Gerätetypen und Vertexverarbeitungsanforderungen (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> <dt>

[Rendern von Scheitelpunkt- und Indexpuffern (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Indexpuffer (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
