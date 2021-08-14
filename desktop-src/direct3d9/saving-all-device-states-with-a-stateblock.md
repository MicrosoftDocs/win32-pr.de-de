---
description: Ein Zustandsblock kann verwendet werden, um alle Gerätezustände zu erfassen (siehe Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Speichern aller Gerätezustände mit einem StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffda5b5d637a31c774e97af85ddeca78b0995ee53c015bb2dcd245b42277a4cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520081"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Speichern aller Gerätezustände mit einem StateBlock (Direct3D 9)

Ein Zustandsblock kann verwendet werden, um alle Gerätezustände zu erfassen (siehe Zustandsblöcke Speichern und Wiederherstellen des Zustands [(Direct3D 9)](state-blocks-save-and-restore-state.md)). Die folgenden Zustandselemente sind im Gerätestatus enthalten:

-   Scheitelpunktzustand (siehe [Speichern von Scheitelpunktzuständen mit einem StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Pixelzustand (siehe [Speichern des Pixelzustands mit einem StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Jede Textur, die einem Sampler zugewiesen ist.
-   Jede Scheitelpunkttextur.
-   Jede Verschiebungszuordnungstextur.
-   Die aktuelle Texturpalette.
-   Für jeden Scheitelpunktstream: ein Zeiger auf den Scheitelpunktpuffer, jedes Argument aus [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api)und der Unterteiler (falls eins) aus [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Ein Zeiger auf den Indexpuffer.
-   Der Viewport.
-   Das Scissors-Rechteck.
-   Die Welt-, Ansichts- und Projektionsmatrizen.
-   Die Texturtransformationen.
-   Die Clippingebenen (sofern diese noch nicht angezeigt werden).
-   Das aktuelle Material.

Um alle Gerätezustände mit einem Zustandsblock zu erfassen, geben Sie D3DSBT ALL beim Aufrufen von \_ [**IDirect3DDevice9::CreateStateBlock an.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zustandsblöcke Speichern und Wiederherstellen des Zustands](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
