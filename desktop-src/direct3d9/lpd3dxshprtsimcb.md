---
description: Rückruffunktion für die PrT-Simulation und -Komprimierung (Precomputed Radiance Transfer).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a7c4911bf2a7b7fa2aa83422a206644f6eb747
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342805"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="4cdfc-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="4cdfc-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="4cdfc-104">Rückruffunktion für die PrT-Simulation und -Komprimierung (Precomputed Radiance Transfer).</span><span class="sxs-lookup"><span data-stu-id="4cdfc-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cdfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cdfc-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="4cdfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cdfc-106">Parameters</span></span>

<span data-ttu-id="4cdfc-107">fPercentDone: Gleitkommazahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen (zwischen 0 und 100 Prozent) darstellt.</span><span class="sxs-lookup"><span data-stu-id="4cdfc-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="4cdfc-108">lpUserContext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird; Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="4cdfc-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="4cdfc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cdfc-109">Return Value</span></span>

<span data-ttu-id="4cdfc-110">Diese Funktion muss implementiert werden, um S \_ OK zurück zu geben, um den Simulator weiter ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="4cdfc-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="4cdfc-111">Jeder andere Wert hält den Simulator an.</span><span class="sxs-lookup"><span data-stu-id="4cdfc-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cdfc-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4cdfc-112">Remarks</span></span>

<span data-ttu-id="4cdfc-113">Achten Sie darauf, die [**Aufrufkonvention für Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben, wenn Sie die Rückruffunktion deklarieren.</span><span class="sxs-lookup"><span data-stu-id="4cdfc-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="4cdfc-114">Andernfalls können Stapelüberläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="4cdfc-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="4cdfc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cdfc-115">Requirement</span></span>                         | <span data-ttu-id="4cdfc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4cdfc-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="4cdfc-117">Header</span><span class="sxs-lookup"><span data-stu-id="4cdfc-117">Header</span></span>                   | <span data-ttu-id="4cdfc-118">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="4cdfc-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="4cdfc-119">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="4cdfc-119">Import Library</span></span>           | <span data-ttu-id="4cdfc-120">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="4cdfc-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="4cdfc-121">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="4cdfc-121">Minimum Operating System</span></span> | <span data-ttu-id="4cdfc-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4cdfc-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="4cdfc-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4cdfc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cdfc-124">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="4cdfc-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
