---
title: pointer_default-Attribut
description: Das Attribut \ Zeiger \_ default \ gibt das Standard Zeiger Attribut für alle Zeiger außer der Spitze der obersten Ebene an, die in Parameterlisten angezeigt werden.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- Pointer_default Attribut-Mittel l
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038844"
---
# <a name="pointer_default-attribute"></a><span data-ttu-id="c7b16-104">Zeiger- \_ Standard Attribut</span><span class="sxs-lookup"><span data-stu-id="c7b16-104">pointer\_default attribute</span></span>

<span data-ttu-id="c7b16-105">Das **\[ \_ Default \] -Zeiger** Attribut gibt das Standard Zeiger Attribut für alle Zeiger außer der Spitze der obersten Ebene an, die in Parameterlisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c7b16-105">The **\[pointer\_default\]** attribute specifies the default pointer attribute for all pointers except top-level pointers that appear in parameter lists.</span></span>

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a><span data-ttu-id="c7b16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7b16-106">Parameters</span></span>

<span data-ttu-id="c7b16-107">Dieses Attribut hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7b16-107">This attribute has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="c7b16-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7b16-108">Examples</span></span>

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="c7b16-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7b16-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b16-110">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="c7b16-110">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="c7b16-111">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="c7b16-111">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7b16-112">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="c7b16-112">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="c7b16-113">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="c7b16-113">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="c7b16-114">**ptr**</span><span class="sxs-lookup"><span data-stu-id="c7b16-114">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="c7b16-115">**ref**</span><span class="sxs-lookup"><span data-stu-id="c7b16-115">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="c7b16-116">**gem**</span><span class="sxs-lookup"><span data-stu-id="c7b16-116">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="c7b16-117">Standard Zeiger Typen</span><span class="sxs-lookup"><span data-stu-id="c7b16-117">Default Pointer Types</span></span>](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 