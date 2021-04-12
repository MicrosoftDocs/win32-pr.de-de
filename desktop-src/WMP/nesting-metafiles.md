---
title: Schachteln von Metadateien
description: Schachteln von Metadateien
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Media-Metadateien, Schachteln
- Windows Media-Metadateien, verweisen auf andere Metadateien
- Schachteln von Metadateien
- Metadatendateien, Schachteln
- Metadatendateien, verweisen auf andere Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309328"
---
# <a name="nesting-metafiles"></a><span data-ttu-id="7679f-108">Schachteln von Metadateien</span><span class="sxs-lookup"><span data-stu-id="7679f-108">Nesting Metafiles</span></span>

<span data-ttu-id="7679f-109">Eine Metadatei kann auf eine andere Metadatendatei verweisen.</span><span class="sxs-lookup"><span data-stu-id="7679f-109">A metafile can reference another metafile.</span></span> <span data-ttu-id="7679f-110">Verwenden Sie das **ENTRYREF** -Element, um auf eine andere Metadatendatei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="7679f-110">To reference another metafile, use the **ENTRYREF** element.</span></span> <span data-ttu-id="7679f-111">Ein **ENTRYREF** -Element in der primären Metadatei verweist auf eine externe Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="7679f-111">An **ENTRYREF** element in the primary metafile points to an external metafile.</span></span>

<span data-ttu-id="7679f-112">Das Windows Media Player-Steuerelement verarbeitet die **Einstiegs** Elemente der Metadatei, auf die verwiesen wird, als ob Sie in der primären Metadatendatei an der Position des **ENTRYREF** -Elements enthalten wären.</span><span class="sxs-lookup"><span data-stu-id="7679f-112">The Windows Media Player control processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="7679f-113">Allerdings werden alle **Eingabe** Elemente in der Metadatei, auf die verwiesen wird, ausgelassen, deren **skipifref** -Attribut auf "yes" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7679f-113">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="7679f-114">Die Windows Media Player 7,0-, 7,1-und Windows Media Player für Windows XP-Steuerelemente ignorieren alle **ENTRYREF** -Elemente in der Metadatei, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7679f-114">The Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP controls ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="7679f-115">Folglich können Metadateien nur eine Ebene tief in diesen Versionen verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="7679f-115">Thus, metafiles can only be nested one level deep using these versions.</span></span> <span data-ttu-id="7679f-116">Diese Versionen ignorieren auch das Element " **ASX** " und seine Attribute in der referenzierten Datei.</span><span class="sxs-lookup"><span data-stu-id="7679f-116">These versions also ignore the **ASX** element and its attributes in the referenced file.</span></span> <span data-ttu-id="7679f-117">Windows Media Player 9 oder höher unterstützt das Schachteln von Metadateien bis zu 5 Tiefe.</span><span class="sxs-lookup"><span data-stu-id="7679f-117">Windows Media Player 9 Series or later supports nesting metafiles up to 5 deep.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7679f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7679f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7679f-119">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="7679f-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




