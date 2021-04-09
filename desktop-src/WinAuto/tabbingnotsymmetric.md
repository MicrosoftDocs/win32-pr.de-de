---
title: Tabbingnotsymmetric
description: Tabbingnotsymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101875"
---
# <a name="tabbingnotsymmetric"></a><span data-ttu-id="f03f1-103">Tabbingnotsymmetric</span><span class="sxs-lookup"><span data-stu-id="f03f1-103">TabbingNotSymmetric</span></span>

## <a name="text"></a><span data-ttu-id="f03f1-104">Text</span><span class="sxs-lookup"><span data-stu-id="f03f1-104">Text</span></span>

<span data-ttu-id="f03f1-105">Ein rückwärts-und vorwärts-Tabstopps ergibt nicht dasselbe Element.</span><span class="sxs-lookup"><span data-stu-id="f03f1-105">Tabbing backwards and forwards does not yield the same element.</span></span> <span data-ttu-id="f03f1-106">Erwartet, {0} aber empfangen {1}</span><span class="sxs-lookup"><span data-stu-id="f03f1-106">Expected {0} but received {1}</span></span>

## <a name="type"></a><span data-ttu-id="f03f1-107">type</span><span class="sxs-lookup"><span data-stu-id="f03f1-107">Type</span></span>

<span data-ttu-id="f03f1-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="f03f1-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="f03f1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f03f1-109">Description</span></span>

<span data-ttu-id="f03f1-110">Bei Verwendung der Standardtastatur Navigation (Tab oder UMSCHALT + TAB) ist es nicht möglich, den Pfad des Durchlaufs durch die Elementstruktur des Überprüfungs Ziels zu wiederholen, wenn die Richtung des Durchlaufs umgekehrt ist.</span><span class="sxs-lookup"><span data-stu-id="f03f1-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to repeat the path of traversal through the element tree of the verification target if the direction of traversal is reversed.</span></span> <span data-ttu-id="f03f1-111">Beispielsweise führt das x-fache der Tabulator Taste (Tabulator x) von Element a (0) zu Element a (x) und die anschließende Tab-Taste (UMSCHALT + TAB) x mal dazu, dass Element a (0) den Fokus durch einen anderen Satz von zwischen Elementen wiedererlangt.</span><span class="sxs-lookup"><span data-stu-id="f03f1-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times results in element A(0) regaining focus through a different set of intermediate elements.</span></span>

<span data-ttu-id="f03f1-112">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da das Durchlaufen von Elementen unberechenbar und unvorhersehbar</span><span class="sxs-lookup"><span data-stu-id="f03f1-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements appears erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f03f1-113">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="f03f1-113">Possible causes</span></span>

-   <span data-ttu-id="f03f1-114">Mehrere Elemente oder ihre übergeordneten Elemente sind benutzerdefinierte Steuerelemente, die die Tabstopps nicht ordnungsgemäß implementieren.</span><span class="sxs-lookup"><span data-stu-id="f03f1-114">Multiple elements or their parents are custom controls that don't implement tabbing correctly.</span></span> <span data-ttu-id="f03f1-115">Beispielsweise ist die Eigenschaft MSAA State nicht ordnungsgemäß festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f03f1-115">For example, the MSAA State property is not set correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f03f1-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f03f1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f03f1-117">Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f03f1-117">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 