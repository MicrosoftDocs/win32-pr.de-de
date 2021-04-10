---
description: Ein Zustands Block ist eine Gruppe von Geräte Zuständen.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Status Blöcke speichern und Wiederherstellen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957710"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>Status Blöcke speichern und Wiederherstellen (Direct3D 9)

Ein Zustands Block ist eine Gruppe von Geräte Zuständen. Der Gerätezustand besteht aus dem renderzustand, dem Scheitelpunkt Status, dem Pixel Zustand oder allen oben genannten. Ein Zustands Block enthält eine Momentaufnahme des aktuellen Zustands eines Geräts, oder Sie können einen Zustands Block erstellen, der jede von der Anwendung vornimmt, geänderte Zustandsänderung aufzeichnet.

## <a name="capture-a-block-of-state"></a>Erfassen eines Zustands Blocks

Wählen Sie den Typ des Zustands aus, den Sie erfassen möchten, und erstellen Sie wie folgt einen Zustands Block:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9:: kreatestateblock**](/windows/desktop/api) erstellt einen Zustands Block und erfasst automatisch den Gerätezustand. Der Gerätestatus wird durch den Zustands Blocktyp im ersten Argument angegeben. Dieser Status kann einer der folgenden sein: alle Gerätezustände (Weitere Informationen finden Sie unter speichern [aller Gerätezustände mit einem stateblock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), alle Pixel Zustände (siehe [Speichern des Pixel Zustands mit einem stateblock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) oder den Status aller Scheitel Punkte (siehe [Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).

Das Effektsystem verwendet einen Zustands Block, um den Zustand zu speichern. Nach dem Aufruf von [**ID3DXEffect:: begin**](id3dxeffect--begin.md) wird ein Zustands Block erstellt, und der Zustand wird aufgezeichnet. Wenn [**ID3DXEffect:: End**](id3dxeffect--end.md) aufgerufen wird, wird der Status Block Status erneut auf das Gerät angewendet.

## <a name="capture-individual-states"></a>Erfassen einzelner Zustände

Um eine benutzerdefinierte Zustands Sequenz zu speichern, müssen Sie den Zustand, den Sie speichern möchten, in einem [**IDirect3DDevice9:: beginstateblock**](/windows/desktop/api) -und [**IDirect3DDevice9:: endstateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) -paar umschließen. Beginstateblock weist das aktuelle Gerät an, einen Zustands Block einzurichten und ihm jede Zustandsänderung hinzuzufügen, die bis zum Aufruf von endstateblock auftritt. Hier sehen Sie ein Beispiel:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



Dadurch wird eine beliebige Anzahl von Zustandsänderungen in beliebiger Reihenfolge in einem benutzerdefinierten stateblock gespeichert. Wenn Sie später mit dem stateblock den Gerätestatus zurücksetzen möchten, wenden Sie sich an [**IDirect3DStateBlock9:: apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply). Dadurch wird nur der Gerätestatus überschrieben, der im Zustands Block aufgezeichnet wurde. Jeder andere Gerätezustand, der nicht mit dem benutzerdefinierten stateblock aufgezeichnet wurde, wird nicht geändert. Da das stateblock-Objekt eine Schnittstelle ist, müssen Sie es erneut freigeben, wenn Sie damit abgeschlossen sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zustände (Direct3D 9)](states.md)
</dt> </dl>

 

 
