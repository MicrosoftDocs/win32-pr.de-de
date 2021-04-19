---
description: Ein portabler Typ, der zum Darstellen eines Vektors von Gleit Komma-oder ganzzahligen 4 32-Bit-Komponenten verwendet wird, die jeweils optimal ausgerichtet und einem Hardware Vektor Register zugeordnet sind.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Xmvector-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361284"
---
# <a name="xmvector-data-type"></a><span data-ttu-id="d0b4f-103">Xmvector-Datentyp</span><span class="sxs-lookup"><span data-stu-id="d0b4f-103">XMVECTOR Data Type</span></span>

<span data-ttu-id="d0b4f-104">Ein portabler Typ, der zum Darstellen eines Vektors von Gleit Komma-oder ganzzahligen 4 32-Bit-Komponenten verwendet wird, die jeweils optimal ausgerichtet und einem Hardware Vektor Register zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-104">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b4f-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0b4f-105">Remarks</span></span>

<span data-ttu-id="d0b4f-106">Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die `XMVECTOR` beim Programmieren in C++ verfügbar sind, finden Sie unter [xmvector Extensions](ovw-xmvector-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="d0b4f-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTOR` when programming in C++, see [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span></span>

<span data-ttu-id="d0b4f-107">In der directxmath-Bibliothek ist ein nicht transparenter Typ, um Portabilität und Optimierung vollständig zu unterstützen `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="d0b4f-107">In the DirectXMath Library, to fully support portability and optimization, `XMVECTOR` is, by design, an opaque type.</span></span> <span data-ttu-id="d0b4f-108">Die tatsächliche Implementierung von `XMVECTOR` ist plattformabhängig.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-108">The actual implementation of `XMVECTOR` is platform dependent.</span></span>

<span data-ttu-id="d0b4f-109">Im Allgemeinen sollte Code nicht auf die Besonderheiten einer bestimmten plattformspezifischen Implementierung von beruhen `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="d0b4f-109">In general, code should not rely on the specifics of any given platform specific implementation of `XMVECTOR`.</span></span> <span data-ttu-id="d0b4f-110">Plattformspezifische Implementierungen haben folgende Merkmale:</span><span class="sxs-lookup"><span data-stu-id="d0b4f-110">Platform-specific implementations have these characteristics:</span></span>

-   <span data-ttu-id="d0b4f-111">Sie sind nicht portabel.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-111">They are not portable.</span></span>
-   <span data-ttu-id="d0b4f-112">Sie können sich zwischen Releases ändern.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-112">They may change between releases.</span></span>
-   <span data-ttu-id="d0b4f-113">Die Verletzung der Verwendung von Implementierungsdetails ist möglicherweise suboptimal.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-113">Injudicious use of implementation details may be suboptimal.</span></span>

<span data-ttu-id="d0b4f-114">Entwickler sollten die Funktionen " [Accessor](ovw-xnamath-reference-functions-accessors.md)", " [Load](ovw-xnamath-reference-functions-load.md)" und " [Store](ovw-xnamath-reference-functions-storage.md) " der directxmath-Bibliothek verwenden, um die Vektoren zu erhalten und festzulegen, und die [Bibliotheks-4D-Vektor Funktionen der directxmath-Bibliothek](ovw-xnamath-reference-functions-vector4.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b4f-114">Developers should use DirectXMath Library's [accessor](ovw-xnamath-reference-functions-accessors.md), [load](ovw-xnamath-reference-functions-load.md), and [store](ovw-xnamath-reference-functions-storage.md) functions to get and set the vectors, and the [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) to manipulate them.</span></span>

<span data-ttu-id="d0b4f-115">Informationen zu-Projekten, die ausführliche Informationen zur Implementierung `XMVECTOR` von auf verschiedenen Plattformen benötigen, finden Sie unter [Bibliotheks internale](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="d0b4f-115">For projects that need detailed information about how to implement `XMVECTOR` on different platforms, see [Library Internals](pg-xnamath-internals.md).</span></span>

### <a name="compiler-aliases"></a><span data-ttu-id="d0b4f-116">Compileraliase</span><span class="sxs-lookup"><span data-stu-id="d0b4f-116">Compiler Aliases</span></span>

<span data-ttu-id="d0b4f-117">In der Header Datei "directxmath. h" werden Aliase für das- `XMVECTOR` Objekt verwendet, insbesondere " **cxmvector** " und " **fxmvector**".</span><span class="sxs-lookup"><span data-stu-id="d0b4f-117">The DirectXMath.h header file uses aliases to the `XMVECTOR` object, specifically **CXMVECTOR** and **FXMVECTOR**.</span></span> <span data-ttu-id="d0b4f-118">Der Header verwendet diese Aliase, um die optimalen Inline Aufruf Konventionen verschiedener Compiler einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-118">The header uses these aliases to comply with the optimal in-line calling conventions of different compilers.</span></span> <span data-ttu-id="d0b4f-119">Bei den meisten Projekten, für die directxmath verwendet wird, genügt es, diese Typen als exakten Alias für zu behandeln `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="d0b4f-119">For most projects that use DirectXMath it is sufficient to treat these types as an exact alias to `XMVECTOR`.</span></span>

<span data-ttu-id="d0b4f-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d0b4f-120">For example:</span></span>


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



<span data-ttu-id="d0b4f-121">Informationen zu-Projekten, die ausführliche Informationen dazu benötigen, wie verschiedene Plattformen ihre Aufruf Konventionen verarbeiten, finden Sie unter [Bibliotheks](pg-xnamath-internals.md)interne Informationen.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-121">For projects that need detailed information about how different platforms handle their calling conventions, see [Library Internals](pg-xnamath-internals.md).</span></span>

<span data-ttu-id="d0b4f-122">Bei xnamath 2. x hat der `XMVECTOR` Datentyp die Member. x,. y,. z,. und. w, was im Allgemeinen zu einer schlechten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-122">For XNAMATH 2.x, the `XMVECTOR` data type has .x, .y, .z, .and .w element members, which generally cause poor performance.</span></span> <span data-ttu-id="d0b4f-123">Die Verwendung des XM \_ Strict \_ VECTOR4-Typs bietet ein Opt-in der directxmath-Definition eines nicht transparenten Datentyps.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-123">The use of the XM\_STRICT\_VECTOR4 type provides an opt-in of the DirectXMath definition of an opaque data type.</span></span>

<span data-ttu-id="d0b4f-124">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="d0b4f-124">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="d0b4f-125">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="d0b4f-125">Platform Requirements</span></span>

<span data-ttu-id="d0b4f-126">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-126">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="d0b4f-127">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0b4f-127">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b4f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0b4f-128">Requirements</span></span>



| <span data-ttu-id="d0b4f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0b4f-129">Requirement</span></span> | <span data-ttu-id="d0b4f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d0b4f-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b4f-131">Header</span><span class="sxs-lookup"><span data-stu-id="d0b4f-131">Header</span></span><br/> | <dl> <span data-ttu-id="d0b4f-132"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b4f-132"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b4f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0b4f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b4f-134">Directxmath-Bibliothekstypen</span><span class="sxs-lookup"><span data-stu-id="d0b4f-134">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="d0b4f-135">**XMVECTORI32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d0b4f-135">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="d0b4f-136">**XMVECTORF32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d0b4f-136">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="d0b4f-137">**XMVECTORU32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d0b4f-137">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="d0b4f-138">**XMVECTORU8-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d0b4f-138">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="d0b4f-139">**Xmvector-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d0b4f-139">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 




