---
description: Erfahren Sie mehr über die Enumerationen, die in der api für die nebeneinander seitige Assembly verwendet werden, z. B. ASM_CMP_FLAGS und CREATE_ASM_NAME_OBJ_FLAGS.
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: Nebenseitige Assemblyenumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f393ab9d8657ecaa52cad555dad5a831699687
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404743"
---
# <a name="side-by-side-assembly-enumerations"></a><span data-ttu-id="2cd52-103">Nebenseitige Assemblyenumeration</span><span class="sxs-lookup"><span data-stu-id="2cd52-103">Side-by-Side Assembly Enumerations</span></span>

<span data-ttu-id="2cd52-104">Die API für die seitige Assembly verwendet die folgenden Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="2cd52-104">The side-by-side assembly API uses the following enumerations.</span></span>



| <span data-ttu-id="2cd52-105">Enumeration</span><span class="sxs-lookup"><span data-stu-id="2cd52-105">Enumeration</span></span>                                                         | <span data-ttu-id="2cd52-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cd52-106">Description</span></span>                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cd52-107">**\_ASM-CMP-FLAGS \_**</span><span class="sxs-lookup"><span data-stu-id="2cd52-107">**ASM\_CMP\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | <span data-ttu-id="2cd52-108">Wird von der [**IsEqual-Methode**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) verwendet, um anzugeben, welche Teile von zwei Assemblynamen verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="2cd52-108">Used by the [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) method to specify which parts of two assembly names to compare.</span></span>                                                                       |
| [<span data-ttu-id="2cd52-109">**\_ \_ ASM-ANZEIGEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="2cd52-109">**ASM\_DISPLAY\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | <span data-ttu-id="2cd52-110">Wird von der [**GetDisplayName-Methode**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) verwendet, um anzugeben, welche Teile des nebenseitigen Assemblynamens in die Zeichenfolgendarstellung des Namens enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="2cd52-110">Used by the [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) method to specify which portions of the side-by-side assembly name to include in the string representation of the name.</span></span> |
| [<span data-ttu-id="2cd52-111">**\_ASM-NAME**</span><span class="sxs-lookup"><span data-stu-id="2cd52-111">**ASM\_NAME**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | <span data-ttu-id="2cd52-112">Eigenschaften-IDs für die Name-Wert-Paare in einem nebeneinander angegebenen Assemblynamen.</span><span class="sxs-lookup"><span data-stu-id="2cd52-112">Property IDs for the name-value pairs in an side-by-side assembly name.</span></span>                                                                                                                    |
| [<span data-ttu-id="2cd52-113">**ERSTELLEN \_ VON \_ ASM-NAMENS-OBJ-FLAGS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2cd52-113">**CREATE\_ASM\_NAME\_OBJ\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | <span data-ttu-id="2cd52-114">Wird von der [**CreateAssemblyNameObject-Funktion verwendet,**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) um den namen der seiteseitigen Assembly anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2cd52-114">Used by the [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) function to specify the side-by-side assembly name.</span></span>                                                               |



 

 

 



