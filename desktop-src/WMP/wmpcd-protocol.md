---
title: Wmpcd-Protokoll
description: Wmpcd-Protokoll
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows-Media Player, Protokolle
- Windows Media Player-Objektmodell, Protokolle
- Objektmodell, Protokolle
- Windows Media Player ActiveX-Steuerelement, Protokolle für das Objektmodell
- ActiveX-Steuerelement, Protokolle für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Protokolle für das Objektmodell
- Windows Media Player Mobile, Protokolle für das Objektmodell
- Protokolle, Windows Media Player-Objektmodell
- Protokolle, wmpcd
- Wmpcd-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206708"
---
# <a name="wmpcd-protocol"></a><span data-ttu-id="dd56c-113">Wmpcd-Protokoll</span><span class="sxs-lookup"><span data-stu-id="dd56c-113">WMPCD Protocol</span></span>

<span data-ttu-id="dd56c-114">Mit dem wmpcd-Protokoll können Sie mithilfe der URL-Syntax Spuren auf einer Compact Disk angeben.</span><span class="sxs-lookup"><span data-stu-id="dd56c-114">The WMPCD protocol enables you to specify tracks on a compact disc using URL syntax.</span></span> <span data-ttu-id="dd56c-115">Dies ist die allgemeine Syntax des Protokolls:</span><span class="sxs-lookup"><span data-stu-id="dd56c-115">This is the general syntax of the protocol:</span></span>


```C++
wmpcd://drive/track
```



<span data-ttu-id="dd56c-116">Das *Laufwerk* Segment ist der Index des CD-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd56c-116">The *drive* segment is the index of the CD drive.</span></span> <span data-ttu-id="dd56c-117">Das *Track* -Segment ist die Nummer des Titels. Im folgenden Beispiel wird die Verwendung des wmpcd-Protokolls veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="dd56c-117">The *track* segment is the number of the track. The following example demonstrates using the WMPCD protocol.</span></span>


```C++
player.url = "wmpcd://0/4";
```



<span data-ttu-id="dd56c-118">Im Beispiel wird der vierte Titel auf der Festplatte auf dem ersten CD-Laufwerk (dem Laufwerk mit dem Index 0) wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="dd56c-118">The example plays the fourth track on the disc in the first CD drive (the drive whose index is 0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd56c-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd56c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd56c-120">**Unterstützte Protokolle und Dateitypen**</span><span class="sxs-lookup"><span data-stu-id="dd56c-120">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




