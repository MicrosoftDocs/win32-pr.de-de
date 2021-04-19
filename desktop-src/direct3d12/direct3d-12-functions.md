---
title: Kernfunktionen (Direct3D 12-Grafiken)
description: Die folgenden Funktionen werden in d3d12. h deklariert.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "106341903"
---
# <a name="core-functions"></a><span data-ttu-id="ecdd5-103">Core-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ecdd5-103">Core functions</span></span>

<span data-ttu-id="ecdd5-104">Die folgenden Funktionen werden in d3d12. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="ecdd5-104">The following functions are declared in d3d12.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ecdd5-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ecdd5-105">In this section</span></span>

| <span data-ttu-id="ecdd5-106">Thema</span><span class="sxs-lookup"><span data-stu-id="ecdd5-106">Topic</span></span> | <span data-ttu-id="ecdd5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecdd5-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="ecdd5-108">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="ecdd5-108">**D3D12CreateDevice**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | <span data-ttu-id="ecdd5-109">Erstellt ein Gerät, das den Anzeige Adapter darstellt.</span><span class="sxs-lookup"><span data-stu-id="ecdd5-109">Creates a device that represents the display adapter.</span></span> |
| [<span data-ttu-id="ecdd5-110">**D3D12CreateRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="ecdd5-110">**D3D12CreateRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | <span data-ttu-id="ecdd5-111">Deserialisiert eine Stamm Signatur, sodass Sie die Layoutdefinition bestimmen können ([**D3D12 \_ root \_ Signature \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span><span class="sxs-lookup"><span data-stu-id="ecdd5-111">Deserializes a root signature so you can determine the layout definition ([**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span></span> |
| [<span data-ttu-id="ecdd5-112">**D3D12CreateVersionedRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="ecdd5-112">**D3D12CreateVersionedRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | <span data-ttu-id="ecdd5-113">Generiert eine Schnittstelle, die die deserialisierte Datenstruktur über [**getunconvertedrootsignaturedesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="ecdd5-113">Generates an interface that can return the deserialized data structure, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span></span> |
| [<span data-ttu-id="ecdd5-114">**D3D12EnableExperimentalFeatures**</span><span class="sxs-lookup"><span data-stu-id="ecdd5-114">**D3D12EnableExperimentalFeatures**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | <span data-ttu-id="ecdd5-115">Aktiviert eine Liste von experimentellen Features.</span><span class="sxs-lookup"><span data-stu-id="ecdd5-115">Enables a list of experimental features.</span></span> |
| [<span data-ttu-id="ecdd5-116">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="ecdd5-116">**D3D12GetDebugInterface**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | <span data-ttu-id="ecdd5-117">Ruft eine Debugschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="ecdd5-117">Gets a debug interface.</span></span> |
| [<span data-ttu-id="ecdd5-118">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="ecdd5-118">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | <span data-ttu-id="ecdd5-119">Serialisiert eine Stamm Signatur Version 1,0, die an [**ID3D12Device:: kreaterootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ecdd5-119">Serializes a root signature version 1.0 that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |
| [<span data-ttu-id="ecdd5-120">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="ecdd5-120">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | <span data-ttu-id="ecdd5-121">Serialisiert eine Stamm Signatur einer beliebigen Version, die an [**ID3D12Device:: kreaterootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ecdd5-121">Serializes a root signature of any version that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="ecdd5-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ecdd5-122">Related topics</span></span>

* [<span data-ttu-id="ecdd5-123">Core-Referenz</span><span class="sxs-lookup"><span data-stu-id="ecdd5-123">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="ecdd5-124">Direct3D 12-Referenz</span><span class="sxs-lookup"><span data-stu-id="ecdd5-124">Direct3D 12 reference</span></span>](direct3d-12-reference.md)






