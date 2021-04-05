---
title: Zeiger-Typattribute
description: Die folgenden Attribute geben die Merkmale von Zeigern an.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL-Mittell, Attribute, Zeigertyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714357"
---
# <a name="pointer-type-attributes"></a><span data-ttu-id="615c1-104">Zeiger-Typattribute</span><span class="sxs-lookup"><span data-stu-id="615c1-104">Pointer Type Attributes</span></span>

<span data-ttu-id="615c1-105">Die folgenden Attribute geben die Merkmale von Zeigern an.</span><span class="sxs-lookup"><span data-stu-id="615c1-105">The following attributes specify the characteristics of pointers.</span></span>



| <span data-ttu-id="615c1-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="615c1-106">Attribute</span></span>                                   | <span data-ttu-id="615c1-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="615c1-107">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="615c1-108">**ptr**</span><span class="sxs-lookup"><span data-stu-id="615c1-108">**ptr**</span></span>](ptr.md)                          | <span data-ttu-id="615c1-109">Legt einen Zeiger als vollständigen Zeiger fest, der alle Funktionen eines C-sprach Zeigers enthält, einschließlich Aliasing.</span><span class="sxs-lookup"><span data-stu-id="615c1-109">Designates a pointer as a full pointer, with all the capabilities of a C-language pointer, including aliasing.</span></span>                                                                                       |
| [<span data-ttu-id="615c1-110">**ref**</span><span class="sxs-lookup"><span data-stu-id="615c1-110">**ref**</span></span>](ref.md)                          | <span data-ttu-id="615c1-111">Legt den einfachsten Zeigertyp in der mittleren l fest – einen, der einfach die Adresse einiger Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="615c1-111">Designates the simplest type of pointer in MIDL—one that simply provides the address of some data.</span></span> <span data-ttu-id="615c1-112">Verweis Zeiger können niemals NULL sein.</span><span class="sxs-lookup"><span data-stu-id="615c1-112">Reference pointers can never be null.</span></span>                                                             |
| [<span data-ttu-id="615c1-113">**gem**</span><span class="sxs-lookup"><span data-stu-id="615c1-113">**unique**</span></span>](unique.md)                    | <span data-ttu-id="615c1-114">Ermöglicht, dass ein Zeiger NULL ist, aber keine Aliasing unterstützt.</span><span class="sxs-lookup"><span data-stu-id="615c1-114">Lets a pointer be null, but does not support aliasing.</span></span>                                                                                                                                               |
| [<span data-ttu-id="615c1-115">**Zeiger \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="615c1-115">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="615c1-116">Wird auf eine Schnittstelle angewendet, um den Standard Zeigertyp für alle Zeiger in dieser Schnittstelle anzugeben, außer für Parameter Zeiger der obersten Ebene, die [**automatisch auf Verweis**](ref.md) Zeiger festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="615c1-116">Applied to an interface to specify the default pointer type for all pointers in that interface, except for top-level parameter pointers, which automatically default to [**ref**](ref.md) pointers.</span></span> |
| [<span data-ttu-id="615c1-117">**IID \_ ist**</span><span class="sxs-lookup"><span data-stu-id="615c1-117">**iid\_is**</span></span>](iid-is.md)                   | <span data-ttu-id="615c1-118">Stellt den Schnittstellen Bezeichner der COM-Schnittstelle bereit, die das-Objekt des Zeigers ist.</span><span class="sxs-lookup"><span data-stu-id="615c1-118">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                                                                                            |
| [<span data-ttu-id="615c1-119">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="615c1-119">**string**</span></span>](string.md)                    | <span data-ttu-id="615c1-120">Gibt an, dass der Zeiger auf eine Zeichenfolge zeigt.</span><span class="sxs-lookup"><span data-stu-id="615c1-120">Specifies that the pointer points to a string.</span></span>                                                                                                                                                       |



 

 

 




