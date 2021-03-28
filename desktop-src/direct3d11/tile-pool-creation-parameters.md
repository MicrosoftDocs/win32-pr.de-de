---
title: Parameter zum Erstellen des Kachelpools
description: Verwenden Sie die Parameter in diesem Abschnitt, um Kachel Pools über die ID3D11Device-API-API zu definieren.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036483"
---
# <a name="tile-pool-creation-parameters"></a><span data-ttu-id="53833-103">Parameter zum Erstellen des Kachelpools</span><span class="sxs-lookup"><span data-stu-id="53833-103">Tile pool creation parameters</span></span>

<span data-ttu-id="53833-104">Verwenden Sie die Parameter in diesem Abschnitt, um Kachel Pools über die [**ID3D11Device::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) -API zu definieren.</span><span class="sxs-lookup"><span data-stu-id="53833-104">Use the parameters in this section to define tile pools via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API.</span></span>

<dl> <dt>

<span data-ttu-id="53833-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Größe**</span><span class="sxs-lookup"><span data-stu-id="53833-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="53833-106">Zuordnungs Größe, als Vielfaches von 64 KB.</span><span class="sxs-lookup"><span data-stu-id="53833-106">Allocation size, as a multiple of 64KB.</span></span> <span data-ttu-id="53833-107">0 ist gültig, da Sie später einen [**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) -Vorgang verwenden können.</span><span class="sxs-lookup"><span data-stu-id="53833-107">0 is valid because you can later use a [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation.</span></span>

</dd> <dt>

<span data-ttu-id="53833-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Unterstützte ressourcenmisc-Flags**</span><span class="sxs-lookup"><span data-stu-id="53833-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="53833-109">D3D11 \_ \_ ressourcenmisc- \_ Kachel \_ Pool (identifiziert die Ressource als Kachel Pool), \_ D3D11 \_ ressourcenmisc \_ Shared, \_ Shared \_ keyedmutex oder \_ Shared \_ nthandle.</span><span class="sxs-lookup"><span data-stu-id="53833-109">D3D11\_RESOURCE\_MISC\_TILE\_POOL (identifies the resource as a tile pool), D3D11\_RESOURCE\_MISC\_SHARED, \_SHARED\_KEYEDMUTEX, or \_SHARED\_NTHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="53833-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Unterstützte Ressourcenverwendung**</span><span class="sxs-lookup"><span data-stu-id="53833-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="53833-111">D3D11 \_ \_ nur Verwendungs Standard.</span><span class="sxs-lookup"><span data-stu-id="53833-111">D3D11\_USAGE\_DEFAULT only.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="53833-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53833-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53833-113">Erstellen von Kachel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53833-113">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




