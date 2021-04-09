---
title: VARIANT-Struktur
description: Die meisten Funktionen von Microsoft Active Accessibility und die IAccessible-Eigenschaften und-Methoden übernehmen eine VARIANT-Struktur als Parameter. Im Wesentlichen handelt es sich bei der VARIANT-Struktur um einen Container für eine große Union, die viele Datentypen enthält.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101870"
---
# <a name="variant-structure"></a><span data-ttu-id="c2d1f-104">VARIANT-Struktur</span><span class="sxs-lookup"><span data-stu-id="c2d1f-104">VARIANT Structure</span></span>

<span data-ttu-id="c2d1f-105">Die meisten Funktionen von Microsoft Active Accessibility und die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften und-Methoden übernehmen eine [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur als Parameter.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-105">Most of the Microsoft Active Accessibility functions and the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods take a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure as a parameter.</span></span> <span data-ttu-id="c2d1f-106">Im Wesentlichen handelt es sich bei der **Variant** -Struktur um einen Container für eine große Union, die viele Datentypen enthält.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-106">Essentially, the **VARIANT** structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="c2d1f-107">Der Wert im ersten Element der Struktur, **VT**, beschreibt, welche der Union-Member gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-107">The value in the first member of the structure, **vt**, describes which of the union members is valid.</span></span> <span data-ttu-id="c2d1f-108">Obwohl die [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur viele verschiedene Datentypen unterstützt, werden von Microsoft Active Accessibility nur die folgenden Typen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-108">Although the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure supports many different data types, Microsoft Active Accessibility uses only the following types.</span></span>



| <span data-ttu-id="c2d1f-109">VT-Wert</span><span class="sxs-lookup"><span data-stu-id="c2d1f-109">vt Value</span></span>     | <span data-ttu-id="c2d1f-110">Entsprechender Wertelement Name</span><span class="sxs-lookup"><span data-stu-id="c2d1f-110">Corresponding value member name</span></span> |
|--------------|---------------------------------|
| <span data-ttu-id="c2d1f-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c2d1f-111">VT\_I4</span></span>       | <span data-ttu-id="c2d1f-112">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="c2d1f-112">**lVal**</span></span>                        |
| <span data-ttu-id="c2d1f-113">VT \_ -Verteilung</span><span class="sxs-lookup"><span data-stu-id="c2d1f-113">VT\_DISPATCH</span></span> | <span data-ttu-id="c2d1f-114">**pdispVal**</span><span class="sxs-lookup"><span data-stu-id="c2d1f-114">**pdispVal**</span></span>                    |
| <span data-ttu-id="c2d1f-115">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c2d1f-115">VT\_BSTR</span></span>     | <span data-ttu-id="c2d1f-116">**bstrauval**</span><span class="sxs-lookup"><span data-stu-id="c2d1f-116">**bstrVal**</span></span>                     |
| <span data-ttu-id="c2d1f-117">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="c2d1f-117">VT\_EMPTY</span></span>    | <span data-ttu-id="c2d1f-118">none</span><span class="sxs-lookup"><span data-stu-id="c2d1f-118">none</span></span>                            |



 

<span data-ttu-id="c2d1f-119">Wenn Sie Informationen in einer [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur erhalten, überprüfen Sie das **VT** -Element, um herauszufinden, welches Mitglied gültige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-119">When you receive information in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure, check the **vt** member to find out which member contains valid data.</span></span> <span data-ttu-id="c2d1f-120">Wenn Sie Informationen mithilfe einer **Variant** -Struktur senden, legen Sie auf ähnliche Weise fest, dass **VT** das Unionmember enthält, das die Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-120">Similarly, when you send information using a **VARIANT** structure, always set **vt** to reflect the union member that contains the information.</span></span>

<span data-ttu-id="c2d1f-121">Bevor Sie die-Struktur verwenden, initialisieren Sie Sie, indem Sie die [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) -Component Object Model (com)-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-121">Before using the structure, initialize it by calling the [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM) function.</span></span> <span data-ttu-id="c2d1f-122">Wenn die Struktur fertig ist, löschen Sie Sie, bevor der Speicher, der die [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) enthält, durch Aufrufen von [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-122">When finished with the structure, clear it before the memory that contains the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) is freed by calling [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span></span>

 

 