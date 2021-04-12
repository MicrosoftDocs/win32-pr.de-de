---
title: Eingeschränktes Attribut
description: Das Attribut \ restricted \ gibt an, dass eine Bibliothek oder ein Member eines Moduls, einer Schnittstelle oder einer dispinterface nicht willkürlich aufgerufen werden kann.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- eingeschränkte Attribute-Mittell
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390250"
---
# <a name="restricted-attribute"></a><span data-ttu-id="dc671-104">Eingeschränktes Attribut</span><span class="sxs-lookup"><span data-stu-id="dc671-104">restricted attribute</span></span>

<span data-ttu-id="dc671-105">Das **\[ restricted \]** -Attribut gibt an, dass eine Bibliothek oder ein Member eines Moduls, einer Schnittstelle oder einer dispinterface nicht willkürlich aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc671-105">The **\[restricted\]** attribute specifies that a library, or member of a module, interface, or dispinterface cannot be called arbitrarily.</span></span>

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a><span data-ttu-id="dc671-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc671-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc671-107">*andere-Attribute*</span><span class="sxs-lookup"><span data-stu-id="dc671-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dc671-108">NULL oder mehr mittlere Attribute.</span><span class="sxs-lookup"><span data-stu-id="dc671-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="dc671-109">*Anweisungstyp*</span><span class="sxs-lookup"><span data-stu-id="dc671-109">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="dc671-110">Eines der folgenden: [**Library**](library.md), [**Module**](module.md), [**Interface**](interface.md), [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="dc671-110">One of the following: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc671-111">*Anweisungs Name*</span><span class="sxs-lookup"><span data-stu-id="dc671-111">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dc671-112">Der Bezeichner, mit dem sich die Software auf diese Anweisung bezieht.</span><span class="sxs-lookup"><span data-stu-id="dc671-112">The identifier by which the software refers to this statement.</span></span>

</dd> <dt>

<span data-ttu-id="dc671-113">*definiert*</span><span class="sxs-lookup"><span data-stu-id="dc671-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="dc671-114">Mittel l-Sprachelemente, die den Inhalt dieser Anweisung definieren.</span><span class="sxs-lookup"><span data-stu-id="dc671-114">MIDL language elements that define the contents of this statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc671-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc671-115">Remarks</span></span>

<span data-ttu-id="dc671-116">Mit diesem Attribut können Sie den Zugriff auf Elemente von Schnittstellen, Bibliotheken, Modulen und dispinterfaces steuern.</span><span class="sxs-lookup"><span data-stu-id="dc671-116">This attribute enables you to control access to elements of interfaces, libraries, modules, and dispinterfaces.</span></span> <span data-ttu-id="dc671-117">Beispielsweise kann verhindert werden, dass ein Datenelement von einem makroprogrammierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc671-117">For example, it can prevent a data item from being used by a macro programmer.</span></span> <span data-ttu-id="dc671-118">Sie können dieses Attribut auf einen Member einer Co- [**Klasse**](coclass.md)anwenden, unabhängig davon, ob der Member eine dispinterface oder eine Schnittstelle ist, und unabhängig davon, ob der Member eine Senke (eingehend) oder eine Quelle (ausgehend) ist.</span><span class="sxs-lookup"><span data-stu-id="dc671-118">You can apply this attribute to a member of a [**coclass**](coclass.md), independent of whether the member is a dispinterface or interface, and independent of whether the member is a sink (incoming) or source (outgoing).</span></span> <span data-ttu-id="dc671-119">Ein Member einer **Co-Klasse** kann nicht sowohl das **\[ restricted \]** -als auch das **\[ Default \]** -Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dc671-119">A member of a **coclass** cannot have both the **\[restricted\]** and **\[default\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="dc671-120">Flags</span><span class="sxs-lookup"><span data-stu-id="dc671-120">Flags</span></span>

<span data-ttu-id="dc671-121">impltypeflag " \_ frestrihiert", funkflag " \_ frestrihiert"</span><span class="sxs-lookup"><span data-stu-id="dc671-121">IMPLTYPEFLAG\_FRESTRICTED, FUNCFLAG\_FRESTRICTED</span></span>

## <a name="examples"></a><span data-ttu-id="dc671-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc671-122">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a><span data-ttu-id="dc671-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dc671-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc671-124">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="dc671-124">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="dc671-125">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="dc671-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="dc671-126">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="dc671-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="dc671-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="dc671-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="dc671-128">**Mond**</span><span class="sxs-lookup"><span data-stu-id="dc671-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="dc671-129">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="dc671-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="dc671-130">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="dc671-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="dc671-131">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="dc671-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 