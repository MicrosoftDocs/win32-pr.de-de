---
description: Mit den Maus Cursor Methoden kann die Anwendung einen Farb Cursor angeben, indem eine Oberfläche bereitgestellt wird, die ein Bild enthält.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Arbeiten mit Maus Cursorn (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482414"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a><span data-ttu-id="c874f-103">Arbeiten mit Maus Cursorn (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c874f-103">Working with Mouse Cursors (Direct3D 9)</span></span>

<span data-ttu-id="c874f-104">Mit den Maus Cursor Methoden kann die Anwendung einen Farb Cursor angeben, indem eine Oberfläche bereitgestellt wird, die ein Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="c874f-104">The mouse cursor methods enable the application to specify a color cursor by providing a surface that contains an image.</span></span> <span data-ttu-id="c874f-105">Das System stellt sicher, dass dieser Cursor zur Hälfte der Anzeige Rate oder mehr aktualisiert wird, wenn die Frame Rate der Anwendung langsam ist.</span><span class="sxs-lookup"><span data-stu-id="c874f-105">The system will ensure that this cursor will be updated at half the display rate or more if the application's frame rate is slow.</span></span> <span data-ttu-id="c874f-106">Der Cursor wird jedoch nie häufiger aktualisiert als die Aktualisierungsrate der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="c874f-106">However, the cursor will never be updated more frequently than the display refresh rate.</span></span>

<span data-ttu-id="c874f-107">Die Position des Mauszeigers ist an den System Cursor gebunden und entsprechend der aktuellen räumlichen Auflösung des Anzeigemodus skaliert, kann aber explizit von der Anwendung verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c874f-107">The mouse cursor position is tied to the system cursor, appropriately scaled for the current display mode spatial resolution, but it can be moved explicitly by the application.</span></span> <span data-ttu-id="c874f-108">Dies entspricht dem Verhalten des mit der Win32-API unterstützten System Maus Cursors.</span><span class="sxs-lookup"><span data-stu-id="c874f-108">This is analogous to the behavior of the Win32 API - supported system mouse cursor.</span></span> <span data-ttu-id="c874f-109">Weitere Informationen zur Verwendung eines Mauszeigers in ihrer Direct3D-Anwendung finden Sie in den folgenden Referenz Themen.</span><span class="sxs-lookup"><span data-stu-id="c874f-109">For more information about how to use a mouse cursor in your Direct3D application, see the following reference topics.</span></span>

-   [<span data-ttu-id="c874f-110">**IDirect3DDevice9:: ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="c874f-110">**IDirect3DDevice9::ShowCursor**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [<span data-ttu-id="c874f-111">**IDirect3DDevice9:: setcurrsorposition**</span><span class="sxs-lookup"><span data-stu-id="c874f-111">**IDirect3DDevice9::SetCursorPosition**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [<span data-ttu-id="c874f-112">**IDirect3DDevice9:: setcurrsorproperties**</span><span class="sxs-lookup"><span data-stu-id="c874f-112">**IDirect3DDevice9::SetCursorProperties**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

<span data-ttu-id="c874f-113">Direct3D stellt sicher, dass die Maus entweder von Hardware Implementierungen oder von der Direct3D-Laufzeit unterstützt wird, die beim Aufrufen von IDirect3DDevice9 die hardwarebeschleunigte Blitvorgänge ausführt, wenn [**::P erneut gesendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)wird.</span><span class="sxs-lookup"><span data-stu-id="c874f-113">Direct3D ensures that the mouse is supported either by hardware implementations or by the Direct3D run time that performs hardware-accelerated blitting operations when calling [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c874f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c874f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c874f-115">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="c874f-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
