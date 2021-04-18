---
title: Kunstdateien
description: Kunstdateien
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338411"
---
# <a name="art-files"></a><span data-ttu-id="12a04-107">Kunstdateien</span><span class="sxs-lookup"><span data-stu-id="12a04-107">Art Files</span></span>

<span data-ttu-id="12a04-108">Sie müssen eine oder mehrere kunstdateien für Ihre Skin erstellen.</span><span class="sxs-lookup"><span data-stu-id="12a04-108">You must create one or more art files for your skin.</span></span> <span data-ttu-id="12a04-109">Ohne Kunst kann der Benutzer nichts überprüfen.</span><span class="sxs-lookup"><span data-stu-id="12a04-109">Without art, the user will have nothing to look at.</span></span> <span data-ttu-id="12a04-110">Sie könnten ein unsichtbares Skin erstellen, aber niemand würde es sehen.</span><span class="sxs-lookup"><span data-stu-id="12a04-110">You could create an invisible skin, but no one would see it!</span></span> <span data-ttu-id="12a04-111">Selbst dann müssten Sie trotzdem kunstdateien für ihre unsichtbaren Bilder erstellen, da die Skin-Definitionsdatei kunstdateien für bestimmte Elemente erfordert.</span><span class="sxs-lookup"><span data-stu-id="12a04-111">And even then, you would still have to create art files to hold your invisible images, because the skin definition file requires art files for specific elements.</span></span>

<span data-ttu-id="12a04-112">Es gibt drei Verwendungsmöglichkeiten für Kunst in Skins: primäre Bilder, Mapping-Bilder und alternative Bilder.</span><span class="sxs-lookup"><span data-stu-id="12a04-112">There are three uses for art in skins: primary images, mapping images, and alternate images.</span></span>

## <a name="primary-images"></a><span data-ttu-id="12a04-113">Primäre Images</span><span class="sxs-lookup"><span data-stu-id="12a04-113">Primary Images</span></span>

<span data-ttu-id="12a04-114">Sie müssen ein primäres Image für Ihre Skin erstellen.</span><span class="sxs-lookup"><span data-stu-id="12a04-114">You must create a primary image for your skin.</span></span> <span data-ttu-id="12a04-115">Dies wird den Benutzern angezeigt, wenn Sie Ihre Skin installieren.</span><span class="sxs-lookup"><span data-stu-id="12a04-115">This is what the users will see when they install your skin.</span></span> <span data-ttu-id="12a04-116">Das primäre Image besteht aus einem oder mehreren Bildern, die von bestimmten Skin-Steuerelementen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="12a04-116">The primary image is composed of one or more images that are created by specific skin controls.</span></span>

<span data-ttu-id="12a04-117">Wenn Sie über mehr als ein Steuerelement verfügen, müssen Sie die z-Reihenfolge angeben, mit der definiert wird, welche Steuerelemente vor anderen Steuerelementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="12a04-117">If you have more than one control, you must specify the z-order, which defines which controls are displayed in front of other controls.</span></span> <span data-ttu-id="12a04-118">Jedes **Ansichts** Element verfügt über ein Hintergrundbild, dem Sie andere Element Bilder hinzufügen können, sodass Sie ein primäres verbundbild erstellen können.</span><span class="sxs-lookup"><span data-stu-id="12a04-118">Each **View** element will have a background image that you can add other element images to, allowing you to create a primary composite image.</span></span>

<span data-ttu-id="12a04-119">Möglicherweise verfügen Sie auch über sekundäre Images, z. b. eine gleitende Leiste, die nicht angezeigt wird, wenn die Skin zum ersten Mal angezeigt wird. Diese werden jedoch angezeigt, wenn der Benutzer eine Aktion durchführt.</span><span class="sxs-lookup"><span data-stu-id="12a04-119">You also may have secondary images, such as a sliding tray, that do not display when your skin first appears, but that show up when the user takes some action.</span></span> <span data-ttu-id="12a04-120">Diese Regeln folgen denselben Regeln wie primäre Images, da Sie mit einem Satz von Steuerelementen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="12a04-120">These follow the same rules as primary images, in that they are created with a set of controls.</span></span>

## <a name="mapping-images"></a><span data-ttu-id="12a04-121">Mapping von Bildern</span><span class="sxs-lookup"><span data-stu-id="12a04-121">Mapping Images</span></span>

<span data-ttu-id="12a04-122">Eines der leistungsstärksten Features von Windows Media Player Skins ist, dass Sie die Image Zuordnung verwenden können, um Ereignisse für Ihre Skin zu Triggern zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="12a04-122">One of the most powerful features of Windows Media Player skins is that you can use image mapping to trigger events for your skin.</span></span> <span data-ttu-id="12a04-123">Bild Zuordnungen sind Dateien, die besondere Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="12a04-123">Image maps are files that contain special images.</span></span> <span data-ttu-id="12a04-124">Die Bilder in einer Imagemapdatei sind jedoch nicht zum Anzeigen durch den Benutzer gedacht, sondern werden von Windows Media Player verwendet, um Maßnahmen zu ergreifen, wenn der Benutzer auf die Skin klickt.</span><span class="sxs-lookup"><span data-stu-id="12a04-124">The images in an image map file, however, are not meant to be viewed by the user, but are used by Windows Media Player to take action when the user clicks on your skin.</span></span>

<span data-ttu-id="12a04-125">Für verschiedene Steuerelemente sind unterschiedliche Arten von Bild Zuordnungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="12a04-125">Different controls need different kinds of image maps.</span></span> <span data-ttu-id="12a04-126">Wenn Sie z. b. einem Teil eines Bilds einen bestimmten roten Wert zuordnen und der Benutzer auf den entsprechenden Bereich des primären Bilds klickt, wird ein Ereignis durch eine Schaltfläche ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="12a04-126">For example, if you color part of an image map a specific red value, and the user clicks on the corresponding area of your primary image, a button will fire an event.</span></span> <span data-ttu-id="12a04-127">Die Farbe wird verwendet, um zu definieren, welche Ereignisse ausgelöst werden, indem Sie auf einen bestimmten Bereich der Skin klicken.</span><span class="sxs-lookup"><span data-stu-id="12a04-127">Color is used to define which events are triggered by clicking in a particular area of the skin.</span></span>

## <a name="alternate-images"></a><span data-ttu-id="12a04-128">Alternative Images</span><span class="sxs-lookup"><span data-stu-id="12a04-128">Alternate Images</span></span>

<span data-ttu-id="12a04-129">Sie können auch alternative Images einrichten, die angezeigt werden, wenn ein Benutzer etwas bewirkt.</span><span class="sxs-lookup"><span data-stu-id="12a04-129">You can also set up alternate images to display when a user does something.</span></span> <span data-ttu-id="12a04-130">Beispielsweise können Sie ein alternatives Bild einer Schaltfläche erstellen, das nur angezeigt wird, wenn mit dem Mauszeiger auf die Schaltfläche gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="12a04-130">For example, you can create an alternate image of a button that will be displayed only when the mouse hovers over the button.</span></span> <span data-ttu-id="12a04-131">Dies ist eine gute Möglichkeit, den Benutzern mitzuteilen, was Sie tun können, und es ist auch möglich, eine stark erkennbare Benutzeroberfläche zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="12a04-131">This is a good way to let users know what they can do, and also allows for a highly discoverable user interface.</span></span> <span data-ttu-id="12a04-132">Durch die sorgfältige Verwendung von Quick Infos und Hover-Bildern können Sie ungewöhnliche Benutzeroberflächen erstellen, die dem Benutzer weiterhin Feedback zu den verfügbaren Optionen geben.</span><span class="sxs-lookup"><span data-stu-id="12a04-132">By using ToolTips and hover images carefully, you can create unusual user interfaces that still give the user feedback about what options are available.</span></span>

<span data-ttu-id="12a04-133">In den folgenden Abschnitten finden Sie weitere Informationen zu kunstdateien:</span><span class="sxs-lookup"><span data-stu-id="12a04-133">The following sections provide more information about art files:</span></span>

-   [<span data-ttu-id="12a04-134">Primäre Images</span><span class="sxs-lookup"><span data-stu-id="12a04-134">Primary Images</span></span>](primary-images.md)
-   [<span data-ttu-id="12a04-135">Mapping von Bildern</span><span class="sxs-lookup"><span data-stu-id="12a04-135">Mapping Images</span></span>](mapping-images.md)
-   [<span data-ttu-id="12a04-136">Alternative Images</span><span class="sxs-lookup"><span data-stu-id="12a04-136">Alternate Images</span></span>](alternate-images.md)
-   [<span data-ttu-id="12a04-137">Kunst Dateiformate</span><span class="sxs-lookup"><span data-stu-id="12a04-137">Art File Formats</span></span>](art-file-formats.md)
-   [<span data-ttu-id="12a04-138">Beispiel für einfache Kunst</span><span class="sxs-lookup"><span data-stu-id="12a04-138">Simple Art Example</span></span>](simple-art-example.md)

## <a name="related-topics"></a><span data-ttu-id="12a04-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12a04-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a04-140">**Skin-Dateien**</span><span class="sxs-lookup"><span data-stu-id="12a04-140">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




