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
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a><span data-ttu-id="d1084-103">Status Blöcke speichern und Wiederherstellen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1084-103">State Blocks Save and Restore State (Direct3D 9)</span></span>

<span data-ttu-id="d1084-104">Ein Zustands Block ist eine Gruppe von Geräte Zuständen.</span><span class="sxs-lookup"><span data-stu-id="d1084-104">A state block is a group of device states.</span></span> <span data-ttu-id="d1084-105">Der Gerätezustand besteht aus dem renderzustand, dem Scheitelpunkt Status, dem Pixel Zustand oder allen oben genannten.</span><span class="sxs-lookup"><span data-stu-id="d1084-105">Device state is made up of render state, vertex state, pixel state, or all of the above.</span></span> <span data-ttu-id="d1084-106">Ein Zustands Block enthält eine Momentaufnahme des aktuellen Zustands eines Geräts, oder Sie können einen Zustands Block erstellen, der jede von der Anwendung vornimmt, geänderte Zustandsänderung aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d1084-106">A state block contains a snapshot of a device's current state, or you can create a state block that records each state change that your application makes.</span></span>

## <a name="capture-a-block-of-state"></a><span data-ttu-id="d1084-107">Erfassen eines Zustands Blocks</span><span class="sxs-lookup"><span data-stu-id="d1084-107">Capture a Block of State</span></span>

<span data-ttu-id="d1084-108">Wählen Sie den Typ des Zustands aus, den Sie erfassen möchten, und erstellen Sie wie folgt einen Zustands Block:</span><span class="sxs-lookup"><span data-stu-id="d1084-108">Choose the type of state that you want to capture, and create a state block like this:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



<span data-ttu-id="d1084-109">[**IDirect3DDevice9:: kreatestateblock**](/windows/desktop/api) erstellt einen Zustands Block und erfasst automatisch den Gerätezustand.</span><span class="sxs-lookup"><span data-stu-id="d1084-109">[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) creates a state block, and automatically captures the device state.</span></span> <span data-ttu-id="d1084-110">Der Gerätestatus wird durch den Zustands Blocktyp im ersten Argument angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1084-110">The device state is specified by the state block type in the first argument.</span></span> <span data-ttu-id="d1084-111">Dieser Status kann einer der folgenden sein: alle Gerätezustände (Weitere Informationen finden Sie unter speichern [aller Gerätezustände mit einem stateblock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), alle Pixel Zustände (siehe [Speichern des Pixel Zustands mit einem stateblock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) oder den Status aller Scheitel Punkte (siehe [Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="d1084-111">This state can be one of the following: all device state (see [Saving All Device States with a StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), all pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)), or all vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>

<span data-ttu-id="d1084-112">Das Effektsystem verwendet einen Zustands Block, um den Zustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d1084-112">The effect system uses a state block to save state.</span></span> <span data-ttu-id="d1084-113">Nach dem Aufruf von [**ID3DXEffect:: begin**](id3dxeffect--begin.md) wird ein Zustands Block erstellt, und der Zustand wird aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d1084-113">After [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called, a state block is created and state is captured.</span></span> <span data-ttu-id="d1084-114">Wenn [**ID3DXEffect:: End**](id3dxeffect--end.md) aufgerufen wird, wird der Status Block Status erneut auf das Gerät angewendet.</span><span class="sxs-lookup"><span data-stu-id="d1084-114">When [**ID3DXEffect::End**](id3dxeffect--end.md) is called, the state block state is reapplied to the device.</span></span>

## <a name="capture-individual-states"></a><span data-ttu-id="d1084-115">Erfassen einzelner Zustände</span><span class="sxs-lookup"><span data-stu-id="d1084-115">Capture Individual States</span></span>

<span data-ttu-id="d1084-116">Um eine benutzerdefinierte Zustands Sequenz zu speichern, müssen Sie den Zustand, den Sie speichern möchten, in einem [**IDirect3DDevice9:: beginstateblock**](/windows/desktop/api) -und [**IDirect3DDevice9:: endstateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) -paar umschließen.</span><span class="sxs-lookup"><span data-stu-id="d1084-116">To save a custom state sequence, wrap the state that you want to save in a [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) and [**IDirect3DDevice9::EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) pair.</span></span> <span data-ttu-id="d1084-117">Beginstateblock weist das aktuelle Gerät an, einen Zustands Block einzurichten und ihm jede Zustandsänderung hinzuzufügen, die bis zum Aufruf von endstateblock auftritt.</span><span class="sxs-lookup"><span data-stu-id="d1084-117">BeginStateBlock tells the current device to set up a state block and add to it every state change that occurs until EndStateBlock is called.</span></span> <span data-ttu-id="d1084-118">Hier sehen Sie ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d1084-118">Here's an example:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



<span data-ttu-id="d1084-119">Dadurch wird eine beliebige Anzahl von Zustandsänderungen in beliebiger Reihenfolge in einem benutzerdefinierten stateblock gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1084-119">This will save any number of state changes in any sequence to a custom stateblock.</span></span> <span data-ttu-id="d1084-120">Wenn Sie später mit dem stateblock den Gerätestatus zurücksetzen möchten, wenden Sie sich an [**IDirect3DStateBlock9:: apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span><span class="sxs-lookup"><span data-stu-id="d1084-120">Later, when you want to use the stateblock to reset the device state, call [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span></span> <span data-ttu-id="d1084-121">Dadurch wird nur der Gerätestatus überschrieben, der im Zustands Block aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1084-121">This will overwrite only the device state that has been captured in the state block.</span></span> <span data-ttu-id="d1084-122">Jeder andere Gerätezustand, der nicht mit dem benutzerdefinierten stateblock aufgezeichnet wurde, wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d1084-122">Any other device state that was not captured with the custom stateblock will not be changed.</span></span> <span data-ttu-id="d1084-123">Da das stateblock-Objekt eine Schnittstelle ist, müssen Sie es erneut freigeben, wenn Sie damit abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="d1084-123">Once again, since the stateblock object is an interface, you will need to release it when you are done with it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1084-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1084-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1084-125">Zustände (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1084-125">States (Direct3D 9)</span></span>](states.md)
</dt> </dl>

 

 
