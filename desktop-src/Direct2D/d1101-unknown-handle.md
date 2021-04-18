---
title: D1101 unbekanntes handle
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Eine Schnittstelle, die nicht von dieser DLL zugewiesen wurde, wurde an Sie übermittelt.
keywords:
- D1101 unbekanntes handle Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106368703"
---
# <a name="d1101-unknown-handle"></a><span data-ttu-id="2d5c9-104">D1101: Unbekanntes handle</span><span class="sxs-lookup"><span data-stu-id="2d5c9-104">D1101: Unknown Handle</span></span>

<span data-ttu-id="2d5c9-105">Eine Schnitt \[ *Stelle* \] , die von dieser DLL nicht zugeordnet wurde, wurde an Sie übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2d5c9-105">An interface \[*interface*\] not allocated by this DLL was passed to it.</span></span>

## <a name="placeholders"></a><span data-ttu-id="2d5c9-106">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="2d5c9-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="2d5c9-107"><span id="interface"></span><span id="INTERFACE"></span>*berfläche*</span><span class="sxs-lookup"><span data-stu-id="2d5c9-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="2d5c9-108">Die Adresse der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2d5c9-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="2d5c9-109">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="2d5c9-109">Possible Causes</span></span>

<span data-ttu-id="2d5c9-110">Ungültige Ressourcenverwendung.</span><span class="sxs-lookup"><span data-stu-id="2d5c9-110">Invalid resource usage.</span></span> <span data-ttu-id="2d5c9-111">Die Ressource, die außerhalb von Direct2D erstellt wurde, wird mit einer Direct2D-Factory verwendet, oder die auf einer Factory erstellten Ressourcen wurden mit einer Ressource verwendet, die von einer anderen Factory erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2d5c9-111">The resource created outside of Direct2D is used with a Direct2D factory, or the resources created on one factory was used with a resource created by another factory.</span></span>

 

 




