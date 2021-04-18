---
description: Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Gleit Komma Werten in eine Instanz des xmvector-Typs unterstützt.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: XMVECTORF32-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365484"
---
# <a name="xmvectorf32-data-type"></a><span data-ttu-id="65e73-103">XMVECTORF32-Datentyp</span><span class="sxs-lookup"><span data-stu-id="65e73-103">XMVECTORF32 Data Type</span></span>

<span data-ttu-id="65e73-104">Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Gleit Komma Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="65e73-104">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a><span data-ttu-id="65e73-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65e73-105">Remarks</span></span>

<span data-ttu-id="65e73-106">Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die `XMVECTORF32` beim Programmieren in C++ verfügbar sind, finden Sie unter [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="65e73-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORF32` when programming in C++, see [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span></span>

<span data-ttu-id="65e73-107">Die **XMVECTORF32**-, [**XMVECTORU32**](xmvectoru32-data-type.md)-, [**XMVECTORI32**](xmvectori32-data-type.md)-und [**XMVECTORU8**](xmvectoru8-data-type.md) -Strukturen werden als Mechanismus zur Erstellung von [**xmvector**](xmvector-data-type.md) aus unterschiedlichen Konstanten Datentypen (Gleit Komma Zahl, Ganzzahl ohne Vorzeichen, Ganzzahl und Byte) mithilfe von Initialisierern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="65e73-107">The **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="65e73-108">Dies ist für die Unterstützung von [**xmvector**](xmvector-data-type.md)erforderlich, da Initialisierer aus Gründen der Portabilität und Optimierung nicht selbst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="65e73-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="65e73-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="65e73-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



<span data-ttu-id="65e73-110">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="65e73-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="65e73-111">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="65e73-111">Platform Requirements</span></span>

<span data-ttu-id="65e73-112">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="65e73-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="65e73-113">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="65e73-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e73-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65e73-114">Requirements</span></span>



| <span data-ttu-id="65e73-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65e73-115">Requirement</span></span> | <span data-ttu-id="65e73-116">Wert</span><span class="sxs-lookup"><span data-stu-id="65e73-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e73-117">Header</span><span class="sxs-lookup"><span data-stu-id="65e73-117">Header</span></span><br/> | <dl> <span data-ttu-id="65e73-118"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="65e73-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e73-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65e73-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e73-120">Directxmath-Bibliothekstypen</span><span class="sxs-lookup"><span data-stu-id="65e73-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="65e73-121">**XMVECTORI32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65e73-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="65e73-122">**Xmvector-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65e73-122">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="65e73-123">**XMVECTORU32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65e73-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="65e73-124">**XMVECTORU8-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65e73-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="65e73-125">**XMVECTORF32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65e73-125">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> </dl>

 

 




