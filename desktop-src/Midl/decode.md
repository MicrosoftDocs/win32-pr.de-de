---
title: Attribut decodieren
description: Das Attribut \ Decode \ ACF gibt an, dass eine Prozedur oder ein Typ die deserialisierungsunterstützung benötigt.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Decodieren von attributmittell
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314906"
---
# <a name="decode-attribute"></a><span data-ttu-id="504e5-104">Attribut decodieren</span><span class="sxs-lookup"><span data-stu-id="504e5-104">decode attribute</span></span>

<span data-ttu-id="504e5-105">Das Attribut "ACF **\[ decodieren \]** " gibt an, dass eine Prozedur oder ein Typ die deserialisierungsunterstützung benötigt.</span><span class="sxs-lookup"><span data-stu-id="504e5-105">The **\[decode\]** ACF attribute specifies that a procedure or a type needs de-serialization support.</span></span>

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="504e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="504e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="504e5-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="504e5-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="504e5-108">Gibt andere Attribute an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="504e5-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="504e5-109">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="504e5-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="504e5-110">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="504e5-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="504e5-111">*Schnittstellen Definition*</span><span class="sxs-lookup"><span data-stu-id="504e5-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="504e5-112">Gibt IDL-Anweisungen an, die die Definition der-Schnittstelle bilden.</span><span class="sxs-lookup"><span data-stu-id="504e5-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="504e5-113">*OP-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="504e5-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="504e5-114">Gibt andere operative Attribute an, die für die Prozedur gelten, z **\[** . b. [**Codieren**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="504e5-114">Specifies other operational attributes that apply to the procedure such as **\[**[**encode**](encode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="504e5-115">*proc-Name*</span><span class="sxs-lookup"><span data-stu-id="504e5-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="504e5-116">Gibt den Namen der Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="504e5-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="504e5-117">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="504e5-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="504e5-118">Gibt andere Attribute an, z **\[** . b. [**Codieren**](encode.md) **\]** und **\[** [**zuordnen**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="504e5-118">Specifies other attributes such as **\[**[**encode**](encode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="504e5-119">*Typname*</span><span class="sxs-lookup"><span data-stu-id="504e5-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="504e5-120">Gibt einen Typ an, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="504e5-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="504e5-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="504e5-121">Remarks</span></span>

<span data-ttu-id="504e5-122">Das Attribut " **\[ decodieren \]** " bewirkt, dass der Mittell-Compiler Code generiert, mit dem eine Anwendung serialisierte Daten aus einem Puffer abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="504e5-122">The **\[decode\]** attribute causes the MIDL compiler to generate code that an application can use to retrieve serialized data from a buffer.</span></span> <span data-ttu-id="504e5-123">Das **\[** [**Codieren**](encode.md) - **\]** Attribut bietet Serialisierungsunterstützung und erzeugt den Code zum Serialisieren von Daten in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="504e5-123">The **\[**[**encode**](encode.md)**\]** attribute provides serialization support, generating the code to serialize data into a buffer.</span></span>

<span data-ttu-id="504e5-124">Verwenden **\[** Sie die Attribute [**Codieren**](encode.md) **\]** und **\[ decodieren \]** in einer ACF, um Serialisierungscode für Prozeduren oder Typen zu generieren, die in der IDL-Datei einer Schnittstelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="504e5-124">Use the **\[**[**encode**](encode.md)**\]** and **\[decode\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="504e5-125">Wenn die **\[ Decodierung \]** als Schnittstellen Attribut verwendet wird, gilt sie für alle Typen und Prozeduren, die in der IDL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="504e5-125">When used as an interface attribute, **\[decode\]** applies to all types and procedures defined in the IDL file.</span></span> <span data-ttu-id="504e5-126">Wenn die **\[ Decodierung \]** als Type-Attribut verwendet wird, gilt sie nur für den angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="504e5-126">When used as a type attribute, **\[decode\]** applies only to the specified type.</span></span> <span data-ttu-id="504e5-127">Wenn die **\[ Decodierung \]** als Betriebs Attribut verwendet wird, gilt sie nur für diese Prozedur.</span><span class="sxs-lookup"><span data-stu-id="504e5-127">When used as an operational attribute, **\[decode\]** applies only to that procedure.</span></span>

<span data-ttu-id="504e5-128">Weitere Informationen zur Verwendung dieser Serialisierungsunterstützung finden Sie unter [Serialisierung Services](/windows/desktop/Rpc/serialization-services) und **\[** [**Codieren**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="504e5-128">For more information about using this serialization support, see [Serialization Services](/windows/desktop/Rpc/serialization-services) and **\[**[**encode**](encode.md)**\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="504e5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="504e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="504e5-130">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="504e5-130">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="504e5-131">**allocate**</span><span class="sxs-lookup"><span data-stu-id="504e5-131">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="504e5-132">**Codieren**</span><span class="sxs-lookup"><span data-stu-id="504e5-132">**encode**</span></span>](encode.md)
</dt> </dl>

 

 