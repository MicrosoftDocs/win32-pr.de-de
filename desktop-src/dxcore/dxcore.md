---
title: DXCore
description: DXCore ist eine adapterenumerationsapi für DirectX-Geräte.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: 80e93ac7440629a809cb01b4d1d4fa2e73b7ee91
ms.sourcegitcommit: aa021b23d7e8bba2e1df9de93a1c315a17681810
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "106340949"
---
# <a name="dxcore"></a><span data-ttu-id="860ea-103">DXCore</span><span class="sxs-lookup"><span data-stu-id="860ea-103">DXCore</span></span>

<span data-ttu-id="860ea-104">DXCore ist eine adapterenumerationsapi für Grafiken und Compute-Geräte, sodass sich einige ihrer Funktionen mit denen von [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)überlappen.</span><span class="sxs-lookup"><span data-stu-id="860ea-104">DXCore is an adapter enumeration API for graphics and compute devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span> <span data-ttu-id="860ea-105">DXCore wird von Direct3D 12 verwendet.</span><span class="sxs-lookup"><span data-stu-id="860ea-105">DXCore is used by Direct3D 12.</span></span>

<span data-ttu-id="860ea-106">Dieser Dokumentations Satz enthält Informationen über die Programmierung mit DXCore sowie die DXCore-Referenz.</span><span class="sxs-lookup"><span data-stu-id="860ea-106">This documentation set contains information about programming with DXCore, as well as the DXCore reference.</span></span>

## <a name="requirements"></a><span data-ttu-id="860ea-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="860ea-107">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="860ea-108">**Unterstützte Laufzeitumgebungen**</span><span class="sxs-lookup"><span data-stu-id="860ea-108">**Supported runtime environments**</span></span> | <span data-ttu-id="860ea-109">Windows/C++</span><span class="sxs-lookup"><span data-stu-id="860ea-109">Windows/C++</span></span> |
| <span data-ttu-id="860ea-110">**Empfohlene Programmiersprachen**</span><span class="sxs-lookup"><span data-stu-id="860ea-110">**Recommended programming languages**</span></span> | <span data-ttu-id="860ea-111">C++</span><span class="sxs-lookup"><span data-stu-id="860ea-111">C++</span></span> |
| <span data-ttu-id="860ea-112">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="860ea-112">**Minimum supported client**</span></span> | <span data-ttu-id="860ea-113">Windows 10, Version 2004 (10,0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="860ea-113">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="860ea-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="860ea-114">**Header**</span></span> | <span data-ttu-id="860ea-115">DXCore. h und dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="860ea-115">dxcore.h and dxcore_interface.h</span></span> |
| <span data-ttu-id="860ea-116">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="860ea-116">**Library**</span></span> | <span data-ttu-id="860ea-117">DXCore. lib</span><span class="sxs-lookup"><span data-stu-id="860ea-117">dxcore.lib</span></span> |
| <span data-ttu-id="860ea-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="860ea-118">**DLL**</span></span> | <span data-ttu-id="860ea-119">dxcore.dll</span><span class="sxs-lookup"><span data-stu-id="860ea-119">dxcore.dll</span></span> |

## <a name="in-this-section"></a><span data-ttu-id="860ea-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="860ea-120">In this section</span></span>

| <span data-ttu-id="860ea-121">Thema</span><span class="sxs-lookup"><span data-stu-id="860ea-121">Topic</span></span> | <span data-ttu-id="860ea-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="860ea-122">Description</span></span> |
|-|-|
| [<span data-ttu-id="860ea-123">DXCore-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="860ea-123">DXCore programming guide</span></span>](dxcore-programming-guide.md) | <span data-ttu-id="860ea-124">Leitfaden für die Programmierung mit DXCore.</span><span class="sxs-lookup"><span data-stu-id="860ea-124">Guidance for programming with DXCore.</span></span> |
| [<span data-ttu-id="860ea-125">DXCore-Referenz</span><span class="sxs-lookup"><span data-stu-id="860ea-125">DXCore reference</span></span>](dxcore-reference.md) | <span data-ttu-id="860ea-126">In diesem Abschnitt werden die in DXCore. h und dxcore_interface. h deklarierten DXCore-APIs behandelt.</span><span class="sxs-lookup"><span data-stu-id="860ea-126">This section covers DXCore APIs declared in dxcore.h and dxcore_interface.h.</span></span> |
