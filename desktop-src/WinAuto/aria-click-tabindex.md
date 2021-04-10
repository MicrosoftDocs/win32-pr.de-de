---
title: Aria-TabIndex-Fehler
description: Aria-TabIndex-Fehler
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- Ariatabindexerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039779"
---
# <a name="aria-tabindex-error"></a><span data-ttu-id="d4a04-104">Aria-TabIndex-Fehler</span><span class="sxs-lookup"><span data-stu-id="d4a04-104">ARIA Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="d4a04-105">Text</span><span class="sxs-lookup"><span data-stu-id="d4a04-105">Text</span></span>

<span data-ttu-id="d4a04-106">Das Element ist nicht deaktiviert und verfügt über einen **Click** -Ereignishandler, verfügt jedoch über **TabIndex** < 0 und ist nicht standardmäßig in der Aktivier Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d4a04-106">Element is not disabled and has a **click** event handler but it has **tabIndex** < 0 and is not in the tab order by default.</span></span>

## <a name="type"></a><span data-ttu-id="d4a04-107">type</span><span class="sxs-lookup"><span data-stu-id="d4a04-107">Type</span></span>

<span data-ttu-id="d4a04-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="d4a04-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d4a04-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4a04-109">Description</span></span>

<span data-ttu-id="d4a04-110">Dieser Fehler gilt für Elemente, die einen Click-Ereignishandler haben und nicht deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d4a04-110">This error applies to elements that have a click event handler and are not disabled.</span></span> <span data-ttu-id="d4a04-111">Diese Elemente müssen sich in der Aktivier Reihenfolge befinden.</span><span class="sxs-lookup"><span data-stu-id="d4a04-111">These elements must be in the tab order.</span></span> <span data-ttu-id="d4a04-112">Dadurch wird sichergestellt, dass ein Element mithilfe der Tab-Taste erreicht werden kann. auf diese Weise navigieren Benutzer in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="d4a04-112">This ensures that an element can be reached using the Tab key, which is how screen reader users typically navigate the UI.</span></span>

<span data-ttu-id="d4a04-113">Legen Sie zum Beheben dieses Fehlers das [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) -Attribut auf einen Wert fest, der größer oder gleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="d4a04-113">To fix this error, set the [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) attribute to a value that is equal to or greater than 0.</span></span> <span data-ttu-id="d4a04-114">Sie müssen das **TabIndex** -Attribut nicht explizit für Tags festlegen, die sich standardmäßig in der Aktivier Reihenfolge befinden, z. b [**. (mit**](https://developer.mozilla.org/docs/Web/HTML/Element/a) [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) -Attribut), [**Schaltfläche**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**Eingabe**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (mit Ausnahme von "Hidden"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**Textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)und [**Area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (als Teil der ImageMap).</span><span class="sxs-lookup"><span data-stu-id="d4a04-114">You do not need to explicitly set the **tabindex** attribute for tags that are in the tab order by default, such as [**a**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (with [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) attribute), [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluding "hidden"), [**select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea), and [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (as part of the image map).</span></span>

## <a name="example"></a><span data-ttu-id="d4a04-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4a04-115">Example</span></span>


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




