---
description: Vertex-Puffer, die von der IDirect3DVertexBuffer9-Schnittstelle dargestellt werden, sind Speicherpuffer, die Scheitelpunkt Daten enthalten.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Vertex-Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e38feb34e7b9f637f383bf451bff812d9ee6fb1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746112"
---
# <a name="vertex-buffers-direct3d-9"></a>Vertex-Puffer (Direct3D 9)

Vertex-Puffer, die von der [**IDirect3DVertexBuffer9**](/windows/desktop/api) -Schnittstelle dargestellt werden, sind Speicherpuffer, die Scheitelpunkt Daten enthalten. Vertex-Puffer können einen beliebigen Scheitelpunkt (transformiert oder untransformiert) enthalten, der durch die Verwendung der Renderingmethoden in der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle gerendert werden kann. Sie können die Scheitel Punkte in einem Scheitelpunkt Puffer verarbeiten, um Vorgänge wie z. b. Transformation, Beleuchtung oder das Erstellen von clippingflags auszuführen. Die Transformation wird immer durchgeführt.

Die Flexibilität der Scheitelpunkt Puffer macht Sie ideal für stagingpunkte, um transformierte Geometrie wieder zu verwenden. Sie können einen einzelnen Vertex-Puffer erstellen, transformieren, Licht und die Scheitel Punkte darin Ausschneiden und das Modell in der Szene so oft wie nötig rendern, ohne es neu zu transformieren, auch wenn sich der Status der gerenderte renderzustände ändert. Dies ist nützlich, wenn Modelle gerendert werden, die mehrere Texturen verwenden: die Geometrie wird nur einmal transformiert, und Teile davon können bei Bedarf gerendert werden, die mit den erforderlichen Texturänderungen interleavt ist. Nach der Verarbeitung von Scheitel Punkten vorgenommene Änderungen des Rendering-Zustands werden bei der nächsten Verarbeitung der Scheitel Punkte wirksam.

-   [Beschreibung](#description)
-   [Speicher Pool und Verwendung](#memory-pool-and-usage)

## <a name="description"></a>BESCHREIBUNG

Ein Vertex-Puffer wird in Bezug auf seine Funktionen beschrieben: er kann nur im Systemspeicher vorhanden sein, wenn er nur für Schreibvorgänge verwendet wird, und der Typ und die Anzahl der Scheitel Punkte, die er enthalten kann. Alle diese Merkmale werden in einer [**D3DVERTEXBUFFER- \_**](d3dvertexbuffer-desc.md) Debug-Struktur gespeichert.

Der formatmember ist auf D3DFMT \_ vertexdata festgelegt, um anzugeben, dass es sich hierbei um einen Scheitelpunkt Puffer handelt. Der Typ identifiziert den Ressourcentyp des Scheitelpunkt Puffers. Der Member der Verwendungs Struktur enthält allgemeine funktionsflags. Das D3DUSAGE \_ softwareprocessing-Flag gibt an, dass der Scheitelpunkt Puffer bei der Verarbeitung von Software Scheitel Punkten verwendet werden soll. Das vorhanden sein des Kennzeichens D3DUSAGE \_ Schreibweise in der Verwendung gibt an, dass der Vertex-Pufferspeicher nur für Schreibvorgänge verwendet wird. Dadurch wird der Treiber freigegeben, um die Vertex-Daten am besten Speicherort zu platzieren, um eine schnelle Verarbeitung und Rendering zu ermöglichen. Wenn das \_ Flag D3DUSAGE Write only nicht verwendet wird, ist es weniger wahrscheinlich, dass der Treiber die Daten an einem Speicherort speichert, der für Lesevorgänge ineffizient ist. Dadurch wird die Verarbeitungs-und renderinggeschwindigkeit verringert. Wenn dieses Flag nicht angegeben wird, wird davon ausgegangen, dass Anwendungen Lese-und Schreibvorgänge für die Daten innerhalb des Scheitelpunkt Puffers ausführen.

Pool gibt die Speicher Klasse an, die dem Vertex-Puffer zugeordnet ist. Das D3DPOOL \_ SystemMem-Flag gibt an, dass das System den Vertex-Puffer im Systemspeicher erstellt hat.

Der Size-Member speichert die Größe der Vertex-Puffer Daten in Bytes. Der FVF-Member enthält eine Kombination aus [D3DFVF](d3dfvf.md) , die den Typ der im Puffer enthaltenen Scheitel Punkte identifiziert.

## <a name="memory-pool-and-usage"></a>Speicher Pool und Verwendung

Sie können Scheitelpunkt Puffer mit der [**IDirect3DDevice9:: kreatevertexbuffer**](/windows/desktop/api) -Methode erstellen, die Pool-(Speicher Klasse) und Verwendungs Parameter annimmt. **IDirect3DDevice9:: kreatevertexbuffer** kann auch mit einem angegebenen Code für die Verarbeitung fester Funktionen oder als Ausgabe von Prozess Scheitel Punkten erstellt werden. Weitere Informationen finden Sie unter [SVF-Vertex-Puffer (Direct3D 9)](fvf-vertex-buffers.md).

Das D3DUSAGE \_ softwareprocessing-Flag kann festgelegt werden, wenn der gemischte Modus oder die Verarbeitung von Software Scheitel Punkten (D3DCREATE \_ mixed \_ vertexprocessing/D3DCREATE \_ Software \_ vertexprocessing) für dieses Gerät aktiviert ist. D3DUSAGE \_ softwareprocessing muss für Puffer festgelegt werden, die bei der Verarbeitung von Software Scheitel Punkten im gemischten Modus verwendet werden. für die bestmögliche Leistung sollte jedoch nicht festgelegt werden, wenn die Verarbeitung von Hardware Scheitel Punkten im gemischten Modus verwendet wird. ( D3DCREATE \_ Hardware \_ vertexprocessing). Das Festlegen von D3DUSAGE \_ softwareprocessing ist jedoch die einzige Option, wenn ein einzelner Puffer sowohl mit der Hardware-als auch der Software Scheitelpunkt Verarbeitung verwendet werden soll. D3DUSAGE \_ softwareprocessing ist sowohl für gemischte als auch für Software Geräte zulässig.

Es ist möglich, Vertex-und Index Puffer in den Systemspeicher zu erzwingen, indem Sie D3DPOOL \_ SystemMem angeben, auch wenn die Vertex-Verarbeitung in der Hardware erfolgt. Dies ist eine Möglichkeit, eine übermäßig große Menge an Seiten gesperrtem Arbeitsspeicher zu vermeiden, wenn ein Treiber diese Puffer in den AGP-Speicher versetzt.

In diesem Abschnitt werden die Konzepte erläutert, die zum verstehen und Verwenden von Scheitelpunkt Puffern in einer Direct3D Die Informationen sind in die folgenden Abschnitte unterteilt.

-   [Erstellen eines Scheitelpunkt Puffers (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Zugreifen auf den Inhalt eines Scheitelpunkt Puffers (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Rendering von einem Scheitelpunkt Puffer (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [Vertex-Puffer von "f" (Direct3D 9)](fvf-vertex-buffers.md)
-   [Vertex-Verarbeitung fester Funktionen (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Programmierbare Vertex-Verarbeitung (Direct3D 9)](programmable-vertex-processing.md)
-   [Gerätetypen und Vertex-Verarbeitungsanforderungen (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> <dt>

[Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Index Puffer (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
