---
description: Rückruffunktion für die PRT-Simulation und-Komprimierung.
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482086"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="0fd23-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="0fd23-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="0fd23-104">Rückruffunktion für die PRT-Simulation und-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="0fd23-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd23-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="0fd23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fd23-106">Parameters</span></span>

<span data-ttu-id="0fd23-107">"vollständig": Gleit Komma Zahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen darstellt (zwischen 0 und 100 Prozent).</span><span class="sxs-lookup"><span data-stu-id="0fd23-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="0fd23-108">lpusercontext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion weitergeleitet wird. wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0fd23-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fd23-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fd23-109">Return Value</span></span>

<span data-ttu-id="0fd23-110">Diese Funktion muss implementiert werden, damit S OK zurückgegeben wird \_ , um den Simulator weiterhin ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="0fd23-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="0fd23-111">Jeder andere Wert hält den Simulator an.</span><span class="sxs-lookup"><span data-stu-id="0fd23-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd23-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fd23-112">Remarks</span></span>

<span data-ttu-id="0fd23-113">Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufruf Konvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0fd23-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="0fd23-114">Andernfalls können Stapel Überläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="0fd23-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="0fd23-115">Header</span><span class="sxs-lookup"><span data-stu-id="0fd23-115">Header</span></span>                   | <span data-ttu-id="0fd23-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="0fd23-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="0fd23-117">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="0fd23-117">Import Library</span></span>           | <span data-ttu-id="0fd23-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="0fd23-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="0fd23-119">Mindestens Betriebs System</span><span class="sxs-lookup"><span data-stu-id="0fd23-119">Minimum Operating System</span></span> | <span data-ttu-id="0fd23-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0fd23-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="0fd23-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0fd23-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd23-122">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="0fd23-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
