---
title: Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D
description: In diesem Abschnitt werden Interop-Techniken mit früheren Versionen von Direct3D und Direct2D, der Direct3D 11on12-API und der Portierungs Richtlinien von Direct3D 11 bis Direct3D 12 behandelt.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105070"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a><span data-ttu-id="18fe4-103">Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D</span><span class="sxs-lookup"><span data-stu-id="18fe4-103">Working with Direct3D 11, Direct3D 10 and Direct2D</span></span>

<span data-ttu-id="18fe4-104">In diesem Abschnitt werden Interop-Techniken mit früheren Versionen von Direct3D und Direct2D, der Direct3D 11on12-API und der Portierungs Richtlinien von Direct3D 11 bis Direct3D 12 behandelt.</span><span class="sxs-lookup"><span data-stu-id="18fe4-104">This section covers interop techniques with earlier versions of Direct3D and Direct2D, the Direct3D 11on12 API, and porting guidelines from Direct3D 11 to Direct3D 12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18fe4-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="18fe4-105">In this section</span></span>



| <span data-ttu-id="18fe4-106">Thema</span><span class="sxs-lookup"><span data-stu-id="18fe4-106">Topic</span></span>                                                                                             | <span data-ttu-id="18fe4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18fe4-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18fe4-108">Direct3D 12-Interop</span><span class="sxs-lookup"><span data-stu-id="18fe4-108">Direct3D 12 Interop</span></span>](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | <span data-ttu-id="18fe4-109">D3D12 kann zum Schreiben von Anwendungen verwendet werden, die in Komponenten integriert sind.</span><span class="sxs-lookup"><span data-stu-id="18fe4-109">D3D12 can be used to write componentized applications.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="18fe4-110">Direct3D 11 on 12</span><span class="sxs-lookup"><span data-stu-id="18fe4-110">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)<br/>                                             | <span data-ttu-id="18fe4-111">D3D11On12 ist ein Mechanismus, mit dem Entwickler D3D11-Schnittstellen und-Objekte verwenden können, um die D3D12-API zu steuern.</span><span class="sxs-lookup"><span data-stu-id="18fe4-111">D3D11On12 is a mechanism by which developers can use D3D11 interfaces and objects to drive the D3D12 API.</span></span> <span data-ttu-id="18fe4-112">D3D11on12 ermöglicht die Verwendung von Komponenten, die mit D3D11 (z. b. D2D Text und UI) geschrieben wurden, mit Komponenten, die für die D3D12-API geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="18fe4-112">D3D11on12 enables components written using D3D11 (for example, D2D text and UI) to work together with components written targeting the D3D12 API.</span></span> <span data-ttu-id="18fe4-113">D3D11on12 ermöglicht außerdem die inkrementelle Portierung einer Anwendung von D3D11 auf D3D12, indem Teile der App zur Vereinfachung der Ausrichtung auf D3D11 verwendet werden, während andere für die Leistung vorgesehen sind, während andere für die Leistung vorgesehen sind</span><span class="sxs-lookup"><span data-stu-id="18fe4-113">D3D11on12 also enables incremental porting of an application from D3D11 to D3D12, by enabling portions of the app to continue targeting D3D11 for simplicity while others target D3D12 for performance, while always having complete and correct rendering.</span></span> <span data-ttu-id="18fe4-114">D3D11On12 vereinfacht die Verwendung von Interop-Techniken zum Freigeben von Ressourcen und Synchronisieren von Arbeit zwischen den beiden APIs.</span><span class="sxs-lookup"><span data-stu-id="18fe4-114">D3D11On12 makes it simpler than using interop techniques to share resources and synchronize work between the two APIs.</span></span> <br/> |
| [<span data-ttu-id="18fe4-115">Portieren von Direct3D 11 zu Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="18fe4-115">Porting from Direct3D 11 to Direct3D 12</span></span>](porting-from-direct3d-11-to-direct3d-12.md)<br/> | <span data-ttu-id="18fe4-116">Dieser Abschnitt enthält eine Anleitung zum Portieren von einer benutzerdefinierten Direct3D 11-Grafik-Engine zu Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="18fe4-116">This section provides some guidance on porting from a custom Direct3D 11 graphics engine to Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="18fe4-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="18fe4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18fe4-118">Direct3D 12-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="18fe4-118">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





