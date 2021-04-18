---
description: In der folgenden Tabelle sind Rückgabecodes von API-Funktionen enthalten.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Direct3D 10-Rückgabe Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340116"
---
# <a name="direct3d-10-return-codes"></a><span data-ttu-id="66645-103">Direct3D 10-Rückgabe Codes</span><span class="sxs-lookup"><span data-stu-id="66645-103">Direct3D 10 Return Codes</span></span>

<span data-ttu-id="66645-104">In der folgenden Tabelle sind Rückgabecodes von API-Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="66645-104">The following table contains return codes from API functions.</span></span>



| <span data-ttu-id="66645-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="66645-105">HRESULT</span></span>                                         | <span data-ttu-id="66645-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66645-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66645-107">D3d10- \_ Fehler \_ Datei \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="66645-107">D3D10\_ERROR\_FILE\_NOT\_FOUND</span></span>                  | <span data-ttu-id="66645-108">Die Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="66645-108">The file was not found.</span></span>                                                                                                                               |
| <span data-ttu-id="66645-109">D3d10 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte</span><span class="sxs-lookup"><span data-stu-id="66645-109">D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS</span></span> | <span data-ttu-id="66645-110">Es sind zu viele eindeutige Instanzen eines bestimmten [Zustands Objekt](d3d10-graphics-programming-guide-api-features-state-objects.md)Typs vorhanden.</span><span class="sxs-lookup"><span data-stu-id="66645-110">There are too many unique instances of a particular type of [state object](d3d10-graphics-programming-guide-api-features-state-objects.md).</span></span>          |
| <span data-ttu-id="66645-111">D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="66645-111">D3DERR\_INVALIDCALL</span></span>                             | <span data-ttu-id="66645-112">Der Methoden Aufrufwert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="66645-112">The method call is invalid.</span></span> <span data-ttu-id="66645-113">Beispielsweise ist der-Parameter einer Methode möglicherweise kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="66645-113">For example, a method's parameter may not be a valid pointer.</span></span>                                                             |
| <span data-ttu-id="66645-114">D3DERR \_ wasstilldrawing</span><span class="sxs-lookup"><span data-stu-id="66645-114">D3DERR\_WASSTILLDRAWING</span></span>                         | <span data-ttu-id="66645-115">Der vorherige Blit-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig.</span><span class="sxs-lookup"><span data-stu-id="66645-115">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                                                   |
| <span data-ttu-id="66645-116">E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="66645-116">E\_FAIL</span></span>                                         | <span data-ttu-id="66645-117">Es wurde versucht, ein Gerät mit aktivierter [debugschicht](d3d10-graphics-programming-guide-api-features-layers.md) zu erstellen, und die Ebene ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="66645-117">Attempted to create a device with the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="66645-118">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="66645-118">E\_INVALIDARG</span></span>                                   | <span data-ttu-id="66645-119">An die Rückgabe Funktion wurde ein ungültiger Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="66645-119">An invalid parameter was passed to the returning function.</span></span>                                                                                            |
| <span data-ttu-id="66645-120">E \_ outo-Memory</span><span class="sxs-lookup"><span data-stu-id="66645-120">E\_OUTOFMEMORY</span></span>                                  | <span data-ttu-id="66645-121">Direct3D konnte nicht genügend Arbeitsspeicher zuordnen, um den-Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="66645-121">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                                                   |
| <span data-ttu-id="66645-122">E \_ notimpl</span><span class="sxs-lookup"><span data-stu-id="66645-122">E\_NOTIMPL</span></span>                                      | <span data-ttu-id="66645-123">Der Methodenaufrufe wird nicht mit der übergebenen Parameter Kombination implementiert.</span><span class="sxs-lookup"><span data-stu-id="66645-123">The method call isn't implemented with the passed parameter combination.</span></span>                                                                              |
| <span data-ttu-id="66645-124">S \_ false</span><span class="sxs-lookup"><span data-stu-id="66645-124">S\_FALSE</span></span>                                        | <span data-ttu-id="66645-125">Alternativer Erfolgs Wert, der einen erfolgreichen, aber nicht dem Standard entsprechende Abschluss angibt (die genaue Bedeutung hängt vom Kontext ab).</span><span class="sxs-lookup"><span data-stu-id="66645-125">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span>                                 |
| <span data-ttu-id="66645-126">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="66645-126">S\_OK</span></span>                                           | <span data-ttu-id="66645-127">Kein Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="66645-127">No error occurred.</span></span>                                                                                                                                    |



 

<span data-ttu-id="66645-128">Um Code zu schreiben, der die [HRESULT-Werte](../winprog/windows-data-types.md) robuster verarbeitet, verwenden Sie die Makros erfolgreich (HR) und failed (HR).</span><span class="sxs-lookup"><span data-stu-id="66645-128">To write code that handles [HRESULT values](../winprog/windows-data-types.md) robustly, use the SUCCEEDED(hr) and FAILED(hr) macros.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66645-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66645-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66645-130">Direct3D-Referenz</span><span class="sxs-lookup"><span data-stu-id="66645-130">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[<span data-ttu-id="66645-131">Referenz für Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="66645-131">Reference for Direct3D 10</span></span>](d3d10-graphics-reference.md)
</dt> </dl>

 

 
