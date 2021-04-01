---
description: Bitmap-Klassifizierungen
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Bitmap-Klassifizierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215220"
---
# <a name="bitmap-classifications"></a><span data-ttu-id="986a0-103">Bitmap-Klassifizierungen</span><span class="sxs-lookup"><span data-stu-id="986a0-103">Bitmap Classifications</span></span>

<span data-ttu-id="986a0-104">Es gibt zwei Klassen von Bitmaps:</span><span class="sxs-lookup"><span data-stu-id="986a0-104">There are two classes of bitmaps:</span></span>

-   <span data-ttu-id="986a0-105">[Geräteunabhängige Bitmaps](device-independent-bitmaps.md) (DIB).</span><span class="sxs-lookup"><span data-stu-id="986a0-105">[Device-independent bitmaps](device-independent-bitmaps.md) (DIB).</span></span> <span data-ttu-id="986a0-106">Das DIB-Dateiformat wurde entworfen, um sicherzustellen, dass mit einer Anwendung erstellte bitzugeordnete Grafiken geladen und in einer anderen Anwendung angezeigt werden können. dabei bleibt die Darstellung des Originals unverändert.</span><span class="sxs-lookup"><span data-stu-id="986a0-106">The DIB file format was designed to ensure that bitmapped graphics created using one application can be loaded and displayed in another application, retaining the same appearance as the original.</span></span>

-   <span data-ttu-id="986a0-107">[Geräte abhängige Bitmaps](device-dependent-bitmaps.md) (DDB), die auch als GDI-Bitmaps bezeichnet werden, waren die einzigen Bitmaps, die in früheren Versionen von 16-Bit-Versionen von Microsoft Windows (vor Version 3,0) verfügbar waren.</span><span class="sxs-lookup"><span data-stu-id="986a0-107">[Device-dependent bitmaps](device-dependent-bitmaps.md) (DDB), also known as GDI bitmaps, were the only bitmaps available in early versions of 16-bit Microsoft Windows (prior to version 3.0).</span></span> <span data-ttu-id="986a0-108">Wenn jedoch die Anzeige Technologie verbessert wurde und die Anzahl der verfügbaren Anzeigegeräte zunimmt, sind bestimmte inhärente Probleme aufgetreten, die nur mit Disb gelöst werden konnten.</span><span class="sxs-lookup"><span data-stu-id="986a0-108">However, as display technology improved and as the variety of available display devices increased, certain inherent problems surfaced which could only be solved using DIBs.</span></span> <span data-ttu-id="986a0-109">Es gab z. b. keine Methode zum Speichern (oder abrufen) der Auflösung des Anzeige Typs, für den eine Bitmap erstellt wurde, sodass eine Zeichnungsanwendung nicht schnell feststellen konnte, ob eine Bitmap für den Typ des Videoanzeige Geräts geeignet war, auf dem die Anwendung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="986a0-109">For example, there was no method of storing (or retrieving) the resolution of the display type on which a bitmap was created, so a drawing application could not quickly determine whether a bitmap was suitable for the type of video display device on which the application was running.</span></span>

    <span data-ttu-id="986a0-110">Trotz dieser Probleme sind DDSB (auch als kompatible Bitmaps bezeichnet) weiterhin für eine bessere GDI-Leistung und in anderen Situationen nützlich.</span><span class="sxs-lookup"><span data-stu-id="986a0-110">Despite these problems, DDBs (also known as compatible bitmaps) are still useful for better GDI performance and for other situations.</span></span>

 

 



