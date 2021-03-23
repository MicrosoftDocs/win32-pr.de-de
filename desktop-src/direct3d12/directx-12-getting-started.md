---
title: Grundlegendes zu Direct3D 12
description: Um 3D-Spiele und-Apps für Windows 10 und Windows 10 Mobile zu schreiben, müssen Sie sich mit den Grundlagen der Direct3D 12-Technologie und der Vorbereitung der Verwendung in ihren spielen und apps vertraut machen.
ms.assetid: DED7A434-FCD4-4F41-8B2C-E5AE6E48430F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1353c8c66fd401e364b9db302463f164f757c9ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548749"
---
# <a name="understanding-direct3d-12"></a><span data-ttu-id="0e0be-103">Grundlegendes zu Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0e0be-103">Understanding Direct3D 12</span></span>

<span data-ttu-id="0e0be-104">Um 3D-Spiele und-Apps für Windows 10 und Windows 10 Mobile zu schreiben, müssen Sie sich mit den Grundlagen der Direct3D 12-Technologie und der Vorbereitung der Verwendung in ihren spielen und apps vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="0e0be-104">To write 3D games and apps for Windows 10 and Windows 10 Mobile, you must understand the basics of the Direct3D 12 technology, and how to prepare to use it in your games and apps.</span></span>

<span data-ttu-id="0e0be-105">In den Themen in diesem Abschnitt finden Sie Informationen zur Umgebung, in der Sie Ihre apps und Spiele mit Direct3D 12 programmieren.</span><span class="sxs-lookup"><span data-stu-id="0e0be-105">Use the topics in this section to set up and learn about the environment in which you will program your apps and games with Direct3D 12.</span></span> <span data-ttu-id="0e0be-106">Diese Inhalte helfen Ihnen auch, ihre Direct3D 11-apps und-Spiele auf Direct3D 12 zu portieren, sodass Sie die Vorteile der Features und Effizienz von Direct3D 12 nutzen können.</span><span class="sxs-lookup"><span data-stu-id="0e0be-106">This content will also help you to port your Direct3D 11 apps and games to Direct3D 12, so you can take advantage of Direct3D 12 features and efficiencies.</span></span>

<span data-ttu-id="0e0be-107">Um mit Direct3D 12 programmieren zu können, benötigen Sie folgende Komponenten:</span><span class="sxs-lookup"><span data-stu-id="0e0be-107">To program with Direct3D 12, you need these components:</span></span>

-   <span data-ttu-id="0e0be-108">Eine Hardwareplattform mit einer Direct3D 12-kompatiblen GPU</span><span class="sxs-lookup"><span data-stu-id="0e0be-108">A hardware platform with a Direct3D 12-compatible GPU</span></span>
-   <span data-ttu-id="0e0be-109">[Anzeigen von Treibern](/previous-versions//ff569172(v=vs.85)) , die das Windows-Anzeigetreiber Modell (WDDM) 2,0 unterstützen</span><span class="sxs-lookup"><span data-stu-id="0e0be-109">[Display drivers](/previous-versions//ff569172(v=vs.85)) that support the Windows Display Driver Model (WDDM) 2.0</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0e0be-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0e0be-110">In this section</span></span>



| <span data-ttu-id="0e0be-111">Thema</span><span class="sxs-lookup"><span data-stu-id="0e0be-111">Topic</span></span>                                                                                                               | <span data-ttu-id="0e0be-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e0be-112">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e0be-113">Setup für die Direct3D 12-Programmierumgebung</span><span class="sxs-lookup"><span data-stu-id="0e0be-113">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)<br/>               | <span data-ttu-id="0e0be-114">Beschreibt die Installation, Tools und unterstützten Bibliotheken, die eine produktive Direct3D 12-Entwicklungsumgebung bilden.</span><span class="sxs-lookup"><span data-stu-id="0e0be-114">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span> <br/>                              |
| [<span data-ttu-id="0e0be-115">Erstellen einer grundlegenden Direct3D 12-Komponente</span><span class="sxs-lookup"><span data-stu-id="0e0be-115">Creating a Basic Direct3D 12 Component</span></span>](creating-a-basic-direct3d-12-component.md)<br/>                     | <span data-ttu-id="0e0be-116">In diesem Thema wird der aufrufflow zum Erstellen einer grundlegenden Direct3D 12-Komponente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0e0be-116">This topic describes the call flow to create a basic Direct3D 12 component.</span></span><br/>                                                                            |
| [<span data-ttu-id="0e0be-117">Wichtige Änderungen von Direct3D 11 zu Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0e0be-117">Important Changes from Direct3D 11 to Direct3D 12</span></span>](important-changes-from-directx-11-to-directx-12.md)<br/> | <span data-ttu-id="0e0be-118">Direct3D 12 stellt eine bedeutende Abweichung vom Programmiermodell Direct3D 11 dar.</span><span class="sxs-lookup"><span data-stu-id="0e0be-118">Direct3D 12 represents a significant departure from the Direct3D 11 programming model.</span></span> <span data-ttu-id="0e0be-119">Mit Direct3D 12 können apps näher an der Hardware heran liegen als je zuvor.</span><span class="sxs-lookup"><span data-stu-id="0e0be-119">Direct3D 12 lets apps get closer to hardware than ever before.</span></span> <br/> |
| [<span data-ttu-id="0e0be-120">Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="0e0be-120">Hardware Feature Levels</span></span>](hardware-feature-levels.md)<br/>                                                   | <span data-ttu-id="0e0be-121">Beschreibt die Funktionalität der- \_ Hardware Funktionsebenen von 11 bis 12 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="0e0be-121">Describes the functionality of the 11\_0 through 12\_1 hardware feature levels.</span></span><br/>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="0e0be-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0e0be-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e0be-123">Direct3D 12-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="0e0be-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

