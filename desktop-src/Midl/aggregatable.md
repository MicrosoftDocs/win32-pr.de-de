---
title: Aggregierbares Attribut
description: Das Attribut \ aggregatable \ gibt an, dass die Klasse Aggregationen unterstützt.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- Zusammenfassung des aggregierbare-Attributs
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314841"
---
# <a name="aggregatable-attribute"></a><span data-ttu-id="58d0d-104">Aggregierbares Attribut</span><span class="sxs-lookup"><span data-stu-id="58d0d-104">aggregatable attribute</span></span>

<span data-ttu-id="58d0d-105">Das Aggregat Attribut gibt an, dass die-Klasse **\[ Aggregationen \]** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58d0d-105">The **\[aggregatable\]** attribute indicates that the class supports aggregation.</span></span>

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="58d0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58d0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d0d-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="58d0d-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="58d0d-108">Andere Attribute, die auf die-Klasse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="58d0d-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="58d0d-109">*Name der Co-Klasse*</span><span class="sxs-lookup"><span data-stu-id="58d0d-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="58d0d-110">Der Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="58d0d-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="58d0d-111">*coclass-Interface-List*</span><span class="sxs-lookup"><span data-stu-id="58d0d-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="58d0d-112">Eine Liste der Schnittstellen für die-Klasse.</span><span class="sxs-lookup"><span data-stu-id="58d0d-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58d0d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58d0d-113">Remarks</span></span>

<span data-ttu-id="58d0d-114">Verwenden Sie das **\[ aggregierbare \]** -Attribut einer [**Co-Klasse**](coclass.md) -Anweisung, um den Benutzern mitzuteilen, dass die-Klasse Aggregationen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58d0d-114">Use the **\[aggregatable\]** attribute on a [**coclass**](coclass.md) statement to let users know that the class supports aggregations.</span></span> <span data-ttu-id="58d0d-115">Das heißt, die-Klasse ermöglicht es, dass ihre Schnittstellen von einer Container Klasse verfügbar gemacht werden, als wären diese Schnittstellen die eigenen Schnittstellen des Containers.</span><span class="sxs-lookup"><span data-stu-id="58d0d-115">That is, the class allows its interfaces to be exposed by a container class as if these interfaces were the container's own interfaces.</span></span>

<span data-ttu-id="58d0d-116">Die TYPEFLAG-Darstellung für dieses Attribut ist "TYPEFLAG" \_ .</span><span class="sxs-lookup"><span data-stu-id="58d0d-116">The typeflag representation for this attribute is TYPEFLAG\_FAGGREGATABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="58d0d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58d0d-117">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="58d0d-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58d0d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d0d-119">**coclass**</span><span class="sxs-lookup"><span data-stu-id="58d0d-119">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="58d0d-120">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="58d0d-120">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="58d0d-121">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="58d0d-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="58d0d-122">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="58d0d-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 