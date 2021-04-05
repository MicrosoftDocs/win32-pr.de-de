---
description: Das InkOverlay-Objekt kann an ein Fenster Steuerelement angefügt werden und wird verwendet, um grundlegende Freihand-Funktionen zu aktivieren.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Löschen mithilfe des InkOverlay-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751913"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a><span data-ttu-id="772f5-103">Löschen mithilfe des InkOverlay-Objekts</span><span class="sxs-lookup"><span data-stu-id="772f5-103">Erasing by Using the InkOverlay Object</span></span>

<span data-ttu-id="772f5-104">Das [**InkOverlay**](inkoverlay-class.md) -Objekt kann an ein Fenster Steuerelement angefügt werden und wird verwendet, um grundlegende Freihand-Funktionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="772f5-104">The [**InkOverlay**](inkoverlay-class.md) object can be attached to a window control and is used to enable basic ink capability.</span></span> <span data-ttu-id="772f5-105">Sie können das **InkOverlay** -Objekt verwenden, um frei Hand Eingaben zu löschen, indem Sie die [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) -Eigenschaft auf " **Delete**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="772f5-105">You can use the **InkOverlay** object to erase ink by setting the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) property equal to **Delete**.</span></span> <span data-ttu-id="772f5-106">Anschließend können Sie die Eigenschaft [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) entweder auf den **Strich** oder die **Punkt** Elemente von [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)festlegen.</span><span class="sxs-lookup"><span data-stu-id="772f5-106">You can then set the [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) property to either the **Stroke** or **Point** members of [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span></span> <span data-ttu-id="772f5-107">Wenn die **EraserMode** -Eigenschaft auf **Stroke** festgelegt wird, werden die gesamten Striche gelöscht.</span><span class="sxs-lookup"><span data-stu-id="772f5-107">Setting the **EraserMode** property to **Stroke** erases entire strokes.</span></span> <span data-ttu-id="772f5-108">Wenn die **EraserMode** -Eigenschaft auf " **Point** " festgelegt wird, wird die vom Cursor übergebenen Hand Eingaben gelöscht.</span><span class="sxs-lookup"><span data-stu-id="772f5-108">Setting the **EraserMode** property to **Point** erases the ink that the cursor passes over.</span></span>

 

 



