---
description: Rückruffunktion für UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342795"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="7dca6-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="7dca6-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="7dca6-104">Rückruffunktion für UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="7dca6-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dca6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dca6-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="7dca6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dca6-106">Parameters</span></span>

<span data-ttu-id="7dca6-107">\[out \] fPercentDone: Gleitkommazahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen darstellt (zwischen 0 und 100 Prozent).</span><span class="sxs-lookup"><span data-stu-id="7dca6-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="7dca6-108">\[in \] lpUserContext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7dca6-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="7dca6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dca6-109">Return Value</span></span>

<span data-ttu-id="7dca6-110">Diese Funktion muss implementiert werden, um S \_ OK zurückzugeben, um den Simulator weiter auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7dca6-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="7dca6-111">Jeder andere Wert hält den Simulator an.</span><span class="sxs-lookup"><span data-stu-id="7dca6-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dca6-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7dca6-112">Remarks</span></span>

<span data-ttu-id="7dca6-113">Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufrufkonvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7dca6-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="7dca6-114">Andernfalls können Stapelüberläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="7dca6-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="7dca6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7dca6-115">Requirement</span></span>                         | <span data-ttu-id="7dca6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7dca6-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="7dca6-117">Header</span><span class="sxs-lookup"><span data-stu-id="7dca6-117">Header</span></span>                   | <span data-ttu-id="7dca6-118">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="7dca6-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="7dca6-119">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="7dca6-119">Import Library</span></span>           | <span data-ttu-id="7dca6-120">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="7dca6-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="7dca6-121">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dca6-121">Minimum Operating System</span></span> | <span data-ttu-id="7dca6-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7dca6-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="7dca6-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7dca6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dca6-124">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="7dca6-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
