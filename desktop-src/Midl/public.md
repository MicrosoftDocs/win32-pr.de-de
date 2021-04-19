---
title: Öffentliches Attribut
description: Das \ Public \-Attribut enthält einen Alias, der mit dem typedef-Schlüsselwort in der Typbibliothek deklariert wurde.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- öffentliches Attribut, Mittel l
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338255"
---
# <a name="public-attribute"></a><span data-ttu-id="b2607-104">Öffentliches Attribut</span><span class="sxs-lookup"><span data-stu-id="b2607-104">public attribute</span></span>

<span data-ttu-id="b2607-105">Das **\[ Public \]** -Attribut enthält einen Alias, der mit dem [**typedef**](typedef.md) -Schlüsselwort in der Typbibliothek deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="b2607-105">The **\[public\]** attribute includes an alias declared with the [**typedef**](typedef.md) keyword in the type library.</span></span>

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a><span data-ttu-id="b2607-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2607-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2607-107">*Datentyp*</span><span class="sxs-lookup"><span data-stu-id="b2607-107">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b2607-108">Der Datentyp, für den der Bezeichner als Alias verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2607-108">The data type that the identifier will be an alias for.</span></span>

</dd> <dt>

<span data-ttu-id="b2607-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="b2607-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="b2607-110">Ein weiterer Name, nach dem der *Datentyp* in der Software bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b2607-110">Another name by which *data-type* will be known in the software.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2607-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2607-111">Remarks</span></span>

<span data-ttu-id="b2607-112">Standardmäßig wird ein Alias, der mit [**typedef**](typedef.md) deklariert wird und keine anderen Attribute hat, als **\# define** behandelt und ist nicht in der Typbibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2607-112">By default, an alias that is declared with [**typedef**](typedef.md) and has no other attributes is treated as a **\#define** and is not included in the type library.</span></span> <span data-ttu-id="b2607-113">Durch die Verwendung des **\[ Public \]** -Attributs wird sichergestellt, dass der Alias Teil der Typbibliothek ist.</span><span class="sxs-lookup"><span data-stu-id="b2607-113">Using the **\[public\]** attribute ensures that the alias becomes part of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="b2607-114">Der mittlerer l-Compiler erfordert, dass Sie das **\[ öffentliche \]** Attribut explizit auf jede typedef anwenden, die öffentlich sein soll.</span><span class="sxs-lookup"><span data-stu-id="b2607-114">The MIDL compiler requires that you explicitly apply the **\[public\]** attribute to each typedef that you want public.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b2607-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2607-115">Examples</span></span>

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a><span data-ttu-id="b2607-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2607-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2607-117">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="b2607-117">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b2607-118">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b2607-118">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b2607-119">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="b2607-119">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="b2607-120">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b2607-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b2607-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="b2607-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 