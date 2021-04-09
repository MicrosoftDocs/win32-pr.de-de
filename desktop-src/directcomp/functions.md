---
title: Directcomposition-Funktionen
description: In diesem Abschnitt werden die Funktionen von Microsoft directcomposition \ 32; beschrieben. Found.
ms.assetid: 750FDFD5-ADD5-43B3-A596-ECDB82C2EF73
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e0b7e32f22faaefdf625e0af2a42a03e469d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101815"
---
# <a name="directcomposition-functions"></a><span data-ttu-id="12490-103">Directcomposition-Funktionen</span><span class="sxs-lookup"><span data-stu-id="12490-103">DirectComposition functions</span></span>

<span data-ttu-id="12490-104">In diesem Abschnitt werden die von der Microsoft directcomposition-API bereitgestellten Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="12490-104">This section describes the functions provided by the Microsoft DirectComposition API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12490-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="12490-105">In this section</span></span>



| <span data-ttu-id="12490-106">Thema</span><span class="sxs-lookup"><span data-stu-id="12490-106">Topic</span></span>                                                                                       | <span data-ttu-id="12490-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12490-107">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12490-108">**Dcompositionattachmougdragzu HWND**</span><span class="sxs-lookup"><span data-stu-id="12490-108">**DCompositionAttachMouseDragToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousedragtohwnd)<br/>   | <span data-ttu-id="12490-109">Erstellt eine Interaktion/inputsink zum Weiterleiten der Maustaste und alle nachfolgenden Verschiebungs-und aufwärts Ereignisse an den angegebenen HWND.</span><span class="sxs-lookup"><span data-stu-id="12490-109">Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.</span></span><br/>                      |
| [<span data-ttu-id="12490-110">**Dcompositionattachmougwheel-HWND**</span><span class="sxs-lookup"><span data-stu-id="12490-110">**DCompositionAttachMouseWheelToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousewheeltohwnd)<br/> | <span data-ttu-id="12490-111">Erstellt eine Interaktion/inputsink zum Weiterleiten von Mausrad Meldungen an das angegebene HWND.</span><span class="sxs-lookup"><span data-stu-id="12490-111">Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.</span></span> <br/>                                                        |
| [<span data-ttu-id="12490-112">**Dcompositionkreatedevice**</span><span class="sxs-lookup"><span data-stu-id="12490-112">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)<br/>                     | <span data-ttu-id="12490-113">Erstellt ein neues Geräte Objekt, das zum Erstellen anderer directcomposition-Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="12490-113">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="12490-114">**DCompositionCreateDevice2**</span><span class="sxs-lookup"><span data-stu-id="12490-114">**DCompositionCreateDevice2**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice2)<br/>                   | <span data-ttu-id="12490-115">Erstellt ein neues Geräte Objekt, das zum Erstellen anderer directcomposition-Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="12490-115">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="12490-116">**DCompositionCreateDevice3**</span><span class="sxs-lookup"><span data-stu-id="12490-116">**DCompositionCreateDevice3**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice3)<br/>                   | <span data-ttu-id="12490-117">Erstellt ein neues directcomposition-Geräte Objekt, das zum Erstellen anderer directcomposition-Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="12490-117">Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.</span></span><br/>                               |
| [<span data-ttu-id="12490-118">**Dcompositionkreatesurfakehandle**</span><span class="sxs-lookup"><span data-stu-id="12490-118">**DCompositionCreateSurfaceHandle**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatesurfacehandle)<br/>       | <span data-ttu-id="12490-119">Erstellt ein neues Kompositions Oberflächen Objekt, das an eine Microsoft DirectX-Swapkette oder einen Auslagerungs Puffer gebunden und mit einem visuellen Element verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="12490-119">Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.</span></span><br/> |
| <span data-ttu-id="12490-120">[**Dcompositiongetframestatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12490-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span></span><br/>         | <span data-ttu-id="12490-121">Ruft Kompositions Statistik Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="12490-121">Retrieves composition statistics information.</span></span><br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="12490-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12490-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12490-123">Directcomposition-Referenz</span><span class="sxs-lookup"><span data-stu-id="12490-123">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

