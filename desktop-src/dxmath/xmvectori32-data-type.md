---
description: Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von ganzzahligen Werten in eine Instanz des xmvector-Typs unterstützt.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: XMVECTORI32-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371783"
---
# <a name="xmvectori32-data-type"></a><span data-ttu-id="4f07b-103">XMVECTORI32-Datentyp</span><span class="sxs-lookup"><span data-stu-id="4f07b-103">XMVECTORI32 Data Type</span></span>

<span data-ttu-id="4f07b-104">Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von ganzzahligen Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f07b-104">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a><span data-ttu-id="4f07b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f07b-105">Remarks</span></span>

<span data-ttu-id="4f07b-106">Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die `XMVECTORI32` beim Programmieren in C++ verfügbar sind, finden Sie unter [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4f07b-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORI32` when programming in C++, see [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span></span>

<span data-ttu-id="4f07b-107">Die [**XMVECTORF32**](xmvectorf32-data-type.md)-, [**XMVECTORU32**](xmvectoru32-data-type.md)-, **XMVECTORI32**-und [**XMVECTORU8**](xmvectoru8-data-type.md) -Strukturen werden als Mechanismus zur Erstellung von [**xmvector**](xmvector-data-type.md) aus unterschiedlichen Konstanten Datentypen (Gleit Komma Zahl, Ganzzahl ohne Vorzeichen, Ganzzahl und Byte) mithilfe von Initialisierern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4f07b-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32**, and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="4f07b-108">Dies ist für die Unterstützung von [**xmvector**](xmvector-data-type.md)erforderlich, da Initialisierer aus Gründen der Portabilität und Optimierung nicht selbst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4f07b-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="4f07b-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4f07b-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



<span data-ttu-id="4f07b-110">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="4f07b-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="4f07b-111">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="4f07b-111">Platform Requirements</span></span>

<span data-ttu-id="4f07b-112">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4f07b-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="4f07b-113">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f07b-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f07b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f07b-114">Requirements</span></span>



| <span data-ttu-id="4f07b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f07b-115">Requirement</span></span> | <span data-ttu-id="4f07b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4f07b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f07b-117">Header</span><span class="sxs-lookup"><span data-stu-id="4f07b-117">Header</span></span><br/> | <dl> <span data-ttu-id="4f07b-118"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f07b-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f07b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f07b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f07b-120">Directxmath-Bibliothekstypen</span><span class="sxs-lookup"><span data-stu-id="4f07b-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="4f07b-121">**Xmvector-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4f07b-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="4f07b-122">**XMVECTORF32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4f07b-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4f07b-123">**XMVECTORU32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4f07b-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4f07b-124">**XMVECTORU8-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4f07b-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="4f07b-125">**XMVECTORI32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4f07b-125">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> </dl>

 

 




