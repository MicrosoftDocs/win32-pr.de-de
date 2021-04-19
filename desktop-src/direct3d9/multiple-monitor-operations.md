---
description: 'Wenn ein Gerät erfolgreich zurückgesetzt wird (IDirect3DDevice9:: Reset) oder (IDirect3D9:: builatedevice) in voll Bild Vorgängen erstellt wurde, wird das Direct3D-Objekt, das das Gerät erstellt hat, als Besitzer aller Adapter auf diesem System markiert.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Multiple-Monitor Vorgänge (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345995"
---
# <a name="multiple-monitor-operations-direct3d-9"></a><span data-ttu-id="204d2-103">Multiple-Monitor Vorgänge (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204d2-103">Multiple-Monitor Operations (Direct3D 9)</span></span>

<span data-ttu-id="204d2-104">Wenn ein Gerät erfolgreich zurückgesetzt wird ([**IDirect3DDevice9:: Reset**](/windows/desktop/api)) oder ([**IDirect3D9:: builatedevice**](/windows/desktop/api)) in voll Bild Vorgängen erstellt wurde, wird das Direct3D-Objekt, das das Gerät erstellt hat, als Besitzer aller Adapter auf diesem System markiert.</span><span class="sxs-lookup"><span data-stu-id="204d2-104">When a device is successfully reset ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) or created ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in full-screen operations, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="204d2-105">Dieser Status wird als exklusiver Modus bezeichnet, und das Direct3D-Objekt besitzt den exklusiven Modus.</span><span class="sxs-lookup"><span data-stu-id="204d2-105">This state is known as exclusive mode, and the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="204d2-106">Der exklusive Modus bedeutet, dass Geräte, die von einem anderen Direct3D-Objekt erstellt wurden, keine voll Bild Vorgänge annehmen und keinen Videospeicher zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="204d2-106">Exclusive mode means that devices created by any other Direct3D object can neither assume full-screen operations nor allocate video memory.</span></span> <span data-ttu-id="204d2-107">Wenn ein Direct3D-Objekt den exklusiven Modus annimmt, werden darüber hinaus alle anderen Geräte als der Vollbildmodus in den Zustand "verloren" versetzt.</span><span class="sxs-lookup"><span data-stu-id="204d2-107">In addition, when a Direct3D object assumes exclusive mode, all devices other than the one that went full-screen are placed in lost state.</span></span> <span data-ttu-id="204d2-108">Weitere Informationen finden Sie unter [verlorene Geräte (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="204d2-108">For details, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="204d2-109">Zusammen mit dem exklusiven Modus wird das Direct3D-Objekt über das Fokus Fenster informiert, das vom Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="204d2-109">Along with exclusive mode, the Direct3D object is informed of the focus window that the device will use.</span></span> <span data-ttu-id="204d2-110">Der exklusive Modus wird freigegeben, wenn das endgültige voll Bild Gerät, das diesem Direct3D-Objekt gehört, entweder auf den Fenstermodus zurückgesetzt oder zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="204d2-110">Exclusive mode is released when the final full-screen device owned by that Direct3D object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="204d2-111">Geräte können in zwei Kategorien unterteilt werden, wenn ein Direct3D-Objekt im exklusiven Modus ist.</span><span class="sxs-lookup"><span data-stu-id="204d2-111">Devices can be divided into two categories when a Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="204d2-112">Die erste Kategorie von Geräten hat die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="204d2-112">The first category of devices have the following characteristics.</span></span>

-   <span data-ttu-id="204d2-113">Sie werden vom gleichen Direct3D-Objekt erstellt, das das voll Bild geschützte Gerät erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="204d2-113">They are created by the same Direct3D object that created the device that is full-screen.</span></span>
-   <span data-ttu-id="204d2-114">Sie haben dasselbe Fokus Fenster wie das Gerät, das voll Bildschirm ist.</span><span class="sxs-lookup"><span data-stu-id="204d2-114">They have the same focus window as the device that is full-screen.</span></span>
-   <span data-ttu-id="204d2-115">Sie stellen einen anderen Adapter von allen voll Bild Geräten dar.</span><span class="sxs-lookup"><span data-stu-id="204d2-115">They represent a different adapter from any full-screen device.</span></span>

<span data-ttu-id="204d2-116">Geräte in dieser Kategorie haben keine Einschränkungen hinsichtlich ihrer Fähigkeit, zurückgesetzt oder erstellt zu werden, und Sie werden nicht in den Zustand "verloren" versetzt.</span><span class="sxs-lookup"><span data-stu-id="204d2-116">Devices in this category have no restrictions concerning their ability to be reset or created, and they are not placed in lost state.</span></span> <span data-ttu-id="204d2-117">Geräte in dieser Kategorie können sogar in den Vollbildmodus versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="204d2-117">Devices in this category can even be put into full-screen mode.</span></span>

<span data-ttu-id="204d2-118">Geräte, die nicht in die erste Kategorie fallen: Geräte, die von einem anderen Direct3D-Objekt erstellt, mit einem anderen Fokus Fenster erstellt und für einen Adapter mit einem bereits voll Bild-Gerät erstellt wurden, können nicht zurückgesetzt werden und bleiben verloren, bis der exklusive Modus verloren geht.</span><span class="sxs-lookup"><span data-stu-id="204d2-118">Devices that do not fall in the first category - devices created by another Direct3D object, created with a different focus window, and created for an adapter with a device that is already full-screen - cannot be reset and remain in lost state until the exclusive mode is lost.</span></span> <span data-ttu-id="204d2-119">Demzufolge kann eine Anwendung mit mehreren Monitoren mehrere Geräte im Vollbildmodus platzieren, aber nur, wenn alle diese Geräte für verschiedene Adapter vorhanden sind, die vom gleichen Direct3D-Objekt erstellt wurden und dasselbe Fokus Fenster gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="204d2-119">As a result, a multiple-monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D object, and share the same focus window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="204d2-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="204d2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="204d2-121">Präsentieren einer Szene</span><span class="sxs-lookup"><span data-stu-id="204d2-121">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 



