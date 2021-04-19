---
description: Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Uint8 \_ t-Werten in eine Instanz des xmvector-Typs unterstützt.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: XMVECTORU8-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355265"
---
# <a name="xmvectoru8-data-type"></a><span data-ttu-id="599d3-103">XMVECTORU8-Datentyp</span><span class="sxs-lookup"><span data-stu-id="599d3-103">XMVECTORU8 Data Type</span></span>

<span data-ttu-id="599d3-104">Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Uint8 \_ t-Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="599d3-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a><span data-ttu-id="599d3-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="599d3-105">Remarks</span></span>

<span data-ttu-id="599d3-106">Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die mit XMVECTORU8 bei der Programmierung in C++ verfügbar sind, finden Sie unter [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="599d3-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU8 when programming in C++, see [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).</span></span>

<span data-ttu-id="599d3-107">Die [**XMVECTORF32**](xmvectorf32-data-type.md)-, [**XMVECTORU32**](xmvectoru32-data-type.md)-, [**XMVECTORI32**](xmvectori32-data-type.md)-und **XMVECTORU8** -Strukturen werden als Mechanismus zur Erstellung von [**xmvector**](xmvector-data-type.md) aus unterschiedlichen Konstanten Datentypen (Gleit Komma Zahl, Ganzzahl ohne Vorzeichen, Ganzzahl und Byte) mithilfe von Initialisierern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="599d3-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and **XMVECTORU8** structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="599d3-108">Dies ist für die Unterstützung von [**xmvector**](xmvector-data-type.md)erforderlich, da Initialisierer aus Gründen der Portabilität und Optimierung nicht selbst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="599d3-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="599d3-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="599d3-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

<span data-ttu-id="599d3-110">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="599d3-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="599d3-111">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="599d3-111">Platform Requirements</span></span>

<span data-ttu-id="599d3-112">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="599d3-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="599d3-113">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="599d3-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="599d3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="599d3-114">Requirements</span></span>



| <span data-ttu-id="599d3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="599d3-115">Requirement</span></span> | <span data-ttu-id="599d3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="599d3-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="599d3-117">Header</span><span class="sxs-lookup"><span data-stu-id="599d3-117">Header</span></span><br/> | <dl> <span data-ttu-id="599d3-118"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="599d3-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="599d3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="599d3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599d3-120">Directxmath-Bibliothekstypen</span><span class="sxs-lookup"><span data-stu-id="599d3-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="599d3-121">**Xmvector-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="599d3-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="599d3-122">**XMVECTORF32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="599d3-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="599d3-123">**XMVECTORI32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="599d3-123">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="599d3-124">**XMVECTORU32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="599d3-124">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="599d3-125">XMVECTORU8-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="599d3-125">XMVECTORU8 Extensions</span></span>](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




