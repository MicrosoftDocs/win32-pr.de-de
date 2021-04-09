---
title: Uianameshouldnotcontaincontroltype
description: Uianameshouldnotcontaincontroltype
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855839"
---
# <a name="uianameshouldnotcontaincontroltype"></a><span data-ttu-id="f921d-103">Uianameshouldnotcontaincontroltype</span><span class="sxs-lookup"><span data-stu-id="f921d-103">UiaNameShouldNotContainControlType</span></span>

## <a name="text"></a><span data-ttu-id="f921d-104">Text</span><span class="sxs-lookup"><span data-stu-id="f921d-104">Text</span></span>

<span data-ttu-id="f921d-105">Der Name des Elements ( {0} ) darf den Text des ControlType () nicht enthalten. {1}</span><span class="sxs-lookup"><span data-stu-id="f921d-105">Element's Name ({0}) should not contain the text of the ControlType ({1})</span></span>

## <a name="type"></a><span data-ttu-id="f921d-106">type</span><span class="sxs-lookup"><span data-stu-id="f921d-106">Type</span></span>

<span data-ttu-id="f921d-107">Warnung</span><span class="sxs-lookup"><span data-stu-id="f921d-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="f921d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f921d-108">Description</span></span>

<span data-ttu-id="f921d-109">Der Name eines Elements enthält seinen UIA-Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="f921d-109">The name of an element incorporates its UIA control type.</span></span> <span data-ttu-id="f921d-110">Diese Warnung kann z. b. auftreten, wenn die UIA-Name-Eigenschaft für ein Element mit dem Steuer Elementtyp "Button" auf "My Button" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f921d-110">For example, this warning can occur if the UIA Name property for an element with the Button control type is set to "My Button".</span></span>

<span data-ttu-id="f921d-111">Dieses Problem führt dazu, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, den Steuerelement Typ zweimal lesen, oder dass er für Benutzer unerklärbar oder nicht intuitiv ist.</span><span class="sxs-lookup"><span data-stu-id="f921d-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the control type will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f921d-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="f921d-112">Possible causes</span></span>

-   <span data-ttu-id="f921d-113">Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f921d-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="f921d-114">Das Element oder das übergeordnete Element verfügt über einen Standardnamen, der nicht auf einen anzeigen Amen überarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f921d-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="f921d-115">Zum Beispiel: Button1.</span><span class="sxs-lookup"><span data-stu-id="f921d-115">For example, button1.</span></span>
-   <span data-ttu-id="f921d-116">Ein Entwickler weiß nicht, dass Bildschirm Sprachausgaben Namen und Steuerelement Typen lesen.</span><span class="sxs-lookup"><span data-stu-id="f921d-116">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f921d-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f921d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f921d-118">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="f921d-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="f921d-119">**Iuiautomationelement:: currentname**</span><span class="sxs-lookup"><span data-stu-id="f921d-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




