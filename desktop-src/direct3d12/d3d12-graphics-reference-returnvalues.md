---
title: Direct3D 12-Rückgabecodes
description: Im folgenden finden Sie Rückgabecodes von API-Funktionen.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337458"
---
# <a name="direct3d-12-return-codes"></a><span data-ttu-id="7bb59-103">Direct3D 12-Rückgabecodes</span><span class="sxs-lookup"><span data-stu-id="7bb59-103">Direct3D 12 Return Codes</span></span>

<span data-ttu-id="7bb59-104">Im folgenden finden Sie Rückgabecodes von API-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7bb59-104">The following are return codes from API functions.</span></span> <span data-ttu-id="7bb59-105">Weitere Rückgabecodes finden Sie unter [DXGI \_ Error](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="7bb59-105">For more return codes, see [DXGI\_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>



| <span data-ttu-id="7bb59-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7bb59-106">HRESULT</span></span>                                                                  | <span data-ttu-id="7bb59-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bb59-107">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb59-108">D3D12- \_ Fehler \_ Adapter wurde \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="7bb59-108">D3D12\_ERROR\_ADAPTER\_NOT\_FOUND</span></span>                                        | <span data-ttu-id="7bb59-109">Das angegebene zwischengespeicherte PSO wurde auf einem anderen Adapter erstellt und kann auf dem aktuellen Adapter nicht wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bb59-109">The specified cached PSO was created on a different adapter and cannot be reused on the current adapter.</span></span>          |
| <span data-ttu-id="7bb59-110">D3D12- \_ Fehler \_ Treiber \_ Version stimmen nicht \_ überein.</span><span class="sxs-lookup"><span data-stu-id="7bb59-110">D3D12\_ERROR\_DRIVER\_VERSION\_MISMATCH</span></span>                                  | <span data-ttu-id="7bb59-111">Das angegebene zwischengespeicherte PSO wurde auf einer anderen Treiber Version erstellt und kann nicht auf dem aktuellen Adapter wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bb59-111">The specified cached PSO was created on a different driver version and cannot be reused on the current adapter.</span></span>  |
| <span data-ttu-id="7bb59-112">D3DERR \_ invalidcall(durch DXGI- \_ Fehler \_ ungültigen-Befehl ersetzt \_ )</span><span class="sxs-lookup"><span data-stu-id="7bb59-112">D3DERR\_INVALIDCALL (replaced with DXGI\_ERROR\_INVALID\_CALL)</span></span>           | <span data-ttu-id="7bb59-113">Der Methoden Aufrufwert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7bb59-113">The method call is invalid.</span></span> <span data-ttu-id="7bb59-114">Beispielsweise ist der-Parameter einer Methode möglicherweise kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="7bb59-114">For example, a method's parameter may not be a valid pointer.</span></span>                             |
| <span data-ttu-id="7bb59-115">D3DERR \_ wasstilldrawing (durch DXGI- \_ Fehler \_ ersetzt \_ ) wurde noch \_ gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7bb59-115">D3DERR\_WASSTILLDRAWING (replaced with DXGI\_ERROR\_WAS\_STILL\_DRAWING)</span></span> | <span data-ttu-id="7bb59-116">Der vorherige Blit-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig.</span><span class="sxs-lookup"><span data-stu-id="7bb59-116">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                   |
| <span data-ttu-id="7bb59-117">E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="7bb59-117">E\_FAIL</span></span>                                                                  | <span data-ttu-id="7bb59-118">Es wurde versucht, ein Gerät mit aktivierter debugschicht zu erstellen, und die Ebene ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="7bb59-118">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span>                             |
| <span data-ttu-id="7bb59-119">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="7bb59-119">E\_INVALIDARG</span></span>                                                            | <span data-ttu-id="7bb59-120">An die Rückgabe Funktion wurde ein ungültiger Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="7bb59-120">An invalid parameter was passed to the returning function.</span></span>                                                             |
| <span data-ttu-id="7bb59-121">E \_ outo-Memory</span><span class="sxs-lookup"><span data-stu-id="7bb59-121">E\_OUTOFMEMORY</span></span>                                                           | <span data-ttu-id="7bb59-122">Direct3D konnte nicht genügend Arbeitsspeicher zuordnen, um den-Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7bb59-122">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                   |
| <span data-ttu-id="7bb59-123">E \_ notimpl</span><span class="sxs-lookup"><span data-stu-id="7bb59-123">E\_NOTIMPL</span></span>                                                               | <span data-ttu-id="7bb59-124">Der Methodenaufrufe wird nicht mit der übergebenen Parameter Kombination implementiert.</span><span class="sxs-lookup"><span data-stu-id="7bb59-124">The method call isn't implemented with the passed parameter combination.</span></span>                                               |
| <span data-ttu-id="7bb59-125">S \_ false</span><span class="sxs-lookup"><span data-stu-id="7bb59-125">S\_FALSE</span></span>                                                                 | <span data-ttu-id="7bb59-126">Alternativer Erfolgs Wert, der einen erfolgreichen, aber nicht dem Standard entsprechende Abschluss angibt (die genaue Bedeutung hängt vom Kontext ab).</span><span class="sxs-lookup"><span data-stu-id="7bb59-126">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="7bb59-127">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="7bb59-127">S\_OK</span></span>                                                                    | <span data-ttu-id="7bb59-128">Kein Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7bb59-128">No error occurred.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="7bb59-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bb59-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb59-130">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7bb59-130">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 