---
title: KeyboardShortcut (Eigenschaft)
description: Die KeyboardShortcut-Eigenschaft beschreibt eine Tastenkombination oder eine Tastenkombination, die ein angegebenes Barrierefreies Objekt aktiviert.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206786"
---
# <a name="keyboardshortcut-property"></a><span data-ttu-id="9219a-103">KeyboardShortcut (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9219a-103">KeyboardShortcut Property</span></span>

<span data-ttu-id="9219a-104">Die **KeyboardShortcut** -Eigenschaft beschreibt eine Tastenkombination oder eine Tastenkombination, die ein angegebenes Barrierefreies Objekt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9219a-104">The **KeyboardShortcut** property describes a key or key combination that activates a specified accessible object.</span></span>

<span data-ttu-id="9219a-105">Die **KeyboardShortcut** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9219a-105">The **KeyboardShortcut** property is retrieved by calling [**IAccessible::get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span></span>

<span data-ttu-id="9219a-106">Die abgerufene Zeichenfolge beschreibt eine *Tastenkombination* (auch als *Tastaturbeschleuniger* bezeichnet) oder eine *Zugriffstaste* (auch als *mnetmonisches* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="9219a-106">The retrieved string describes a *shortcut key* (also called a *keyboard accelerator*) or an *access key* (also called a *mnemonic*).</span></span> <span data-ttu-id="9219a-107">Eine Zugriffstaste ist ein unterstrichenes Zeichen im Text eines Menüs, Menü Elements oder einer Bezeichnung eines Steuer Elements, z. b. einer Schaltfläche "Push".</span><span class="sxs-lookup"><span data-stu-id="9219a-107">An access key is an underlined character in the text of a menu, menu item, or label of a control such as a push button.</span></span>

<span data-ttu-id="9219a-108">Die abgerufene Zeichenfolge muss den Namen des Schlüssels zusammen mit den modifiziererschlüsseln enthalten.</span><span class="sxs-lookup"><span data-stu-id="9219a-108">The retrieved string must contain the name of the key along with the modifier key or keys.</span></span> <span data-ttu-id="9219a-109">Die Zeichenfolge muss das folgende Format aufweisen, damit Clients Sie leicht analysieren können: \[ \[ modifiziererschlüssel \] + \[ ... \] + \] Key Name.</span><span class="sxs-lookup"><span data-stu-id="9219a-109">The string must be in the following format so that clients can easily parse it: \[\[modifier key\]+\[...\]+\] key name.</span></span>

<span data-ttu-id="9219a-110">Beispiele hierfür sind alt + F, STRG + ALT + 4, Win + F1, Strg + Alt + Umschalt + Rücktaste oder einfach RÜCKTASTE.</span><span class="sxs-lookup"><span data-stu-id="9219a-110">Examples include ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+SHIFT+BACKSPACE, or simply BACKSPACE.</span></span>

<span data-ttu-id="9219a-111">In der folgenden Tabelle sind modifiziererschlüssel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9219a-111">The following table lists modifier keys.</span></span>



| <span data-ttu-id="9219a-112">Zusatztaste</span><span class="sxs-lookup"><span data-stu-id="9219a-112">Modifier key</span></span> | <span data-ttu-id="9219a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9219a-113">Description</span></span>                        |
|--------------|------------------------------------|
| <span data-ttu-id="9219a-114">ALT</span><span class="sxs-lookup"><span data-stu-id="9219a-114">ALT</span></span>          | <span data-ttu-id="9219a-115">Alternative Modifizierertaste</span><span class="sxs-lookup"><span data-stu-id="9219a-115">Alternate modifier key</span></span>             |
| <span data-ttu-id="9219a-116">STRG</span><span class="sxs-lookup"><span data-stu-id="9219a-116">CTRL</span></span>         | <span data-ttu-id="9219a-117">Steuerelement-Modifizierertaste</span><span class="sxs-lookup"><span data-stu-id="9219a-117">Control modifier key</span></span>               |
| <span data-ttu-id="9219a-118">Schuss</span><span class="sxs-lookup"><span data-stu-id="9219a-118">SHIFT</span></span>        | <span data-ttu-id="9219a-119">UMSCHALT-Modifizierertaste</span><span class="sxs-lookup"><span data-stu-id="9219a-119">Shift modifier key</span></span>                 |
| <span data-ttu-id="9219a-120">Erringen</span><span class="sxs-lookup"><span data-stu-id="9219a-120">WIN</span></span>          | <span data-ttu-id="9219a-121">WINDOWS-TASTE</span><span class="sxs-lookup"><span data-stu-id="9219a-121">Windows logo key</span></span>                   |
| <span data-ttu-id="9219a-122">FN</span><span class="sxs-lookup"><span data-stu-id="9219a-122">FN</span></span>           | <span data-ttu-id="9219a-123">Funktionstaste auf tragbaren Computern</span><span class="sxs-lookup"><span data-stu-id="9219a-123">Function key on portable computers</span></span> |



 

<span data-ttu-id="9219a-124">Tastenkombinationen nicht lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="9219a-124">Do not localize keyboard shortcut strings.</span></span>

## <a name="handling-objects-that-have-both-key-types"></a><span data-ttu-id="9219a-125">Behandeln von Objekten, die über beide Schlüsseltypen verfügen</span><span class="sxs-lookup"><span data-stu-id="9219a-125">Handling Objects That Have Both Key Types</span></span>

<span data-ttu-id="9219a-126">Wenn ein Objekt über eine Tastenkombination und eine Zugriffstaste verfügt, gibt die **KeyboardShortcut** -Eigenschaft die Zugriffstaste zurück.</span><span class="sxs-lookup"><span data-stu-id="9219a-126">If an object has both a shortcut key and an access key, the **KeyboardShortcut** property returns the access key.</span></span> <span data-ttu-id="9219a-127">Der Zugriffsschlüssel ist der Schlüssel, den ein Benutzer drücken würde, wenn das Objekt oder das übergeordnete Objekt den Tastaturfokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="9219a-127">The access key is the one a user would press when the object or the object's parent has the keyboard focus.</span></span> <span data-ttu-id="9219a-128">Beispielsweise kann das Menü Element **Drucken** sowohl eine Tastenkombination (STRG + P) als auch eine Zugriffstaste (p) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9219a-128">For example, the **Print** menu item might have both a shortcut key (CTRL+P) and an access key (P).</span></span> <span data-ttu-id="9219a-129">Wenn ein Benutzer STRG + P drückt, während das Menü aktiv ist, geschieht nichts.</span><span class="sxs-lookup"><span data-stu-id="9219a-129">If a user presses CTRL+P while the menu is active, nothing happens.</span></span> <span data-ttu-id="9219a-130">Wenn ein Benutzer jedoch P drückt, während das Menü aktiv ist, wird das Dialogfeld **Drucken** der Anwendung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9219a-130">But if a user presses P while the menu is active, it invokes the application's **Print** dialog box.</span></span> <span data-ttu-id="9219a-131">In diesem Fall ist die **KeyboardShortcut** -Eigenschaft "P", um widerzuspiegeln, was der Benutzer drücken muss, wenn das Menü den Tastaturfokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="9219a-131">In this case, the **KeyboardShortcut** property is "P" to reflect what the user must press when the menu has the keyboard focus.</span></span>

 

 




