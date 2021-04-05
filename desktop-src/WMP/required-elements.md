---
title: Erforderliche Elemente
description: Erforderliche Elemente
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player Mobile Skins, Elemente
- Skins, Elemente
- Skin-Definitions Dateien, Elemente
- Elemente, Skin-Definitions Dateien
- Elemente, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710877"
---
# <a name="required-elements"></a><span data-ttu-id="fea44-108">Erforderliche Elemente</span><span class="sxs-lookup"><span data-stu-id="fea44-108">Required Elements</span></span>

<span data-ttu-id="fea44-109">Sie müssen die folgenden Elemente in der Skin-Definitionsdatei angeben:</span><span class="sxs-lookup"><span data-stu-id="fea44-109">You must provide the following elements in your skin definition file:</span></span>

-   <span data-ttu-id="fea44-110">**Header.**</span><span class="sxs-lookup"><span data-stu-id="fea44-110">**Header.**</span></span> <span data-ttu-id="fea44-111">Der Header der Haupt Skin-Definitionsdatei ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fea44-111">The main skin definition file header is required.</span></span> <span data-ttu-id="fea44-112">Informationen zur Header Version finden Sie in der Tabelle im Abschnitt [Erstellen einer Skin-Definitionsdatei](creating-a-skin-definition-file.md) .</span><span class="sxs-lookup"><span data-stu-id="fea44-112">For header version information, see the table in the [Creating a Skin Definition File](creating-a-skin-definition-file.md) section.</span></span>
-   <span data-ttu-id="fea44-113">**Abschnitt Beschreibung.**</span><span class="sxs-lookup"><span data-stu-id="fea44-113">**Description section.**</span></span> <span data-ttu-id="fea44-114">Der Abschnitt Beschreibung ist erforderlich, wenn Sie Skins für Windows Media Player 9-Reihe für Windows Mobile erstellen.</span><span class="sxs-lookup"><span data-stu-id="fea44-114">The Description section is required when creating skins for Windows Media Player 9 Series for Windows Mobile.</span></span> <span data-ttu-id="fea44-115">Dies muss der erste Abschnitt in der Skin-Definitionsdatei sein, und es muss gültige Werte für Dimensionen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fea44-115">It must be the first section in the skin definition file, and it must specify valid values for Dimensions.</span></span> <span data-ttu-id="fea44-116">Die Angabe eines Werts für die Ausrichtung ist optional.</span><span class="sxs-lookup"><span data-stu-id="fea44-116">Specifying a value for Orientation is optional.</span></span>
-   <span data-ttu-id="fea44-117">**Abschnitt Bitmaps.**</span><span class="sxs-lookup"><span data-stu-id="fea44-117">**Bitmaps section.**</span></span> <span data-ttu-id="fea44-118">Der Abschnitt "Bitmaps" ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fea44-118">The Bitmaps section is required.</span></span> <span data-ttu-id="fea44-119">Außerdem muss im Abschnitt Bitmaps gültige Namen für die Dateien background, deaktiviert, per pushübertragung, Region und Super Image angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fea44-119">Additionally, the Bitmaps section must specify valid names for Background, Disabled, Pushed, Region, and Super image files.</span></span>
-   <span data-ttu-id="fea44-120">**Bilddateien.**</span><span class="sxs-lookup"><span data-stu-id="fea44-120">**Image files.**</span></span> <span data-ttu-id="fea44-121">Sie müssen Hintergrund-, deaktivierte, pushdateien, Regions-und Super Bilddateien als Teil ihrer Skin bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fea44-121">You must provide Background, Disabled, Pushed, Region, and Super image files as part of your skin.</span></span> <span data-ttu-id="fea44-122">Wenn Sie Skins für Windows Media Player 10 Mobile oder höher erstellen, müssen Sie keine Regions-oder Super Image Dateien einschließen.</span><span class="sxs-lookup"><span data-stu-id="fea44-122">If you are creating skins for Windows Media Player 10 Mobile or later, you do not need to include Region or Super image files.</span></span>

<span data-ttu-id="fea44-123">Wenn Sie eine Skin erstellen, für die nur Bilder definiert sind, wird die Skin angezeigt, bietet dem Benutzer jedoch keine sinnvollen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fea44-123">If you create a skin with only images defined, the skin will be visible, but will not offer any meaningful functionality to the user.</span></span> <span data-ttu-id="fea44-124">Wenn Sie sich dafür entscheiden, eine Skin ohne Schaltflächen zu erstellen, um zu verhindern, dass der Benutzer bestimmte Inhalte überspringt, beachten Sie, dass es möglicherweise dennoch möglich ist, die Funktionalität den Hardware Schaltflächen auf dem Gerät zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="fea44-124">If you decide to create a skin without buttons, perhaps to prevent the user from skipping over certain content, be aware that it may still be possible to map functionality to the hardware buttons on the device.</span></span>

<span data-ttu-id="fea44-125">Thumb-Dateien sind erforderlich, und ihre trackbars können nicht ohne Daumen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fea44-125">Thumb files are required and your trackbars cannot be used without thumbs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fea44-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fea44-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea44-127">**Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="fea44-127">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 




