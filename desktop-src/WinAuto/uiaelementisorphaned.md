---
title: Uiaelementisorphaned
description: Uiaelementisorphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340213"
---
# <a name="uiaelementisorphaned"></a><span data-ttu-id="f2c97-103">Uiaelementisorphaned</span><span class="sxs-lookup"><span data-stu-id="f2c97-103">UiaElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="f2c97-104">Text</span><span class="sxs-lookup"><span data-stu-id="f2c97-104">Text</span></span>

<span data-ttu-id="f2c97-105">Das Element ist ein verwaistes AutomationElement in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f2c97-105">Element is an orphaned AutomationElement in the tree</span></span>

## <a name="type"></a><span data-ttu-id="f2c97-106">type</span><span class="sxs-lookup"><span data-stu-id="f2c97-106">Type</span></span>

<span data-ttu-id="f2c97-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2c97-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f2c97-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c97-108">Description</span></span>

<span data-ttu-id="f2c97-109">Die Adresse der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle des Objekts, die für die angegebenen Koordinaten abgerufen wurde, ist ein Verweis auf ein verwaistes Element in der Elementstruktur.</span><span class="sxs-lookup"><span data-stu-id="f2c97-109">The address of the object's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="f2c97-110">Dieses Problem ist ein Problem für Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, da Elemente als unsichtbar behandelt werden und dem Benutzer nicht angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="f2c97-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f2c97-111">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="f2c97-111">Possible causes</span></span>

-   <span data-ttu-id="f2c97-112">Die Benutzerinteraktion während der Überprüfung, z. b. das Verschieben des Fokus auf ein nicht-Ziel-HWND, hat den Überprüfungs Vorgang beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="f2c97-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="f2c97-113">Eine falsche oder ungültige Implementierung der Benutzeroberflächen Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="f2c97-113">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2c97-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2c97-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2c97-115">**Iuiautomationelement. elementFromPoint**</span><span class="sxs-lookup"><span data-stu-id="f2c97-115">**IUIAutomationElement.ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




