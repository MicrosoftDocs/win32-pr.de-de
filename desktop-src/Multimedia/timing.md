---
title: Zeitliche Steuerung (Windows Multimedia)
description: Zeitliche Steuerung
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- Drawdib, zeitliche Steuerung
- Drawdibtime-Funktion
- Drawdib, Debuggen
- Debuggen von drawdib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474862"
---
# <a name="timing-windows-multimedia"></a><span data-ttu-id="700b5-107">Zeitliche Steuerung (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="700b5-107">Timing (Windows Multimedia)</span></span>

<span data-ttu-id="700b5-108">Beim Debuggen einer Anwendung können Sie Informationen über die Zeit abrufen, die zum Durchführen von wiederkehrenden drawdib-Vorgängen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="700b5-108">As part of debugging an application, you can obtain information about the amount of time required to complete repetitive DrawDib operations.</span></span> <span data-ttu-id="700b5-109">Die [**drawdibtime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) -Funktion gibt Zeit Steuerungsinformationen für die folgenden Vorgänge zurück:</span><span class="sxs-lookup"><span data-stu-id="700b5-109">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function returns timing information for the following operations:</span></span>

-   <span data-ttu-id="700b5-110">Zeichnen einer Bitmap</span><span class="sxs-lookup"><span data-stu-id="700b5-110">Drawing a bitmap</span></span>
-   <span data-ttu-id="700b5-111">Das Komprimieren einer Bitmap wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="700b5-111">Decompressing a bitmap</span></span>
-   <span data-ttu-id="700b5-112">Dithering einer Bitmap</span><span class="sxs-lookup"><span data-stu-id="700b5-112">Dithering a bitmap</span></span>
-   <span data-ttu-id="700b5-113">Strecken einer Bitmap</span><span class="sxs-lookup"><span data-stu-id="700b5-113">Stretching a bitmap</span></span>
-   <span data-ttu-id="700b5-114">Übertragen einer Bitmap mithilfe der [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion</span><span class="sxs-lookup"><span data-stu-id="700b5-114">Transferring a bitmap by using the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function</span></span>
-   <span data-ttu-id="700b5-115">Übertragen einer Bitmap mithilfe der [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) -Funktion</span><span class="sxs-lookup"><span data-stu-id="700b5-115">Transferring a bitmap by using the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function</span></span>

<span data-ttu-id="700b5-116">Nach dem Abrufen eines Satzes von Werten setzt [**drawdibtime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) die Anzahl und den Wert für jeden Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="700b5-116">After retrieving a set of values, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) resets the count and value for each operation.</span></span>

<span data-ttu-id="700b5-117">Die [**drawdibtime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) -Funktion ist nur in der Debugversion der drawdib-Funktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="700b5-117">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function is available only in the debug version of the DrawDib functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="700b5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="700b5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="700b5-119">Bild Rendering</span><span class="sxs-lookup"><span data-stu-id="700b5-119">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
