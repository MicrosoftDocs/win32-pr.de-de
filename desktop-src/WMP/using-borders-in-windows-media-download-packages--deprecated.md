---
title: Verwenden von Rahmen in Windows-Medien Download Paketen (veraltet)
description: Verwenden von Rahmen in Windows-Medien Download Paketen (veraltet)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Rahmen, Informationen
- Windows Media Download Packages, Rahmen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388398"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="af1aa-109">Verwenden von Rahmen in Windows-Medien Download Paketen (veraltet)</span><span class="sxs-lookup"><span data-stu-id="af1aa-109">Using Borders in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="af1aa-110">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="af1aa-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="af1aa-111">Rahmen ermöglichen es Ihnen, eine angepasste grafische Benutzeroberfläche für Ihren verpackten Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="af1aa-111">Borders enable you to create a customized graphical user interface for your packaged content.</span></span> <span data-ttu-id="af1aa-112">Der Rahmen kann Elemente enthalten, wie z. b. Bilder, interaktive Steuerelemente und Links zu Websites.</span><span class="sxs-lookup"><span data-stu-id="af1aa-112">The border can include elements such as images, interactive controls, and links to websites.</span></span> <span data-ttu-id="af1aa-113">Sie können Rahmen in Fällen verwenden, in denen Sie Ihren gepackten Inhalt, z. b. Branding oder Werbung, zusätzlichen Wert hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="af1aa-113">You can use borders in cases where you want to add additional value to your packaged content, such as for branding or advertising.</span></span> <span data-ttu-id="af1aa-114">Nachdem Benutzer Ihr Windows Media-Downloadpaket heruntergeladen und geöffnet haben, zeigt Windows Media Player automatisch Ihren benutzerdefinierten Rahmen an, wenn der gepackte Inhalt wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af1aa-114">After users download and open your Windows Media Download package, Windows Media Player automatically displays your custom border when it plays the packaged content.</span></span>

<span data-ttu-id="af1aa-115">Im Gegensatz zu einem Skin, das es Benutzern ermöglicht, die Benutzeroberfläche von Windows Media Player vollständig zu ersetzen, wird ein Rahmen nur im Fenster " **jetzt** wiedergegeben" des vollmodusplayers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af1aa-115">Unlike a skin, which enables users to completely replace the Windows Media Player user interface, a border is displayed only in the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="af1aa-116">Die gleichen Tools und Technologien, die Sie zum Erstellen von Skins verwenden, werden jedoch auch zum Erstellen von Rahmen verwendet.</span><span class="sxs-lookup"><span data-stu-id="af1aa-116">However, the same tools and technologies that you use to create skins are also used to create borders.</span></span> <span data-ttu-id="af1aa-117">Die folgende Abbildung zeigt einen Rahmen.</span><span class="sxs-lookup"><span data-stu-id="af1aa-117">The following illustration shows a border.</span></span>

![ein Rahmen, der in Windows Media Player 10 angezeigt wird.](images/border-v10.png)

<span data-ttu-id="af1aa-119">Es ist wichtig, sich mit den grundlegenden Techniken zum Erstellen einer Skin vertraut zu machen, bevor Sie versuchen, einen Rahmen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="af1aa-119">It is important to understand the basic techniques for creating a skin before attempting to create a border.</span></span> <span data-ttu-id="af1aa-120">Die Rahmen Programmierung erfolgt mithilfe von zwei Programmiersprachen: Extensible Markup Language (XML) und Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="af1aa-120">Border programming is accomplished using two programming languages: Extensible Markup Language (XML) and Microsoft JScript.</span></span> <span data-ttu-id="af1aa-121">XML wird zum Definieren von Schnittstellen Elementen verwendet, z. b. Schaltflächen, Schieberegler und Textfelder.</span><span class="sxs-lookup"><span data-stu-id="af1aa-121">XML is used to define interface elements such as buttons, sliders, and text boxes.</span></span> <span data-ttu-id="af1aa-122">Sie müssen nicht alle XML-Details verstehen, da Sie keine neuen XML-Code Elemente schreiben müssen. Sie können einfach die von Windows Media Player bereitgestellten verwenden.</span><span class="sxs-lookup"><span data-stu-id="af1aa-122">You don't need to understand all the details of XML since you don't have to write new XML code elements; you can simply use the ones provided by Windows Media Player.</span></span> <span data-ttu-id="af1aa-123">Obwohl JScript zum Erstellen von Rahmen nicht erforderlich ist, kann es verwendet werden, um zusätzliche Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="af1aa-123">Although JScript is not required for creating borders, it can be used to provide additional functionality.</span></span>

<span data-ttu-id="af1aa-124">Eine komprimierte Rahmen Datei mit der Dateinamenerweiterung. WMZ enthält eine Rahmen Definitionsdatei mit der Dateinamenerweiterung. WMS und alle Bilddateien, die innerhalb des Rahmens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af1aa-124">A compressed border file with a .wmz file name extension includes a border definition file with a .wms file name extension and all the image files used within the border.</span></span>

<span data-ttu-id="af1aa-125">Wenn Sie einen Rahmen in ein Windows Media Download-Paket einschließen möchten, erstellen Sie einfach einen Rahmen, und verweisen Sie auf diesen Rahmen in einer Windows Media Metadatei-Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="af1aa-125">To include a border in a Windows Media Download package, simply create a border and reference that border in a Windows Media metafile playlist.</span></span> <span data-ttu-id="af1aa-126">Die Rahmen Datei wird in Windows Media Player geladen, nachdem der Player die Metadatendatei analysiert und das **Skin** -Element interpretiert hat, das auf den Rahmen verweist.</span><span class="sxs-lookup"><span data-stu-id="af1aa-126">The border file is loaded into Windows Media Player after the Player parses the metafile and interprets the **SKIN** element that references the border.</span></span> <span data-ttu-id="af1aa-127">Das **Skin** -Element wird nur für Rahmen verwendet, und das href-Attribut des **Skin** -Elements kann nur auf ein Skin für jedes Paket verweisen.</span><span class="sxs-lookup"><span data-stu-id="af1aa-127">The **SKIN** element is used only for borders, and the HREF attribute of the **SKIN** element can reference only one skin for each package.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af1aa-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af1aa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af1aa-129">**Rahmen für Windows-Media Player (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="af1aa-129">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="af1aa-130">**Windows Media-Download Pakete (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="af1aa-130">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="af1aa-131">**Windows Media Player Skins**</span><span class="sxs-lookup"><span data-stu-id="af1aa-131">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




