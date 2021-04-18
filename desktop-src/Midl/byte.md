---
title: Byte-Attribut
description: Das Byte-Schlüsselwort gibt ein 8-Bit-Datenelement an.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- Byte-Attribut-Mittell
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340468"
---
# <a name="byte-attribute"></a><span data-ttu-id="e65e3-104">Byte-Attribut</span><span class="sxs-lookup"><span data-stu-id="e65e3-104">byte attribute</span></span>

<span data-ttu-id="e65e3-105">Das **Byte** -Schlüsselwort gibt ein 8-Bit-Datenelement an.</span><span class="sxs-lookup"><span data-stu-id="e65e3-105">The **byte** keyword specifies an 8-bit data item.</span></span>

``` syntax
byte identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="e65e3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e65e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e65e3-107">*Bezeichnername*</span><span class="sxs-lookup"><span data-stu-id="e65e3-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e65e3-108">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="e65e3-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="e65e3-109">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="e65e3-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e65e3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e65e3-110">Remarks</span></span>

<span data-ttu-id="e65e3-111">Ein **Byte** -Datenelement wird bei der Übertragung im Netzwerk nicht als [**char**](char-idl.md) -Typ konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e65e3-111">A **byte** data item does not undergo any conversion for transmission on the network as a [**char**](char-idl.md) type might.</span></span>

<span data-ttu-id="e65e3-112">Der **Bytetyp** ist einer der Basis Typen der IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="e65e3-112">The **byte** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="e65e3-113">Der **Bytetyp** kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e65e3-113">The **byte** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="e65e3-114">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="e65e3-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e65e3-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e65e3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65e3-116">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="e65e3-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e65e3-117">**Char**</span><span class="sxs-lookup"><span data-stu-id="e65e3-117">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="e65e3-118">**const**</span><span class="sxs-lookup"><span data-stu-id="e65e3-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e65e3-119">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="e65e3-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e65e3-120">**typedef**</span><span class="sxs-lookup"><span data-stu-id="e65e3-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




