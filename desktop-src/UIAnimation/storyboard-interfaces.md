---
title: Storyboardschnittstellen
description: Dieser Abschnitt enthält die Referenz Spezifikationen für die Windows Animation Manager-Schnittstellen, die Storyboards unterstützen.
ms.assetid: 372D6348-3DF2-48EB-B495-BAD4E5DAAAD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fba60c480ef4c316731da6eefbe5334616a72b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039178"
---
# <a name="storyboard-interfaces"></a><span data-ttu-id="53326-103">Storyboardschnittstellen</span><span class="sxs-lookup"><span data-stu-id="53326-103">Storyboard Interfaces</span></span>

<span data-ttu-id="53326-104">Dieser Abschnitt enthält die Referenz Spezifikationen für die Windows Animation Manager-Schnittstellen, die Storyboards unterstützen.</span><span class="sxs-lookup"><span data-stu-id="53326-104">This section contains the reference specifications for the Windows Animation Manager interfaces that support storyboards.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53326-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="53326-105">In this section</span></span>



| <span data-ttu-id="53326-106">Thema</span><span class="sxs-lookup"><span data-stu-id="53326-106">Topic</span></span>                                                                                                 | <span data-ttu-id="53326-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53326-107">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53326-108">**Iuianimationstoryboard**</span><span class="sxs-lookup"><span data-stu-id="53326-108">**IUIAnimationStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)<br/>                                   | <span data-ttu-id="53326-109">Definiert ein Storyboard, das eine Gruppe von Übergängen enthält, die relativ zueinander synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="53326-109">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="53326-110">**IUIAnimationStoryboard2**</span><span class="sxs-lookup"><span data-stu-id="53326-110">**IUIAnimationStoryboard2**</span></span>](/windows/win32/api/uianimation/nn-uianimation-iuianimationstoryboard2)<br/>                                 | <span data-ttu-id="53326-111">Definiert ein Storyboard, das eine Gruppe von Übergängen enthält, die relativ zueinander synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="53326-111">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="53326-112">**Iuianimationstoryboarde venthandler**</span><span class="sxs-lookup"><span data-stu-id="53326-112">**IUIAnimationStoryboardEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler)<br/>           | <span data-ttu-id="53326-113">Definiert Methoden für die Verarbeitung von Status-und Update Ereignissen für ein Storyboard.</span><span class="sxs-lookup"><span data-stu-id="53326-113">Defines methods for handling status and update events for a storyboard.</span></span><br/>                                    |
| [<span data-ttu-id="53326-114">**IUIAnimationStoryboardEventHandler2**</span><span class="sxs-lookup"><span data-stu-id="53326-114">**IUIAnimationStoryboardEventHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler2)<br/>         | <span data-ttu-id="53326-115">Definiert Methoden zum Verarbeiten von Storyboard-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="53326-115">Defines methods for handling storyboard events.</span></span> <br/>                                                           |
| [<span data-ttu-id="53326-116">**IUIAnimationLoopIterationChangeHandler2**</span><span class="sxs-lookup"><span data-stu-id="53326-116">**IUIAnimationLoopIterationChangeHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationloopiterationchangehandler2)<br/> | <span data-ttu-id="53326-117">Definiert eine Methode zum Verarbeiten von Storyboard-Schleifen Iterations Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="53326-117">Defines a method for handling storyboard loop iteration events.</span></span><br/>                                            |
| [<span data-ttu-id="53326-118">**Iuianimationprioritycomparison**</span><span class="sxs-lookup"><span data-stu-id="53326-118">**IUIAnimationPriorityComparison**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)<br/>                   | <span data-ttu-id="53326-119">Definiert eine Methode für den Prioritäts Vergleich, die der Animations-Manager verwendet, um Planungs Konflikte aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="53326-119">Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.</span></span><br/>  |
| [<span data-ttu-id="53326-120">**IUIAnimationPriorityComparison2**</span><span class="sxs-lookup"><span data-stu-id="53326-120">**IUIAnimationPriorityComparison2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison2)<br/>                 | <span data-ttu-id="53326-121">Definiert eine Methode, die Planungs Konflikte mithilfe des Prioritäts Vergleichs auflöst.</span><span class="sxs-lookup"><span data-stu-id="53326-121">Defines a method that resolves scheduling conflicts through priority comparison.</span></span><br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="53326-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53326-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53326-123">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="53326-123">Interfaces</span></span>](windows-animation-reference.md)
</dt> </dl>

 

