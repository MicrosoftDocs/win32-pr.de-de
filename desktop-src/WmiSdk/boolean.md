---
title: boolescher Wert (WMI)
description: Ein VT \_ bool-Parameter, der den Wert von Variant \_ true (&\# 8211; 1) oder Variant \_ false (0) annimmt.
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369761"
---
# <a name="boolean-wmi"></a><span data-ttu-id="2af4d-103">boolescher Wert (WMI)</span><span class="sxs-lookup"><span data-stu-id="2af4d-103">boolean (WMI)</span></span>

<span data-ttu-id="2af4d-104">Der boolesche Datentyp ist ein VT \_ bool-Parameter, der den Wert von Variant \_ true (– 1) oder Variant \_ false (0) annimmt.</span><span class="sxs-lookup"><span data-stu-id="2af4d-104">The boolean data type is a VT\_BOOL parameter that takes on the value of VARIANT\_TRUE (–1) or VARIANT\_FALSE (0).</span></span> <span data-ttu-id="2af4d-105">In der folgenden Tabelle werden die Unterschiede zwischen den programmgesteuerten Darstellungen von Logical **true** in C/C++ und dem Automatisierungstyp aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2af4d-105">The following table lists the difference between the programmatic representations of logical **TRUE** in C/C++ and the Automation type.</span></span>

| <span data-ttu-id="2af4d-106">Sprache</span><span class="sxs-lookup"><span data-stu-id="2af4d-106">Language</span></span>   | <span data-ttu-id="2af4d-107">Wert</span><span class="sxs-lookup"><span data-stu-id="2af4d-107">Value</span></span>         | <span data-ttu-id="2af4d-108">Numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="2af4d-108">Numerical value</span></span> |
|------------|---------------|-----------------|
| <span data-ttu-id="2af4d-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="2af4d-109">C/C++</span></span>      | <span data-ttu-id="2af4d-110">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="2af4d-110">**TRUE**</span></span>      | <span data-ttu-id="2af4d-111">1</span><span class="sxs-lookup"><span data-stu-id="2af4d-111">1</span></span>               |
| <span data-ttu-id="2af4d-112">Automation</span><span class="sxs-lookup"><span data-stu-id="2af4d-112">Automation</span></span> | <span data-ttu-id="2af4d-113">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="2af4d-113">VARIANT\_TRUE</span></span> | <span data-ttu-id="2af4d-114">–1</span><span class="sxs-lookup"><span data-stu-id="2af4d-114">–1</span></span>              |

<span data-ttu-id="2af4d-115">Beide Typen sind ungleich 0 (null) und daher nicht " **false**", aber unterschiedliche Darstellungen für " **true**".</span><span class="sxs-lookup"><span data-stu-id="2af4d-115">Both types are nonzero and therefore not **FALSE**, but have different representations for **TRUE**.</span></span>
