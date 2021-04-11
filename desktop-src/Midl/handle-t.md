---
title: handle_t-Attribut
description: Das Handle \_ t-Schlüsselwort deklariert ein Objekt, das dem primitiven handle-Handle \_ t entspricht. Ein Primitives Bindungs Handle ist ein Datenobjekt, das von der Anwendung zur Darstellung der Bindung verwendet werden kann.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t Attribut-Mittel l
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314822"
---
# <a name="handle_t-attribute"></a><span data-ttu-id="d66c3-105">Handle \_ t-Attribut</span><span class="sxs-lookup"><span data-stu-id="d66c3-105">handle\_t attribute</span></span>

<span data-ttu-id="d66c3-106">Das **handle \_ t** -Schlüsselwort deklariert ein Objekt, das dem primitiven handle-Handle **\_ t** entspricht.</span><span class="sxs-lookup"><span data-stu-id="d66c3-106">The **handle\_t** keyword declares an object to be of the primitive handle type **handle\_t**.</span></span> <span data-ttu-id="d66c3-107">Ein Primitives Bindungs Handle ist ein Datenobjekt, das von der Anwendung zur Darstellung der Bindung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d66c3-107">A primitive binding handle is a data object that can be used by the application to represent the binding.</span></span>

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a><span data-ttu-id="d66c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d66c3-108">Parameters</span></span>

<span data-ttu-id="d66c3-109">Dieses Attribut hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d66c3-109">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66c3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d66c3-110">Remarks</span></span>

<span data-ttu-id="d66c3-111">Der **handle \_ t** -Typ ist einer der vordefinierten Typen der IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="d66c3-111">The **handle\_t** type is one of the predefined types of the interface definition language (IDL).</span></span> <span data-ttu-id="d66c3-112">Sie kann als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabetyp-Spezifizierer und Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d66c3-112">It can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="d66c3-113">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="d66c3-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="d66c3-114">In Microsoft RPC können Parameter des Typs **handle \_ t** nur als in- **\[** [](in.md) **\]** Parametern auftreten.</span><span class="sxs-lookup"><span data-stu-id="d66c3-114">In Microsoft RPC, parameters of type **handle\_t** can occur only as **\[**[**in**](in.md)**\]** parameters.</span></span> <span data-ttu-id="d66c3-115">Primitive Handles können nicht über das **\[** [**Unique**](unique.md) - **\]** oder **\[** [**ptr**](ptr.md) - **\]** Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="d66c3-115">Primitive handles cannot have the **\[**[**unique**](unique.md)**\]** or **\[**[**ptr**](ptr.md)**\]** attribute.</span></span>

<span data-ttu-id="d66c3-116">Parameter vom Typ **handle \_ t** (primitive handle Parameters) werden nicht im Netzwerk übertragen.</span><span class="sxs-lookup"><span data-stu-id="d66c3-116">Parameters of type **handle\_t** (primitive handle parameters) are not transmitted on the network.</span></span>

## <a name="see-also"></a><span data-ttu-id="d66c3-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d66c3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66c3-118">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="d66c3-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="d66c3-119">Bindung und Handles</span><span class="sxs-lookup"><span data-stu-id="d66c3-119">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="d66c3-120">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="d66c3-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d66c3-121">**in**</span><span class="sxs-lookup"><span data-stu-id="d66c3-121">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="d66c3-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="d66c3-122">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="d66c3-123">**ptr**</span><span class="sxs-lookup"><span data-stu-id="d66c3-123">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="d66c3-124">**gem**</span><span class="sxs-lookup"><span data-stu-id="d66c3-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 