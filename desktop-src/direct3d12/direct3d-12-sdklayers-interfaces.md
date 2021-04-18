---
title: Shnittstellen der Debugschicht
description: Die folgenden Schnittstellen werden in d3d12sdklayers. h deklariert.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "106340482"
---
# <a name="debug-layer-interfaces"></a><span data-ttu-id="fb11b-103">Debug-ebenenschnittstellen</span><span class="sxs-lookup"><span data-stu-id="fb11b-103">Debug Layer interfaces</span></span>

<span data-ttu-id="fb11b-104">Die folgenden Schnittstellen sind in definiert `d3d12sdklayers.h` .</span><span class="sxs-lookup"><span data-stu-id="fb11b-104">The following interfaces are defined in `d3d12sdklayers.h`.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fb11b-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fb11b-105">In this section</span></span>

| <span data-ttu-id="fb11b-106">Thema</span><span class="sxs-lookup"><span data-stu-id="fb11b-106">Topic</span></span> | <span data-ttu-id="fb11b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb11b-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="fb11b-108">**ID3D12Debug**</span><span class="sxs-lookup"><span data-stu-id="fb11b-108">**ID3D12Debug**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | <span data-ttu-id="fb11b-109">Eine Debug-Schnittstelle steuert Debugeinstellungen und überprüft den Pipeline Zustand.</span><span class="sxs-lookup"><span data-stu-id="fb11b-109">A debug interface controls debug settings and validates pipeline state.</span></span> <span data-ttu-id="fb11b-110">Sie kann nur verwendet werden, wenn die debugschicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fb11b-110">It can only be used if the debug layer is turned on.</span></span> |
| [<span data-ttu-id="fb11b-111">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="fb11b-111">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | <span data-ttu-id="fb11b-112">Fügt der debugschicht die GPU-basierte Validierung und die Synchronisierung der abhängigen Befehls Warteschlange hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb11b-112">Adds GPU-based validation and Dependent Command Queue Synchronization to the debug layer.</span></span> |
| [<span data-ttu-id="fb11b-113">**ID3D12Debug2**</span><span class="sxs-lookup"><span data-stu-id="fb11b-113">**ID3D12Debug2**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | <span data-ttu-id="fb11b-114">Fügt konfigurierbare Ebenen GPU-Based Validierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb11b-114">Adds configurable levels of GPU-Based Validation.</span></span> |
| [<span data-ttu-id="fb11b-115">**ID3D12Debug3**</span><span class="sxs-lookup"><span data-stu-id="fb11b-115">**ID3D12Debug3**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | <span data-ttu-id="fb11b-116">Fügt der GPU-basierten Überprüfung der debugschicht, der abhängigen Befehls Warteschlangen-Synchronisierung und konfigurierbaren Ebenen der GPU-basierten Validierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb11b-116">Adds to the debug layer GPU-based validation, Dependent Command Queue Synchronization, and configurable levels of GPU-based validation.</span></span> |
| [<span data-ttu-id="fb11b-117">**ID3D12DebugCommandList**</span><span class="sxs-lookup"><span data-stu-id="fb11b-117">**ID3D12DebugCommandList**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | <span data-ttu-id="fb11b-118">Stellt Methoden zum Überwachen und Debuggen einer Befehlsliste bereit.</span><span class="sxs-lookup"><span data-stu-id="fb11b-118">Provides methods to monitor and debug a command list.</span></span> |
| [<span data-ttu-id="fb11b-119">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="fb11b-119">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | <span data-ttu-id="fb11b-120">Diese Schnittstelle ermöglicht die Änderung zusätzlicher debugebeneneinstellungen der Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="fb11b-120">This interface enables modification of additional command list debug layer settings.</span></span> |
| [<span data-ttu-id="fb11b-121">**ID3D12DebugCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="fb11b-121">**ID3D12DebugCommandQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | <span data-ttu-id="fb11b-122">Bietet Methoden zum Überwachen und Debuggen einer Befehls Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="fb11b-122">Provides methods to monitor and debug a command queue.</span></span> |
| [<span data-ttu-id="fb11b-123">**ID3D12DebugDevice**</span><span class="sxs-lookup"><span data-stu-id="fb11b-123">**ID3D12DebugDevice**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | <span data-ttu-id="fb11b-124">Diese Schnittstelle stellt ein Grafikgerät zum Debuggen dar.</span><span class="sxs-lookup"><span data-stu-id="fb11b-124">This interface represents a graphics device for debugging.</span></span> |
| [<span data-ttu-id="fb11b-125">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="fb11b-125">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | <span data-ttu-id="fb11b-126">Gibt Geräte weite debugebeneneinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="fb11b-126">Specifies device-wide debug layer settings.</span></span> |
| [<span data-ttu-id="fb11b-127">**ID3D12InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="fb11b-127">**ID3D12InfoQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | <span data-ttu-id="fb11b-128">Eine Informations Warteschlangen Schnittstelle speichert, ruft Debugmeldungen ab und filtert sie.</span><span class="sxs-lookup"><span data-stu-id="fb11b-128">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="fb11b-129">Die Warteschlange besteht aus einer Nachrichten Warteschlange, einem optionalen Speicher Filter Stapel und einem optionalen Abruf Filter Stapel.</span><span class="sxs-lookup"><span data-stu-id="fb11b-129">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> |
| [<span data-ttu-id="fb11b-130">**ID3D12SharingContract**</span><span class="sxs-lookup"><span data-stu-id="fb11b-130">**ID3D12SharingContract**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | <span data-ttu-id="fb11b-131">Teil eines Vertrags zwischen D3D11On12-Diagnose Ebenen und Grafik Diagnosetools.</span><span class="sxs-lookup"><span data-stu-id="fb11b-131">Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="fb11b-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb11b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb11b-133">Einrichtung der Direct3D 12-Programmierungsumgebung</span><span class="sxs-lookup"><span data-stu-id="fb11b-133">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="fb11b-134">Referenz der Debugschicht</span><span class="sxs-lookup"><span data-stu-id="fb11b-134">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="fb11b-135">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fb11b-135">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>