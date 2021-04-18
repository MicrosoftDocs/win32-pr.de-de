---
description: In diesem Abschnitt wird ein Problem aufgeführt, das bei der Arbeit mit Geräte Fenstern in Direct3D-Anwendungen auftreten kann.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Arbeiten mit Geräte Fenstern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343933"
---
# <a name="working-with-device-windows-direct3d-9"></a><span data-ttu-id="8f12b-103">Arbeiten mit Geräte Fenstern (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8f12b-103">Working with Device Windows (Direct3D 9)</span></span>

<span data-ttu-id="8f12b-104">In diesem Abschnitt wird ein Problem aufgeführt, das bei der Arbeit mit Geräte Fenstern in Direct3D-Anwendungen auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="8f12b-104">This section lists an issue that you might encounter when working with device windows in Direct3D applications.</span></span>

-   <span data-ttu-id="8f12b-105">Direct3D verknüpft nur die Fokus Fenster anstelle des Geräte Fensters mit der Direct3D-Nachrichten Verarbeitungs Funktion und verarbeitet nur die Fokus Fenster Meldungen.</span><span class="sxs-lookup"><span data-stu-id="8f12b-105">Direct3D only hooks up the focus windows instead of the device window with the Direct3D message processing function, and only processes the focus window messages.</span></span> <span data-ttu-id="8f12b-106">Daher sollte das Fokus Fenster das übergeordnete Element jedes Geräte Fensters sein.</span><span class="sxs-lookup"><span data-stu-id="8f12b-106">So, the focus window should be the parent of any device window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f12b-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f12b-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f12b-108">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="8f12b-108">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



