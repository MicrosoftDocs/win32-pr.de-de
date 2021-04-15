---
title: Struktur-und Union-Attribute
description: Verwenden Sie die Switch \_ \-Attribute, um das Merkmal einer Union in einem Remote Prozedur aufzurufen. Verwenden Sie das Ignore-Attribut, um bestimmte Struktur-oder Union-Member als lokales Element für die Client Anwendung festzulegen.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL-Mittell, Attribute, Struktur und Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471141"
---
# <a name="structure-and-union-attributes"></a><span data-ttu-id="47328-105">Struktur-und Union-Attribute</span><span class="sxs-lookup"><span data-stu-id="47328-105">Structure and Union Attributes</span></span>

<span data-ttu-id="47328-106">Verwenden Sie **die \_ Switch** - \* Attribute, um das Merkmal einer Union in einem Remote Prozedur aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="47328-106">Use the **switch\_**\* attributes to specify the characteristic of a union in a remote procedure call.</span></span> <span data-ttu-id="47328-107">Verwenden Sie das [**Ignore**](ignore.md) -Attribut, um bestimmte Struktur-oder Union-Member als lokales Element für die Client Anwendung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="47328-107">Use the [**ignore**](ignore.md) attribute to designate certain structure or union members as local to the client application.</span></span>



| <span data-ttu-id="47328-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="47328-108">Attribute</span></span>                           | <span data-ttu-id="47328-109">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="47328-109">Usage</span></span>                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47328-110">**Not**</span><span class="sxs-lookup"><span data-stu-id="47328-110">**switch**</span></span>](switch.md)            | <span data-ttu-id="47328-111">Wählt die Diskriminante für eine gekapselte Union aus.</span><span class="sxs-lookup"><span data-stu-id="47328-111">Selects the discriminant for an encapsulated union.</span></span>                                                                           |
| [<span data-ttu-id="47328-112">**Switch \_ ist**</span><span class="sxs-lookup"><span data-stu-id="47328-112">**switch\_is**</span></span>](switch-is.md)     | <span data-ttu-id="47328-113">Identifiziert den Diskriminanten für eine nicht gekapselte Union.</span><span class="sxs-lookup"><span data-stu-id="47328-113">Identifies the discriminant for a nonencapsulated union.</span></span>                                                                      |
| [<span data-ttu-id="47328-114">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="47328-114">**switch\_type**</span></span>](switch-type.md) | <span data-ttu-id="47328-115">Identifiziert den Typ des Diskriminanten für eine nicht gekapselte Union.</span><span class="sxs-lookup"><span data-stu-id="47328-115">Identifies the type of the discriminant for a nonencapsulated union.</span></span>                                                          |
| [<span data-ttu-id="47328-116">**lassen**</span><span class="sxs-lookup"><span data-stu-id="47328-116">**ignore**</span></span>](ignore.md)            | <span data-ttu-id="47328-117">Gibt an, dass ein in einer Struktur oder Union enthaltener Zeiger und das vom Zeiger festgestellte Objekt nicht übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="47328-117">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span> |



 

<span data-ttu-id="47328-118">Sie können auch die [Zeiger Attribute Array und Format](array-and-sized-pointer-attributes.md) verwenden, um die Merkmale von Struktur-oder Union-Membern anzugeben.</span><span class="sxs-lookup"><span data-stu-id="47328-118">You can also use the [array and sized pointer attributes](array-and-sized-pointer-attributes.md) to specify characteristics of structure or union members.</span></span>

 

 




