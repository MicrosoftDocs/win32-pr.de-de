---
description: Ein Zustands Block kann zum Erfassen aller Gerätezustände verwendet werden (siehe Status Blöcke speichern und Wiederherstellen (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Speichern aller Gerätezustände mit einem stateblock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345598"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Speichern aller Gerätezustände mit einem stateblock (Direct3D 9)

Ein Zustands Block kann zum Erfassen aller Gerätezustände verwendet werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)). Die folgenden Zustands Elemente sind im Gerätestatus enthalten:

-   Scheitelpunkt Status (siehe [Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Pixel Zustand (siehe [Speichern des Pixel Zustands mit einem stateblock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Jede Textur, die einem Sampler zugewiesen ist.
-   Jede Scheitelpunkt Textur.
-   Jede Verschiebungs Karten Textur.
-   Die aktuelle Texturpalette.
-   Für jeden vertexstream: ein Zeiger auf den Vertex-Puffer, jedes Argument aus [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api)und der unter Teiler (sofern vorhanden) von [**IDirect3DDevice9:: setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Ein Zeiger auf den Index Puffer.
-   Der Viewport.
-   Das Scheren Rechteck.
-   Die Matrizen "World", "View" und "Projection".
-   Die Textur Transformationen.
-   Die Clippingebenen (sofern vorhanden).
-   Das aktuelle Material.

Um alle Gerätezustände mit einem Zustands Block zu erfassen, geben Sie D3DSBT all an, \_ Wenn Sie [**IDirect3DDevice9:: createstateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Status Blöcke speichern und Wiederherstellen](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
