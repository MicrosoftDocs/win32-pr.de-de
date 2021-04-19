---
title: Pixel Formate
description: Pixel Formate
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL unter Windows, Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342087"
---
# <a name="pixel-formats"></a><span data-ttu-id="3416d-104">Pixel Formate</span><span class="sxs-lookup"><span data-stu-id="3416d-104">Pixel Formats</span></span>

<span data-ttu-id="3416d-105">Ein *Pixel Format* gibt mehrere Eigenschaften einer OpenGL-Zeichen Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="3416d-105">A *pixel format* specifies several properties of an OpenGL drawing surface.</span></span> <span data-ttu-id="3416d-106">Einige der Eigenschaften, die durch ein Pixel Format angegeben werden, sind:</span><span class="sxs-lookup"><span data-stu-id="3416d-106">Some of the properties specified by a pixel format are:</span></span>

-   <span data-ttu-id="3416d-107">Gibt an, ob der Pixel Puffer einzeln oder doppelt gepuffert ist.</span><span class="sxs-lookup"><span data-stu-id="3416d-107">Whether the pixel buffer is single- or double-buffered.</span></span>
-   <span data-ttu-id="3416d-108">Gibt an, ob sich die Pixeldaten im RGBA-oder Farb Index Formular befinden.</span><span class="sxs-lookup"><span data-stu-id="3416d-108">Whether the pixel data is in RGBA or color-index form.</span></span>
-   <span data-ttu-id="3416d-109">Die Anzahl der Bits, die zum Speichern von Farbdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3416d-109">The number of bits used to store color data.</span></span>
-   <span data-ttu-id="3416d-110">Die Anzahl der Bits, die für den tiefen Puffer (z-Achse) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3416d-110">The number of bits used for the depth (z-axis) buffer.</span></span>
-   <span data-ttu-id="3416d-111">Die Anzahl der Bits, die für den Schablonen Puffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3416d-111">The number of bits used for the stencil buffer.</span></span>
-   <span data-ttu-id="3416d-112">Die Anzahl der Ebenen für Überlagerung und Unterebene.</span><span class="sxs-lookup"><span data-stu-id="3416d-112">The number of overlay and underlay planes.</span></span>
-   <span data-ttu-id="3416d-113">Verschiedene Sichtbarkeits Masken.</span><span class="sxs-lookup"><span data-stu-id="3416d-113">Various visibility masks.</span></span>

<span data-ttu-id="3416d-114">Die Microsoft-Implementierung von OpenGL für Windows verwendet die Pixel [**formatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur, um Pixel Formatierungsdaten zu vermitteln.</span><span class="sxs-lookup"><span data-stu-id="3416d-114">Microsoft's implementation of OpenGL for Windows uses the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure to convey pixel format data.</span></span> <span data-ttu-id="3416d-115">Die Member der Struktur geben die vorangehenden Eigenschaften und mehrere andere an.</span><span class="sxs-lookup"><span data-stu-id="3416d-115">The structure's members specify the preceding properties and several others.</span></span>

<span data-ttu-id="3416d-116">Ein bestimmter Gerätekontext kann mehrere Pixel Formate unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3416d-116">A given device context can support several pixel formats.</span></span> <span data-ttu-id="3416d-117">Windows identifiziert die Pixel Formate, die ein Gerätekontext mit aufeinander folgenden einbasierten Indexwerten unterstützt (1, 2, 3, 4 usw.).</span><span class="sxs-lookup"><span data-stu-id="3416d-117">Windows identifies the pixel formats that a device context supports with consecutive one-based index values (1, 2, 3, 4, and so on).</span></span> <span data-ttu-id="3416d-118">Ein Gerätekontext kann nur ein Aktuelles Pixel Format aufweisen, das aus den von ihm unterstützten Pixel Formaten ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3416d-118">A device context can have just one current pixel format, chosen from the set of pixel formats it supports.</span></span>

<span data-ttu-id="3416d-119">Jedes Fenster verfügt über ein eigenes Aktuelles Pixel Format in OpenGL in Windows.</span><span class="sxs-lookup"><span data-stu-id="3416d-119">Each window has its own current pixel format in OpenGL in Windows.</span></span> <span data-ttu-id="3416d-120">Dies bedeutet beispielsweise, dass eine Anwendung RGBA-und Color-Index OpenGL-Fenster gleichzeitig anzeigen kann, oder ein Single-und Double-Buffered OpenGL-Fenster.</span><span class="sxs-lookup"><span data-stu-id="3416d-120">This means, for example, that an application can simultaneously display RGBA and color-index OpenGL windows, or single- and double-buffered OpenGL windows.</span></span> <span data-ttu-id="3416d-121">Diese Funktion für die Pixel Formate pro Fenster ist auf OpenGL-Fenster beschränkt.</span><span class="sxs-lookup"><span data-stu-id="3416d-121">This per-window pixel format capability is limited to OpenGL windows.</span></span>

<span data-ttu-id="3416d-122">Normalerweise erhalten Sie einen Gerätekontext, legen das Pixel Format des Geräte Kontexts fest und erstellen dann einen OpenGL-renderingkontext, der für dieses Gerät geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3416d-122">Typically, you obtain a device context, set the device context's pixel format, and then create an OpenGL rendering context suitable for that device.</span></span>

> [!Note]  
> <span data-ttu-id="3416d-123">Sie legen das Pixel Format vor dem Erstellen eines renderingkontexts fest, da der renderingkontext das Pixel Format des Geräte Kontexts erbt.</span><span class="sxs-lookup"><span data-stu-id="3416d-123">You set the pixel format before creating a rendering context because the rendering context inherits the device context's pixel format.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3416d-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3416d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3416d-125">Pixel Format Funktionen</span><span class="sxs-lookup"><span data-stu-id="3416d-125">Pixel Format Functions</span></span>](pixel-format-functions.md)
</dt> </dl>

 

 




