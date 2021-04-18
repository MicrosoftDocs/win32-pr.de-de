---
description: Rückruffunktion für uvatlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344172"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="83004-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="83004-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="83004-104">Rückruffunktion für uvatlas.</span><span class="sxs-lookup"><span data-stu-id="83004-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="83004-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83004-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="83004-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83004-106">Parameters</span></span>

<span data-ttu-id="83004-107">\[Out \] -vollständig: Gleit Komma Zahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen darstellt (zwischen 0 und 100 Prozent).</span><span class="sxs-lookup"><span data-stu-id="83004-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="83004-108">\[in \] lpusercontext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird. wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="83004-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="83004-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83004-109">Return Value</span></span>

<span data-ttu-id="83004-110">Diese Funktion muss implementiert werden, damit S OK zurückgegeben wird \_ , um den Simulator weiterhin ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="83004-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="83004-111">Jeder andere Wert hält den Simulator an.</span><span class="sxs-lookup"><span data-stu-id="83004-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="83004-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83004-112">Remarks</span></span>

<span data-ttu-id="83004-113">Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufruf Konvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="83004-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="83004-114">Andernfalls können Stapel Überläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="83004-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="83004-115">Header</span><span class="sxs-lookup"><span data-stu-id="83004-115">Header</span></span>                   | <span data-ttu-id="83004-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="83004-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="83004-117">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="83004-117">Import Library</span></span>           | <span data-ttu-id="83004-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="83004-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="83004-119">Mindestens Betriebs System</span><span class="sxs-lookup"><span data-stu-id="83004-119">Minimum Operating System</span></span> | <span data-ttu-id="83004-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="83004-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="83004-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83004-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83004-122">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="83004-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
