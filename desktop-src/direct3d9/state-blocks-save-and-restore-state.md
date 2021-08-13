---
description: Ein Zustandsblock ist eine Gruppe von Gerätezuständen.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a56ed6490b0d81b7e643ef892e6a760f00b841531bd21dc69a4069f07b9aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291727"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)

Ein Zustandsblock ist eine Gruppe von Gerätezuständen. Der Gerätezustand besteht aus Renderzustand, Scheitelpunktzustand, Pixelzustand oder allen oben genannten Zuständen. Ein Zustandsblock enthält eine Momentaufnahme des aktuellen Zustands eines Geräts, oder Sie können einen Zustandsblock erstellen, der jede Zustandsänderung aufzeichnet, die ihre Anwendung vornimmt.

## <a name="capture-a-block-of-state"></a>Erfassen eines Zustandsblocks

Wählen Sie den Zustandstyp aus, den Sie erfassen möchten, und erstellen Sie einen Zustandsblock wie diesen:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) erstellt einen Zustandsblock und erfasst automatisch den Gerätezustand. Der Gerätezustand wird durch den Zustandsblocktyp im ersten Argument angegeben. Dieser Zustand kann einer der folgenden Sein: der gesamte Gerätezustand (siehe [Speichern aller Gerätezustände mit einem StateBlock (Direct3D 9),](saving-all-device-states-with-a-stateblock.md)der gesamte Pixelzustand (siehe Speichern des [Pixelzustands mit einem StateBlock (Direct3D 9) )](saving-pixel-states-with-a-stateblock.md)oder der gesamte Scheitelpunktzustand (siehe Speichern von [Scheitelpunktzuständen mit einem StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).

Das Effektsystem verwendet einen Zustandsblock, um den Zustand zu speichern. Nachdem [**ID3DXEffect::Begin**](id3dxeffect--begin.md) aufgerufen wurde, wird ein Zustandsblock erstellt und der Zustand erfasst. Wenn [**ID3DXEffect::End**](id3dxeffect--end.md) aufgerufen wird, wird der Zustandsblockzustand erneut auf das Gerät angewendet.

## <a name="capture-individual-states"></a>Erfassen einzelner Zustände

Um eine benutzerdefinierte Zustandssequenz zu speichern, umschließen Sie den Zustand, den Sie speichern möchten, in einem [**IDirect3DDevice9::BeginStateBlock-**](/windows/desktop/api) und [**IDirect3DDevice9::EndStateBlock-Paar.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) BeginStateBlock weist das aktuelle Gerät an, einen Zustandsblock einzurichten und ihm jede Zustandsänderung hinzuzufügen, die auftritt, bis EndStateBlock aufgerufen wird. Hier sehen Sie ein Beispiel:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



Dadurch wird eine beliebige Anzahl von Zustandsänderungen in einer beliebigen Sequenz in einem benutzerdefinierten Zustandsblock gespeichert. Wenn Sie später den Zustandsblock zum Zurücksetzen des Gerätezustands verwenden möchten, rufen Sie [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply)auf. Dadurch wird nur der Gerätezustand überschrieben, der im Zustandsblock erfasst wurde. Jeder andere Gerätezustand, der nicht mit dem benutzerdefinierten Zustandsblock erfasst wurde, wird nicht geändert. Da das stateblock-Objekt eine Schnittstelle ist, müssen Sie es wieder freigeben, wenn Sie damit fertig sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zustände (Direct3D 9)](states.md)
</dt> </dl>

 

 
