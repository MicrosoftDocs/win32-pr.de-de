---
title: Iagentcommandwindow
description: Iagentcommandwindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338600"
---
# <a name="iagentcommandwindow"></a><span data-ttu-id="a94fe-103">Iagentcommandwindow</span><span class="sxs-lookup"><span data-stu-id="a94fe-103">IAgentCommandWindow</span></span>

<span data-ttu-id="a94fe-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a94fe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a94fe-105">**Iagentcommandwindow** definiert eine Schnittstelle, die es Anwendungen ermöglicht, die Eigenschaften des Fensters "Sprachbefehle" festzulegen und abzufragen.</span><span class="sxs-lookup"><span data-stu-id="a94fe-105">**IAgentCommandWindow** defines an interface that allows applications to set and query the properties of the Voice Commands Window.</span></span> <span data-ttu-id="a94fe-106">Das Fenster "Sprachbefehle" ist eine freigegebene Ressource, die in erster Linie so konzipiert ist, dass Benutzer sprach fähige Befehle anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="a94fe-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="a94fe-107">Wenn die Spracherkennung deaktiviert ist, wird das Fenster für die Sprachbefehle weiterhin angezeigt, und der Text "Spracheingabe ist deaktiviert" (in der Sprache des Zeichens).</span><span class="sxs-lookup"><span data-stu-id="a94fe-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="a94fe-108">Wenn keine Sprach-Engine installiert ist, die mit der Spracheinstellung des Zeichens übereinstimmt, zeigt das Fenster an, dass die Spracheingabe nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a94fe-108">If no speech engine is installed that matches the character's language setting, the window displays, "Speech input not available."</span></span> <span data-ttu-id="a94fe-109">Wenn der Input-Active Client keine sprach Parameter für seine Befehle definiert hat und die globalen Sprachbefehle deaktiviert sind, wird im Fenster "keine Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a94fe-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="a94fe-110">Sie können auch die Eigenschaften des Fensters "Sprachbefehle" Abfragen, unabhängig davon, ob die Spracheingabe deaktiviert ist oder eine kompatible Sprach-Engine installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a94fe-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

<span data-ttu-id="a94fe-111">**Methoden in Vtable-Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="a94fe-111">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="a94fe-112">Iagentcommandwindow-Methoden</span><span class="sxs-lookup"><span data-stu-id="a94fe-112">IAgentCommandWindow Methods</span></span>                             | <span data-ttu-id="a94fe-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a94fe-113">Description</span></span>                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a94fe-114">**SetVisible**</span><span class="sxs-lookup"><span data-stu-id="a94fe-114">**SetVisible**</span></span>](iagentcommandwindow--setvisible.md)   | <span data-ttu-id="a94fe-115">Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft des Sprachbefehle Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="a94fe-115">Sets the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span>    |
| [<span data-ttu-id="a94fe-116">**GetVisible**</span><span class="sxs-lookup"><span data-stu-id="a94fe-116">**GetVisible**</span></span>](iagentcommandwindow--getvisible.md)   | <span data-ttu-id="a94fe-117">Gibt den Wert der [**Visible**](visible-property.md) -Eigenschaft des Sprachbefehle Fensters zurück.</span><span class="sxs-lookup"><span data-stu-id="a94fe-117">Returns the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span> |
| [<span data-ttu-id="a94fe-118">**GetPosition**</span><span class="sxs-lookup"><span data-stu-id="a94fe-118">**GetPosition**</span></span>](iagentcommandwindow--getposition.md) | <span data-ttu-id="a94fe-119">Gibt die Position des Sprachbefehle Fensters zurück.</span><span class="sxs-lookup"><span data-stu-id="a94fe-119">Returns the position of the Voice Commands Window.</span></span>                                                  |
| [<span data-ttu-id="a94fe-120">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="a94fe-120">**GetSize**</span></span>](iagentcommandwindow--getsize.md)         | <span data-ttu-id="a94fe-121">Gibt die Größe des Sprachbefehle Fensters zurück.</span><span class="sxs-lookup"><span data-stu-id="a94fe-121">Returns the size of the Voice Commands Window.</span></span>                                                      |



 

 

 




