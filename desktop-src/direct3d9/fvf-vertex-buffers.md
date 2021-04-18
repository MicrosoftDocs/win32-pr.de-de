---
description: 'Das Festlegen des FVF-Parameters der IDirect3DDevice9:: up-Methode auf einen Wert ungleich 0 (null) gibt an, dass der Pufferinhalt durch einen FVF-Code gekennzeichnet werden soll.'
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: Vertex-Puffer von "f" (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86201c3ddc1cab6d492539caccc61c1430b3a2c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341094"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a>Vertex-Puffer von "f" (Direct3D 9)

Das Festlegen des FVF-Parameters der [**IDirect3DDevice9::**](/windows/desktop/api) up-Methode auf einen Wert ungleich 0 (null) gibt an, dass der Pufferinhalt durch einen FVF-Code gekennzeichnet werden soll. Ein Vertex-Puffer, der mit einem FVF-Code erstellt wird, wird als FVF-Vertex-Puffer bezeichnet. Einige Methoden oder Verwendungsmöglichkeiten von [**IDirect3DDevice9**](/windows/desktop/api) erfordern die Verwendung von b-Vertex-Puffern, andere erfordern nicht-b-b-Vertex-Puffer. Als Ziel-Vertex-Puffer Argument für [**IDirect3DDevice9::P rozess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)sind BTEX-Puffer Puffer erforderlich.

FVF-Vertex-Puffer können an einen Quelldaten Strom für beliebige Datenstrom Nummern gebunden werden.

Das vorhanden sein der D3DFVF \_ xyzrhw-Komponente auf FVF-Vertexpuffern gibt an, dass die Scheitel Punkte in diesem Puffer verarbeitet wurden. Für [**IDirect3DDevice9::P rozess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) verwendete Scheitelpunkt Puffer müssen nach der Verarbeitung verarbeitet werden. Vertex-Puffer, die für die Shader-Eingaben fester Funktionen verwendet werden, können entweder vorverarbeitet oder postverarbeitet werden. Wenn der Vertex-Puffer nachträglich verarbeitet wird, wird der Shader effektiv umgangen, und die Daten werden direkt an das primitive Clipping-und Setup-Modul übergeben.

Die Vertex-Puffer von "f" können mit Vertexshadern verwendet werden. Außerdem können Scheitelpunkt Datenströme die gleichen Scheitelpunkt Formate darstellen, die nicht-Sdn-Vertex-Puffer haben können. Sie müssen nicht zum Eingeben von Daten aus separaten Scheitelpunkt Puffern verwendet werden. Die zusätzliche Flexibilität der neuen Scheitelpunkt Datenströme ermöglicht Anwendungen, die Ihre Daten getrennt halten müssen, damit Sie besser funktionieren, aber dies ist nicht zwingend erforderlich. Wenn die Anwendung verschachtelte Daten im Voraus beibehalten kann, ist dies eine Leistungssteigerung. Wenn die Anwendung nur die Daten vor jedem Renderingbefehl interverlässt, sollte Sie die API oder Hardware für mehrere Streams aktivieren.

Die wichtigste Aufgabe bei der Scheitelpunkt Leistung besteht darin, einen 32-Byte-Scheitelpunkt zu verwenden und eine gute Cache Reihenfolge zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Puffer](vertex-buffers.md)
</dt> </dl>

 

 
