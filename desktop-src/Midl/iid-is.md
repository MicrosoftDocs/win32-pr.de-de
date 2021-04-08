---
title: iid_is-Attribut
description: Das Attribut \ IID \_ is \ Pointer gibt die IID der COM-Schnittstelle an, auf die von einem Schnittstellen Zeiger verwiesen wird.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037820"
---
# <a name="iid_is-attribute"></a><span data-ttu-id="cf3ab-104">IID \_ ist Attribut</span><span class="sxs-lookup"><span data-stu-id="cf3ab-104">iid\_is attribute</span></span>

<span data-ttu-id="cf3ab-105">Die **\[ IID \_ ist \]** ein Zeiger Attribut, das die IID der COM-Schnittstelle angibt, auf die von einem Schnittstellen Zeiger verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-105">The **\[iid\_is\]** pointer attribute specifies the IID of the COM interface pointed to by an interface pointer.</span></span>

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a><span data-ttu-id="cf3ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf3ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf3ab-107">*eingeschränkter Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="cf3ab-107">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="cf3ab-108">Gibt einen C-sprach Ausdruck an.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-108">Specifies a C-language expression.</span></span> <span data-ttu-id="cf3ab-109">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-109">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="cf3ab-110">"Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-110">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf3ab-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf3ab-111">Remarks</span></span>

<span data-ttu-id="cf3ab-112">Sie können **\[ IID \_ \]** in Attribut Listen für Funktionsparameter und für Struktur-oder Union-Member verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-112">You can use **\[iid\_is\]** in attribute lists for function parameters and for structure or union members.</span></span> <span data-ttu-id="cf3ab-113">Die stuader verwenden die IID, um zu bestimmen, wie der Schnittstellen Zeiger gemarshallt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-113">The stubs use the IID to determine how to marshal the interface pointer.</span></span> <span data-ttu-id="cf3ab-114">Dies ist nützlich für einen Schnittstellen Zeiger, der als Basisklassen Parameter typisiert ist.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-114">This is useful for an interface pointer that is typed as a base class parameter.</span></span>

<span data-ttu-id="cf3ab-115">Dateien, die das **\[ IID \_ \]** -Attribut verwenden, müssen mit dem mittlerer l-Compiler im Standardmodus kompiliert werden, der nicht den [**/OSF**](-osf.md) -Schalter verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf3ab-115">Files that use the **\[iid\_is\]** attribute must be compiled with the MIDL compiler in default mode, that is not using the [**/osf**](-osf.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="cf3ab-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf3ab-116">Examples</span></span>

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a><span data-ttu-id="cf3ab-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf3ab-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3ab-118">**Objekt (object)**</span><span class="sxs-lookup"><span data-stu-id="cf3ab-118">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="cf3ab-119">**UUID**</span><span class="sxs-lookup"><span data-stu-id="cf3ab-119">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




